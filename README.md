# Building Kotlin/Native for Windows ARM64 (`mingw_arm64`) without a `windows-aarch64` prebuilt

This builds `kotlin-native-prebuilt-windows-aarch64-<version>.zip`: a Kotlin/Native compiler distribution that runs
natively on Windows on ARM64 and compiles programs for `mingw_arm64` (`aarch64-pc-windows-gnu`).
JetBrains does not publish a `windows-aarch64` prebuilt, and the normal build needs one to bootstrap. Here the
bootstrap is replaced by compiling the compiler, the stub DLLs, the stdlib and the runtime from this checkout.

**Status: experimental.** Verified end to end on one machine (see "What was verified"). Not upstream-ready.

## What you get

* `kotlin-native-prebuilt-windows-aarch64-2.5.255-SNAPSHOT.zip` (~85 MB), layout identical to JetBrains' prebuilt:
  `bin/`, `klib/` (stdlib + 8 `mingw_arm64` platform libs), `konan/` (compiler jar, 5 ARM64 JNI DLLs, `konan.properties`,
  runtime bitcode), `licenses/`, `sources/`, `tools/`.
* **Only the `mingw_arm64` target** is in it. No Linux/Android/Apple/`mingw_x64` runtimes or platform libs.
* It does **not** contain LLVM or a MinGW toolchain. Compiling needs the two local directories from steps 1 and 4.

## Contents of this folder

| File | Purpose |
|---|---|
| `kotlin-windows-arm64.patch` | All source/build changes (23 files). Apply on top of commit `4670e95d024e`. |
| `scripts/setup-toolchain.ps1` | Step 4: assembles the dev LLVM directory and the libffi directory. |
| `scripts/build-prebuilt.ps1` | Step 6: runs the Gradle builds and produces the zip. |
| `scripts/smoke-test.ps1` | Step 7: extracts the zip, compiles and runs two sample programs. |

## 0. Requirements

| What | Notes |
|---|---|
| Windows 11 on ARM64 | All builds run natively. |
| Visual Studio 2022 (or newer) with the **ARM64 C++ build tools** and a Windows 10/11 SDK | Needed to build LLVM, and by clang for the JNI libraries. Tested with MSVC 14.44 and SDK 10.0.28000. |
| Python 3, CMake, Ninja, Git | On `PATH`. Tested with CMake in `C:\CMake`, Ninja in `C:\ninja`. |
| MSYS2 with the **CLANGARM64** packages | Step 1. Provides the MinGW sysroot, libc++, libunwind, compiler-rt, libffi. |
| An **ARM64 JDK 17+** to start Gradle, and an **ARM64 JDK 21** to run the compiler | We used Microsoft OpenJDK 17.0.15 and Eclipse Temurin 21 (aarch64). |
| JDKs **8, 11, 17 and 25** for Gradle toolchains | They only compile sources and do not end up in the output. We used x64 Temurin builds; ARM64 builds work too wherever they exist. Keep them outside `~/.gradle/jdks` (see Troubleshooting). |
| ~40 GB free disk, and a lot of time for step 3 | LLVM stage 2 is built with all cores. |

## 1. MSYS2 CLANGARM64

Install MSYS2, open the **CLANGARM64** shell and run:

```
pacman -S mingw-w64-clang-aarch64-toolchain mingw-w64-clang-aarch64-libffi
```

On the reference machine this resulted in: `clang 23.1.4`, `libffi 3.8.0`, `mingw-w64 headers 14.0.0`, plus
`compiler-rt`, `libc++`, `libunwind`, `winpthreads`, `lld`. The prefix used below is `C:\msys64\clangarm64`.
(Only the installed set above was verified; the package group name is the usual one for this environment.)

## 2. Get the source and apply the patch

```
git checkout 4670e95d024e          # "Native: experimental Windows ARM64 (mingw_arm64) host support"
git apply <this folder>\kotlin-windows-arm64.patch
copy local.properties.mingw_arm64.example local.properties     # the example from that commit
```

`local.properties` must contain `kotlin.native.enabled=true` (`build-prebuilt.ps1` adds it if missing). The LLVM path
line in that example is **not** honored by the build; the LLVM path is passed on the Gradle command line (step 6).

The patch assumes the commit above. Without it, the `HostManager`/`konan.properties` entries it builds on are missing.

## 3. Build LLVM natively for ARM64

From an **"ARM64 Native Tools Command Prompt for VS"**:

```
cd kotlin-native\tools\llvm_builder
python package.py --build-targets install-distribution --distribution-components clang libclang lld llvm-ar clang-resource-headers
```

This is the invocation that matches the CMake cache of the build tree used here
(`LLVM_ENABLE_PROJECTS=clang;lld`, `LLVM_ENABLE_RUNTIMES=compiler-rt`, `LLVM_TARGETS_TO_BUILD=all`, Release, 2 stages).
It leaves `llvm-distribution\`, `llvm-stage-1\`, `llvm-stage-2-build\` and `llvm-project\` in that directory.
The tree used for this build was produced with that configuration; the exact command line was not re-run for this guide.

## 4. Assemble the dev LLVM directory and the libffi directory

The Native build expects an LLVM with headers, all static libraries and more tools than the trimmed distribution
contains, and it must not see MSYS2's full `include` tree through libffi. One script does it:

```
powershell -ExecutionPolicy Bypass -File scripts\setup-toolchain.ps1 `
    -LlvmBuilderDir <checkout>\kotlin-native\tools\llvm_builder
```

Defaults: `C:\llvm-arm64-dev-full` and `C:\libffi-arm64` (the latter is the path set in `konan.properties`:
`libffiDir.mingw_arm64`). It builds 28 extra LLVM tools plus `LLVMMCA` / `LLVMX86TargetMCA` with the stage-2 ARM64
`clang-cl`, installs headers and static libs, adds `lld-link.exe` and the ARM64 compiler-rt builtins from MSYS2, and
verifies that every `.exe`/`.dll` in `bin` is ARM64.

## 5. Check the toolchain by hand (optional)

```
C:\llvm-arm64-dev-full\bin\clang.exe --version        # Target: aarch64-pc-windows-msvc
```

## 6. Build the prebuilt zip

```
powershell -ExecutionPolicy Bypass -File scripts\build-prebuilt.ps1 `
    -KotlinRoot <checkout> `
    -ClientJdk 'C:\Program Files\Microsoft\jdk-17.0.15.6-hotspot' `
    -ToolchainJdks C:\jdks\jdk8, C:\jdks\jdk11, C:\jdks\jdk17, C:\jdks\jdk25
```

It runs, with `PATH` stripped of entries containing parentheses (needed by `run_konan.bat`):

```
gradlew :kotlin-native:dist :kotlin-native:distPlatformLibs
gradlew :kotlin-native:bundlePrebuilt -x :kotlin-native:crossDist -x :kotlin-native:crossDistStdlibCache -x :kotlin-native:crossDistPlatformLibs
```

with these flags on both: `-Pkotlin.native.llvm=C:/llvm-arm64-dev-full`,
`-Pkotlin.native.llvm.next.mingw_arm64.version=21` (the `lib\clang\<N>` directory name),
`-Dorg.gradle.java.installations.paths=<the four JDKs>`, `-Dorg.gradle.java.installations.auto-download=false`.
The output is `kotlin-native\kotlin-native-prebuilt-windows-aarch64-<version>.zip`.

Order of work inside Gradle, for orientation: the compiler jar and the five ARM64 JNI DLLs are built from source;
then the Native stdlib is compiled by that in-tree compiler (no bootstrap compiler); then the C++ runtime is compiled to
bitcode with MSYS2 clang + libc++; then platform libraries are generated; then the zip is created.

## 7. Smoke test

```
powershell -ExecutionPolicy Bypass -File scripts\smoke-test.ps1 `
    -Zip <checkout>\kotlin-native\kotlin-native-prebuilt-windows-aarch64-2.5.255-SNAPSHOT.zip `
    -Jdk C:\Users\<you>\.gradle\jdks\eclipse_adoptium-21-aarch64-windows.2
```

It extracts the zip into a new temp folder, compiles `hello.kt` and a program that uses `platform.posix` and
`platform.windows`, checks the executables' PE machine type (must be `aa64`) and runs them.

To compile your own code with the extracted distribution (the compiler is started with `java` directly because
`bin\konanc.bat` breaks on a `PATH` containing `Program Files (x86)`):

```powershell
$kn   = 'C:\kn\kotlin-native-prebuilt-windows-aarch64-2.5.255-SNAPSHOT'
$java = '<arm64 JDK>\bin\java.exe'
$env:PATH = 'C:\llvm-arm64-dev-full\bin;C:\msys64\clangarm64\bin;' + $env:PATH
& $java -ea -Xmx3G "-Dkonan.home=$kn" -cp "$kn\konan\lib\kotlin-native-compiler-embeddable.jar" `
    org.jetbrains.kotlin.cli.utilities.MainKt konanc hello.kt -o hello -target mingw_arm64 `
    "-Xoverride-konan-properties=llvm.mingw_arm64.dev=C:/llvm-arm64-dev-full;llvmVersion.mingw_arm64=21"
```

## What the patch does

| Area | Change |
|---|---|
| Host detection | `build-tools` compiles the in-repo `native/utils` sources instead of the published bootstrap `kotlin-native-utils` (which does not know Windows ARM64). `LLVMDistributionSource.kt` no longer lists `MINGW_ARM64` as a downloadable-LLVM host. |
| No bootstrap for cinterop | `libclangInterop` uses pre-generated sources `gen/main-mingw_arm64/{kotlin,c}` (`usePrebuiltSources=true`). They are byte-identical to what the in-repo generator produces on ARM64 (checked), so the bootstrap loop is closed. |
| Stdlib | `runtime/build.gradle.kts`: on `mingw_arm64`, `stdlibBuildTask` uses the in-tree compiler (`nativeDistribution` + `:kotlin-native:distCompiler`) instead of the released prebuilt. |
| JNI stub DLLs | `Interop/Runtime`: `-DFFI_STATIC_BUILD`, compiler-rt link, new `ssp_compat.c` (stack-protector symbols). `ClangArgs.kt`: libc++ for C++ on `mingw_arm64`. |
| Runtime sources | `StackTrace.cpp` (ARM64 `CONTEXT.Pc`), missing `<exception>` / `<system_error>` includes, `NOMINMAX` for `mingw_arm64`. |
| Toolchain config | `konan.properties`: MSYS2 sysroot, libffi dir, `-stdlib=libc++ -rtlib=compiler-rt -unwindlib=libunwind`, nothing to download for the host. |
| Platform libraries | `posix.def`, `windows.def`, `winhttp.def` adapted to current MinGW-w64 headers; `mingw_arm64`-only `WINAPI_FAMILY=100`, so x64 is unaffected. |
| Skipped native targets | Modules that register Kotlin/Native targets and would ask for the missing prebuilt skip them on `mingw_arm64` (`parcelize-runtime`, `plugin-annotations`, `power-assert-runtime`, `kotlin-test-native-xctest`, two test-library plugins/projects). Local workaround; prints `No Kotlin Targets Declared`. |
| `wasm/wasm.tests` | Treats Windows ARM64 as x64 for its test tools. |

## What was verified

* All five JNI DLLs and all 36 LLVM binaries are ARM64 (PE machine `aa64`).
* The stdlib manifest says `compiler_version=2.5.255-SNAPSHOT` (the in-tree compiler built it); runtime bitcode has
  `target triple = "aarch64-pc-windows-gnu"`.
* A program using `platform.posix` and `platform.windows` compiled with the **extracted** zip, linked, ran, and the
  executable is ARM64.

## Known limitations

* `mingw_arm64` only; no other target runtimes or platform libraries in the bundle.
* Version is the repo default `2.5.255-SNAPSHOT`, not JetBrains' `2.5.20-dev-953`. Renaming the file is not enough: the
  compiler embeds its version, so a different name needs a rebuild with `-PdeployVersion`/`-Pbuild.number`.
* The distribution is not self-contained: compiling needs LLVM (step 4) and the MSYS2 sysroot at the paths above, and
  the LLVM path must be passed with `-Xoverride-konan-properties`.
* Only small programs were tested (stdlib, `platform.posix`, `platform.windows`). Coroutines, threads, GC under load,
  custom cinterop `.def` files and the Kotlin Gradle plugin were **not** tested.
* Hard-coded `C:/` paths in `konan.properties`, and the skip-native-targets edits, make the patch unsuitable for upstream as is.
  The runtime, `.def` and `ClangArgs` changes are generic portability fixes that could be upstreamed.
* `distStdlibCache` is a no-op for `mingw_arm64` (`cacheableTargets.mingw_arm64` is empty), so no precompiled caches.

## Troubleshooting

| Symptom | Cause / fix |
|---|---|
| `\Microsoft was unexpected at this time.` / cinterop task exits 255 | `PATH` contains `)` (e.g. `Program Files (x86)`); `run_konan.bat` breaks. `build-prebuilt.ps1` strips those entries; do the same in your own shell. |
| `Timeout waiting to lock Compressed Files Expansion Cache` or "file in use" on a DLL in `dist` | Two Gradle builds ran at once. Run `gradlew --stop` and use one build at a time. |
| `Unknown host target: windows aarch64` | The patch is not applied, or Gradle runs on an x64 JDK that the daemon JVM criteria did not pick. Use an ARM64 JDK. |
| Toolchain JDK download fails with `... -> ...\.gradle\jdks\temurin-8-...` | Gradle could not move the downloaded JDK into place. Install the JDKs yourself and pass them with `-Dorg.gradle.java.installations.paths`, with auto-download off (as the script does). |
| `llvm-link` / `opt` / `llc` not found | Run step 4; the trimmed LLVM distribution does not contain them. |
| `lld: error: unable to find library -lstdc++` / `-lgcc` | `konan.properties` flags not updated (patch missing), or the compiler-rt builtins are not under `lib\clang\<N>\lib\windows`. |
