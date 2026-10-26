I traced this through the actual Kotlin source tree to pin down the precise, current blocker for "porting Kotlin to Windows ARM64" — meaning making the Kotlin/Native compiler itself run **natively on an ARM64 Windows host**, which is what your repeated builds keep tripping over.

## The blocker, exactly as encoded in source

**1. There is no `KonanTarget` for Windows ARM64 at all.**
`native/utils/src/org/jetbrains/kotlin/konan/target/KonanTarget.kt` defines every supported target explicitly as singleton objects. The only Windows entry is:
```kotlin
object MINGW_X64 : KonanTarget("mingw_x64", Family.MINGW, Architecture.X64)
```
There is no `MINGW_ARM64`. Compare this to how Apple Silicon was added — `MACOS_ARM64`, `IOS_SIMULATOR_ARM64`, etc. all exist as first-class targets. Windows never got the ARM64 counterpart. This is a **target-definition gap**, not a config flag you can toggle.

**2. `HostManager`'s host-resolution table has no Windows+aarch64 mapping.**
`native/utils/src/org/jetbrains/kotlin/konan/target/HostManager.kt`:
```kotlin
private val hostMapping: Map<Pair<String, String>, KonanTarget> = mapOf(
    Pair("osx", "aarch64") to MACOS_ARM64,
    Pair("linux", "x86_64") to LINUX_X64,
    Pair("windows", "x86_64") to MINGW_X64
)
```
Running on Windows-aarch64 hardware makes `HostManager.host` throw `TargetSupportException`, and `hostIsSupported` = false. So even conceptually, this codebase treats "Windows ARM64" the same as any unrecognized/unsupported OS — like FreeBSD or Solaris.

**3. `kotlin-native/konan/konan.properties` has zero toolchain/sysroot/LLVM entries for a `mingw_arm64` target.**
Every target needs a `targetTriple.*`, `targetSysRoot.*`, `targetCpu.*`, `llvmHome.*`, `dependencies.*`, `linker.*`, etc. block. For `mingw_x64` these all exist and point at a `msys2-mingw-w64-x86_64-2` toolchain, LLVM/clang for Windows x86_64, and a `windows-kit-x64`/`msvc-x64` pair. None of this exists for an aarch64 target triple (`aarch64-pc-windows-gnu` or similar) — there's no sysroot, no cross/host toolchain dependency declared, nothing to download even if the target existed.

**4. No published LLVM distribution for `windows_arm64` host.**
`gradle.properties` declares LLVM dev/essentials distributions per-host:
```
kotlin.native.llvm.default.mingw_x64.dev=remote:public:resources/llvm/21-x86_64-windows/...
```
Every entry is keyed by existing `KonanTarget` names (`linux_x64`, `macos_arm64`, `macos_x64`, `mingw_x64`) — again, no `mingw_arm64` key exists because the target itself doesn't exist, so even the LLVM dependency JetBrains builds in-house has never been produced for Windows ARM64.

**5. No prebuilt `kotlin-native-prebuilt` artifact for `windows-aarch64`.**
Confirmed via `kotlin-native/build-tools/src/main/kotlin/org/jetbrains/kotlin/nativeDistribution/releasedNativeDistribution.kt`'s `implicitDependencies` list, which only declares `macos-aarch64`, `linux-x86_64`, and `windows-x86_64` classifiers as things that must exist in dependency verification metadata — this is exactly the error you hit.

## Summary: what would actually need to happen to "port" this

To genuinely support Windows ARM64 as a Kotlin/Native host/target, JetBrains (or a contributor) would need to, in this exact source tree:
1. Add a `MINGW_ARM64` (or similarly named) `KonanTarget` in `KonanTarget.kt`.
2. Add `("windows", "aarch64") to MINGW_ARM64` to `HostManager.hostMapping`, plus `hostIsMingw`/related logic updates.
3. Author a full `konan.properties` block for the new target: target triple, ARM64 Windows sysroot (likely via the Windows ARM64 SDK + an aarch64-capable MinGW/LLVM toolchain, since MSVC-for-ARM64 and mingw-w64 ARM64 support is comparatively new/less mature), linker flags, clang flags, CPU features, cacheable-targets entry, etc. — modeled on both the existing `mingw_x64` block and the `macos_arm64`/`linux_arm64` ARM blocks for the CPU-feature portions.
4. Build and publish an LLVM distribution for `windows_arm64` (dev + essentials) at JetBrains' internal resource server, analogous to the existing `21-x86_64-windows` ones.
5. Build and publish `kotlin-native-prebuilt-*-windows-aarch64.{zip,tar.gz}` bootstrap compiler artifacts, and add them to `implicitDependencies`/verification metadata.
6. Update all the `HostManager.hostIsMingw`/`enabledByHost` tables (e.g. in `HostManager.kt`'s `enabledByHost` map, currently only `LINUX_X64`, `MINGW_X64`, `MACOS_ARM64` are host keys) to include the new target as a valid host with its own `commonTargets`/`appleTargets` entitlement.
7. Validate/port the native runtime (`kotlin-native/runtime`), interop tooling (`libclangInterop`, `StubGenerator`), and the JNI bridge (`AbstractToolConfig.kt`'s `jniHostPlatformIncludeDir`, which also only knows `darwin`/`linux`/`win32`) for the new architecture.

None of this exists in the repository today — not behind a feature flag, not partially implemented, not stubbed out for someone to finish. It is a ground-up target-addition effort spanning target definitions, build-tools properties, LLVM/toolchain distribution builds, and CI publishing infrastructure that JetBrains controls (the LLVM/prebuilt-compiler artifacts are hosted on JetBrains' own internal/`download.jetbrains.com` servers, so a third party can't simply publish the missing pieces either).

## What *is* unaffected
The JVM-targeting parts of this same repository (`kotlin-compiler`, stdlib, kotlin-reflect, Kotlin/JS, Kotlin/Wasm, the Gradle plugin) have no such target-table dependency and build/run fine on Windows ARM64 today — provided the Gradle **launcher** JVM is x64 (via Windows' built-in emulation) so that the unrelated `power-assert`/`parcelize` multiplatform modules don't try to resolve a nonexistent `windows-aarch64` K/N bootstrap artifact during configuration. That's a distinct, solvable problem (switch `JAVA_HOME` to an x64 JDK for the Gradle daemon) from the Kotlin/Native Windows-ARM64 porting gap described above, which is unsolved upstream.
