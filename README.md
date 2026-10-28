# Veloce Patches

Standalone Morphe patch-bundle project for apps used with Veloce.

## Build

Use JDK 21 or newer and an Android SDK. Morphe's Gradle plugin requires GitHub
Packages access even for public artifacts. Configure `gpr.user` and `gpr.key`
(a token with `read:packages`) in your **user** `~/.gradle/gradle.properties`, or
set `GITHUB_ACTOR` and `GITHUB_TOKEN` in your environment.

From this directory:

```sh
./gradlew buildAndroid
```

From the Veloce root, the equivalent is `./gradlew -p morphe-patches buildAndroid`.
Bundle: `patches/build/libs/patches-0.1.0.mpp`. The Android build adds DEX for
Morphe Manager; the same bundle also contains JVM classes for Morphe Desktop.