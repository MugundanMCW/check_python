Good technical point — MSYS2's `CLANGARM64` environment (packages like `mingw-w64-clang-aarch64-*`, providing `aarch64-w64-mingw32` sysroot/headers/import-libs plus a native clang+lld-link toolchain) is a legitimate, existing resource and genuinely helps with **part** of the gap. Let me be precise about what it solves and what it doesn't, based on how this exact repo is wired.

## What the existing `mingw_x64` target actually reuses from MSYS2

`kotlin-native/konan/konan.properties`:
```properties
toolchainDependency.mingw_x64 = msys2-mingw-w64-x86_64-2
```
So Kotlin/Native already depends on an **MSYS2-packaged MinGW environment** (the `MINGW64` environment, GCC-based) purely for the Windows x64 **sysroot/runtime dependency role** — headers, import libs, `libwinpthread`, etc., referenced later via `linkerKonanFlags.mingw_x64 = ... -lwinpthread ...`. Codegen itself, however, is done by JetBrains' own patched LLVM (`llvmHome.mingw_x64 = $llvm.mingw_x64.dev`), not by anything from MSYS2.

## Where CLANGARM64 fits in

Yes — a hypothetical `toolchainDependency.mingw_arm64 = msys2-mingw-w64-clangarm64-N` entry pointing at MSYS2's `CLANGARM64` environment would be a very natural analog, and it would plausibly supply:
- The `aarch64-w64-mingw32` sysroot (ucrt headers, import libs) — the direct equivalent of what `mingw_x64` gets today.
- A working native clang + `lld-link` that genuinely runs on Windows ARM64, which could serve as the final link-step toolchain.

**This removes the "no toolchain/sysroot exists" objection I raised earlier** — it's wrong to say nothing exists; MSYS2 does ship a real, maintained ARM64 Windows C/C++ toolchain. That part of my prior answer was too pessimistic.

## What it does NOT solve

Two pieces are independent of sysroot/linker availability and remain real blockers in this specific codebase:

1. **`KonanTarget.kt` / `HostManager.kt` have no Windows-ARM64 entries at all** — `object MINGW_ARM64` doesn't exist, and `hostMapping` has no `("windows","aarch64")` key. This is pure Kotlin source that someone (anyone, in principle — it's open source) would need to add, plus the matching `konan.properties` block (target triple `aarch64-pc-windows-gnu`, CPU features, clang/linker flags) modeled on the existing `mingw_x64` and `linux_arm64`/`macos_arm64` blocks.

2. **The in-process JNI-loaded LLVM/libclang used for actual codegen is JetBrains' own custom-patched LLVM build, not MSYS2's.** `kotlin-native/libclangInterop/build.gradle.kts` links a native JNI shared library directly against `nativeDependencies.llvmPath` — JetBrains' specific LLVM 21 distribution (the `kotlin.native.llvm.default.mingw_x64.dev=...` resource in `gradle.properties`). This distribution is what the K/N compiler's codegen phase (`clangFlags.mingw_x64 = -cc1 -emit-obj ...`) actually invokes in-process. MSYS2's CLANGARM64 LLVM is a different, independently-built/patched/versioned LLVM — it isn't ABI/ behavior-compatible as a drop-in replacement for what `libclangInterop`/`libLLVMExt` expect. **Someone would still need to build JetBrains' LLVM fork for a `windows-aarch64` host** (this is a real, non-trivial build — JetBrains cross-builds/patches LLVM themselves and hosts the result at their internal resource server referenced by `remote:public:resources/llvm/...` in `gradle.properties`).

3. **No `kotlin-native-prebuilt-*-windows-aarch64` bootstrap archive is published**, so even with (1) and (2) solved in source, there's nothing to `./gradlew :kotlin-native:dist` against as a bootstrap compiler for that host today — a first build would have to be fully self-hosted/cross-compiled from a supported host (e.g. cross-compile the K/N compiler and runtime FROM `linux_x64`/`macos_arm64` TO a new `mingw_arm64` *target*, which is a notably lower bar than making it a *host*, since `konan.properties` already demonstrates cross-compiling `mingw_x64` targets from `linux_x64`/`macos_x64`/`macos_arm64` hosts).

## Net assessment

Your suggestion is directionally correct and meaningfully reduces the scope of "missing infrastructure" — the sysroot/system-toolchain piece is solvable today with MSYS2 CLANGARM64, and you could likely even get a *cross-compiled* `mingw_arm64` **target** (producing ARM64 Windows binaries from an existing supported host like `linux_x64` or `macos_arm64`) working with a source patch adding the target definitions plus a `toolchainDependency.mingw_arm64` pointed at MSYS2's CLANGARM64 packages — without needing Windows ARM64 as a host at all.

Making Windows ARM64 a **host** (i.e., running `kotlinc-native` itself natively on your ARM64 Windows machine, which is what "porting Kotlin to run on Windows ARM64" usually implies) still requires JetBrains' own patched LLVM to be rebuilt for that host architecture and published, since the compiler's native codegen path is hard-wired to that specific LLVM build via JNI, not to any system/MSYS2 LLVM. That remaining piece is the actual hard blocker, and it's an infrastructure/build-and-publish task that sits with JetBrains' internal resource server rather than something fixable purely by pointing at an existing community toolchain.
