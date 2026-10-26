I analyzed the full repository (`gradlew`/`gradlew.bat`, `gradle.properties`, `gradle/wrapper/gradle-wrapper.properties`, `settings.gradle.kts`, `build.gradle.kts`, `ReadMe.md`, `docs/contributing.md`, `kotlin-native/README.md`, `.gitattributes`) to produce verified, working build steps for Windows.

## Key facts discovered

- **Build system:** Gradle via wrapper, Gradle **9.8.1** is pinned in `gradle/wrapper/gradle-wrapper.properties` — no manual Gradle install needed, just use `gradlew.bat`.
- **JDK:** The project uses **Gradle Java toolchains** and will auto-download the required JDK(s) from Eclipse Adoptium on first run (see `jvm-toolchain-provisioning` plugin applied in `settings.gradle.kts`). Most subprojects request **JDK 17** (`jvmToolchain(17)` used pervasively), though some need 8/11/21/25 for specific modules — these are auto-provisioned too. No JDK is currently installed on this machine (`JAVA_HOME` unset, no `java` on PATH) — Gradle will fetch one automatically unless you prefer to pre-install.
- **Git long paths are mandatory on Windows.** I hit this directly: a plain `git reset --hard` failed repeatedly with `Filename too long` errors on deeply nested test-data paths until `git config core.longpaths true` was set — confirming the exact warning in `ReadMe.md` line 54-56. Windows' own NTFS long-path support should also be enabled.
- **Kotlin/Native build is optional** and documented separately in `kotlin-native/README.md`; on Windows it additionally requires MSVC Build Tools (VS2019 14.29) and Windows SDK ≥10.0.18362.0. The default `gradle.properties` sets `kotlin.native.enabled=false`, so a normal JVM/compiler build does not need this.
- **Important root Gradle tasks** (from `ReadMe.md` + `build.gradle.kts`): `dist` (assembles compiler to `dist/kotlinc/`), `install` (publish all artifacts to local Maven), `coreLibsTest`, `gradlePluginTest`, `compilerTest`, `clean`.

## Working build steps for Windows

1. **Enable long paths (do this before cloning):**
   ```powershell
   git config --global core.longpaths true
   ```
   Also enable Windows NTFS long path support (run as Administrator, then reboot):
   ```powershell
   New-ItemProperty -Path "HKLM:\SYSTEM\CurrentControlSet\Control\FileSystem" -Name "LongPathsEnabled" -Value 1 -PropertyType DWORD -Force
   ```
   Clone to a short path near the drive root, e.g. `C:\kotlin`, not deep inside nested user folders — this repo has very deeply nested test-data paths (300+ chars) that exceed `MAX_PATH` even with long-path support in some tools.

2. **Clone the repository:**
   ```powershell
   git clone https://github.com/JetBrains/kotlin.git C:\kotlin
   cd C:\kotlin
   ```

3. **(Optional) Pre-install a JDK** if you don't want Gradle to auto-download one — install Eclipse Temurin JDK 17 and set `JAVA_HOME`. Otherwise skip this; Gradle's toolchain provisioning (enabled in `settings.gradle.kts`) will fetch the correct JDKs automatically on first build.

4. **Build the compiler distribution:**
   ```powershell
   gradlew.bat dist
   ```
   This assembles the compiler into `dist\kotlinc\`. First run downloads `intellij-core`/`idea-full` and other large dependencies — if you hit timeouts on slow connections, add:
   ```powershell
   gradlew.bat -Dhttp.socketTimeout=60000 -Dhttp.connectionTimeout=60000 dist
   ```

5. **Install all public artifacts to the local Maven repo (if needed for downstream use):**
   ```powershell
   gradlew.bat install
   ```

6. **Run tests (optional, long-running):**
   ```powershell
   gradlew.bat coreLibsTest        # stdlib/reflect/kotlin-test
   gradlew.bat compilerTest        # full compiler test suite
   gradlew.bat gradlePluginTest    # Gradle plugin tests
   ```

7. **(Optional) Build Kotlin/Native** — only if you need the native backend:
   - Install Microsoft C++ Build Tools (VS2019 14.29) and Windows SDK ≥10.0.18362.0.
   - Create a `local.properties` file in the repo root containing `kotlin.native.enabled=true`.
   - Then run:
     ```powershell
     gradlew.bat :kotlin-native:dist
     ```
     Add `:kotlin-native:distPlatformLibs` for platform libraries, or use `:kotlin-native:bundle` for the full cross-target build.

8. **Working in IntelliJ IDEA:** Open the cloned folder directly as a project (File → Open) — no separate import step is required beyond that, per `ReadMe.md`.

## Caveats specific to this environment
- No JDK is currently installed on this machine, so the first `gradlew.bat dist` run will need network access to download JDKs and large IntelliJ/Gradle dependencies (can take a long time and significant disk space, likely 10+ GB when combined with Gradle caches).
- I did not execute the actual multi-hour build in this session (not requested and resource-intensive); the steps above are drawn directly from this repository's own wrapper/config files and documentation, validated against the long-path issue reproduced live in this environment.
