# LibVLC for Android

This repository contains the Gradle configuration for building LibVLC as an AAR package.

## Building

You will need JDK 1.6, Gradle 1.12 and Ant installed.

Instructions below are for OS X and Homebrew.

1. Install Android SDK and NDK.

  ```
  $ brew install android-sdk
  $ brew install android-ndk
  ```

2. Set environment.

  ```
  $ export ANDROID_HOME="/usr/local/opt/android-sdk"

  $ export ANDROID_SDK="/usr/local/opt/android-sdk"
  $ export ANDROID_NDK="/usr/local/opt/android-ndk"
  $ export ANDROID_ABI="armeabi-v7a"
  ```

3. Build the SDK.

  ```
  $ gradle buildSdk
  $ gradle assembleRelease
  ```

4. Deploy to Maven Local.

  ```
  $ gradle uploadArchives
  ```

  The dependendency is
  
  ```groovy
  compile "org.videolan:libvlc:0.9.+"
  ```

## Information

* [Android Compile](https://wiki.videolan.org/AndroidCompile) — official documentation.
