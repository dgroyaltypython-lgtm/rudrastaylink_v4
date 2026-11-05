# Changelog — Rudra StayLink Android

## 1.0.4
- Downgraded Coil Android Compose/network artifacts from 3.6.3 to 3.4.0. Coil 3.6.x was built against Kotlin 2.4.10, Compose 1.12.0 and compileSdk 37, which mismatched the app's AGP 8.13.2 / Kotlin 2.3.21 / SDK 36 stack.
- Changed Compose BOM use to `enforcedPlatform(2026.06.01)` so transitive dependencies cannot promote AndroidX Compose runtime/UI/foundation to 1.12.x.
- Replaced the two-workflow debug/release YAML with one Codemagic-only debug APK workflow. It finds the project root, configures the Android SDK, logs Compose/Coil dependency resolution, builds the debug APK in Codemagic, and publishes a clearly named artifact.
- Removed local Windows build helper files to make the intended Codemagic-only workflow clear.
- Bumped versionCode to 4 and versionName to 1.0.4.

## 1.0.3
- Pinned Compose BOM to 2026.06.01 (Compose 1.11.4).

## 1.0.2
- Migrated Kotlin compiler configuration to the `compilerOptions` DSL.

## 1.0.1
- Improved Codemagic project directory detection and build diagnostics.

## 1.0.0
- Initial Android owner app connected to the Django REST API.
