# LibVLC for Android

This repository contains the Gradle configuration for building LibVLC as an AAR package.

## Building

You will need JDK 1.7+ installed.

Instructions below are for OS X and Homebrew.

1. Install Android SDK and NDK.

  ```
  $ brew install android-sdk
  $ brew install android-ndk
  ```

2. Set the environment.

  ```
  $ export BREW_HOME="$(brew --prefix)"

  $ export ANDROID_SDK="${BREW_HOME}/opt/android-sdk"
  $ export ANDROID_NDK="${BREW_HOME}/opt/android-ndk"
  $ export ANDROID_ABI="armeabi-v7a"
  ```

3. Build the SDK.

  ```
  $ ./gradlew buildSdk
  $ ./gradlew assembleRelease
  ```

4. Deploy to Maven Local.

  ```
  $ ./gradlew uploadArchives
  ```

  The dependendency is

  ```groovy
  compile "org.videolan:libvlc:1.1.0"
  ```

## Information

* [Android Compile](https://wiki.videolan.org/AndroidCompile) — official documentation.
* [Android Port](https://git.videolan.org/?p=vlc-ports/android.git) — official source code.
