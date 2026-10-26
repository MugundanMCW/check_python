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
