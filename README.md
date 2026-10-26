## Build command for LLVM on Windows ARM64

Based on `kotlin-native/tools/llvm_builder/package.py` and `README.md` in this repo, run from a Windows ARM64 machine with Python 3, CMake, Ninja, Git, and Visual Studio (with the ARM64 C++ build tools component installed) all present:

### Prerequisites first
```powershell
cd kotlin-native\tools\llvm_builder

# Must be run from a shell where these are on PATH, or pass --ninja/--cmake/--git explicitly:
#   python3, cmake, ninja, git
# Visual Studio must have the ARM64 native toolset installed
# (Visual Studio Installer -> "Desktop development with C++" -> add "MSVC v143 - VS 2022 C++ ARM64 build tools")
```

### Basic full build (default: 2-stage bootstrap, all components)
```powershell
python3 package.py
```
This clones `https://github.com/Kotlin/llvm-project` (branch `kotlin/llvm-21-apple` by default), builds a stage-1 bootstrap LLVM from scratch using whatever `cl.exe`/`clang-cl.exe` the VS ARM64 dev environment provides, then uses that to build the final stage-2 distribution into `./llvm-distribution`. With my fix, the VsDevCmd invocation will now use `-arch=arm64` automatically on your ARM64 host instead of always forcing `amd64`.

### Recommended for a first/validation attempt — minimal, end-user-only components, packaged
```powershell
python3 package.py `
  --build-targets install-distribution `
  --distribution-components clang libclang lld llvm-cov llvm-profdata llvm-ar clang-resource-headers `
  --install-path llvm-windows-arm64 `
  --pack
```
This matches the documented "distribution for end-users" set for Windows from the README, skips building unnecessary LLVM tooling, and produces a zip + `.sha256` at the end (`--pack` always zips on Windows per `host_default_compression()`).

### If the full bootstrap is too slow/risky for a first test
```powershell
python3 package.py --num-stages 1 --install-path llvm-windows-arm64-test --dry-run
```
`--dry-run` just prints the exact `cmake`/`ninja` commands it would run without executing them — useful to sanity-check the generated CMake invocation (confirm it's picking `-arch=arm64`, the right compiler paths, etc.) before committing to a multi-hour build. Drop `--dry-run` once it looks right.

### Key flags you'll likely need, from `package.py -h`
| Flag | Purpose |
|---|---|
| `--vsdevcmd <path>` | Explicit path to `VsDevCmd.bat` if auto-detection via `vswhere` fails |
| `--stage0 <path>` | Point at an existing LLVM toolchain to use as the bootstrap compiler instead of building one from scratch — **you won't have one for this host yet**, so the first run must omit this and let it self-bootstrap |
| `--num-stages 1` | Skip the bootstrap stage entirely (uses your system/VS compiler directly for the single stage) — faster, less "reproducible," good for an initial feasibility test |
| `--save-temporary-files` | Keep intermediate `llvm-stage-*` dirs around for debugging if something fails mid-build |
| `--debug-cmake` | Adds `--debug-trycompile` to CMake, preserves `CMakeError.log` if CMake's own compiler-detection step fails |

### After it builds
Per `kotlin-native/BUILDING_LLVM.md`, point Kotlin/Native's own build at your fresh LLVM:
```powershell
# in the kotlin repo root, pass on the gradle command line:
gradlew.bat ... -Pkotlin.native.llvm=C:\path\to\llvm-windows-arm64 -Pkotlin.native.llvm.next.mingw_arm64.version=<llvm-version>
```
(`<llvm-version>` is whatever's under `<dist>/lib/clang/<version>/include` in your output — the doc explains this lookup.) This still requires the `llvmHome.mingw_arm64`/host wiring I scaffolded earlier in `konan.properties`/`gradle.properties` to actually be filled in and exercised — that part remains unverified since no such build has been run.

**Reminder:** this is the first-ever attempt at this host/arch combination in this codebase. Expect to hit and need to fix additional issues beyond the one `-arch=amd64` bug already corrected — treat the above as a starting point, not a guaranteed-working recipe.


## Source code locations

**1. JetBrains-built LLVM fork**
Repository: **https://github.com/Kotlin/llvm-project**
Branch convention: `kotlin/llvm-<version>-<platform>` (e.g. `kotlin/llvm-21-apple` is referenced as the current default in this repo)

Found directly in this checkout at `kotlin-native/tools/llvm_builder/package.py`:
```python
default_repo = "https://github.com/Kotlin/llvm-project"
default_branch = "kotlin/llvm-21-apple"
```
This is JetBrains' fork of the official `llvm/llvm-project`, patched for Kotlin/Native's needs (opaque pointers, signal-handler fixes, etc. — see `docs/changelogs/*.md` entries like `KT-61299 Native: patch LLVM to prevent it from using signal handlers incompatibly with JVM`). The build script and instructions live in this same repo at:
- `kotlin-native/BUILDING_LLVM.md`
- `kotlin-native/tools/llvm_builder/README.md` and `package.py`

This is the exact thing someone would need to branch/extend with Windows-ARM64 build support to solve blocker #1.

**2. `kotlin-native-prebuilt`**
This is **not a separate repository** — it's a published Maven artifact built directly from this `JetBrains/kotlin` monorepo's `kotlin-native/` subtree. Confirmed in `kotlin-native/build-tools/src/main/kotlin/org/jetbrains/kotlin/nativeDistribution/releasedNativeDistribution.kt`:
```kotlin
"implicitDependencies"("org.jetbrains.kotlin:kotlin-native-prebuilt:$version:macos-aarch64@tar.gz")
"implicitDependencies"("org.jetbrains.kotlin:kotlin-native-prebuilt:$version:linux-x86_64@tar.gz")
"implicitDependencies"("org.jetbrains.kotlin:kotlin-native-prebuilt:$version:windows-x86_64@zip")
```
There's no separate "prebuilt" source project — it's produced by running this repo's own build (the `:kotlin-native:dist`/`:kotlin-native:bundle` Gradle tasks described in `kotlin-native/README.md`) on each of JetBrains' CI build agents (one per supported host: `macos-aarch64`, `linux-x86_64`, `windows-x86_64`) and publishing the resulting archive. To get a `windows-aarch64` variant, JetBrains would need to run that same build on a Windows ARM64 CI agent and publish the output under that new classifier — which in turn requires blocker #1 (the LLVM fork) to exist for that host first.

**In short:** `github.com/Kotlin/llvm-project` is the actual upstream to extend for the LLVM blocker; `kotlin-native-prebuilt` has no separate source — it's just this repo's own `kotlin-native/` build output, republished per-host.

**Yes, that's exactly right.** The chain is:

```
Windows-ARM64 Kotlin/Native support
        requires
Windows-ARM64 build of JetBrains' LLVM fork (github.com/Kotlin/llvm-project)
        which is needed to produce
kotlin-native-prebuilt:<version>:windows-aarch64 artifact
        which is needed for
Kotlin/Native to run natively as a compiler on Windows ARM64
```

**Why this is the real bottleneck:**
`kotlin-native-prebuilt` isn't a separately maintained binary — it's just this repo's own `kotlin-native/` subtree, built on a CI machine with the matching host LLVM already present, then zipped/published. There's no missing "source code" step for it; it's produced by the exact `./gradlew :kotlin-native:dist` build already in this repo (see `kotlin-native/README.md`), run once per supported host.

The one real precondition that build has is: `kotlin-native/konan/konan.properties` says `llvmHome.<host> = $llvm.<host>.dev`, and that LLVM has to already exist for the host running the build (`kotlin-native/tools/llvm_builder/package.py` builds it from `github.com/Kotlin/llvm-project`, branch `kotlin/llvm-21-apple`-style). Looking at `package.py`, it only special-cases `host_is_windows()` for toolchain invocation (MSVC/vsdevcmd, zip packaging) — it does **not** currently appear to special-case or validate CPU architecture beyond that, so it's plausible the script could be pointed at a Windows ARM64 machine with the right toolchain (Clang/LLVM's own build system is itself cross-compile/self-host capable for ARM64 Windows in principle), but this is unverified/untested territory — nobody at JetBrains has done it, so there could be unknown build-system issues specific to that host triple.

**So concretely, to unblock Windows ARM64 as a real Kotlin/Native host, someone needs to:**
1. Get `llvm_builder/package.py` to successfully build LLVM **on/for** a `windows-aarch64` host (this is the actual unknown/untested step — could be straightforward or could hit real snags, since it's never been attempted for this target).
2. Point a `windows-aarch64` K/N build at that LLVM output via `kotlin.native.llvm=<path>` (documented in `BUILDING_LLVM.md`) and run `./gradlew :kotlin-native:dist` on that same ARM64 machine.
3. Publish that output as `kotlin-native-prebuilt:<version>:windows-aarch64` so future builds can download it instead of re-building from scratch.

Everything else (the `MINGW_ARM64` target wiring I added to the Kotlin source, the MSYS2 CLANGARM64 sysroot/linker) only matters for *cross-compiling to* Windows ARM64 as an output target — it doesn't help with step 1, which is the actual gate on using Windows ARM64 *as the machine running the compiler*.
