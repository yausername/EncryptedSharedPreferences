# EncryptedSharedPreferences

This is [androidx EncryptedSharedPreferences](https://developer.android.com/reference/androidx/security/crypto/EncryptedSharedPreferences) but with `minSdkVersion 19`.

[![](https://jitpack.io/v/yausername/EncryptedSharedPreferences.svg)](https://jitpack.io/#yausername/EncryptedSharedPreferences)


* Code is taken from https://android.googlesource.com/platform/frameworks/support/+/refs/heads/androidx-master-dev/security/crypto/ .
* Support for `sdkLevel < 23` was added from https://android-review.googlesource.com/c/platform/frameworks/support/+/1182622/2 (for `sdkLevel < 23` android keystore is not used, keysets are stored in plaintext in sharedprefs)
* This library should be replaced by `androidx.security:security-crypto` if/when support for `sdkLevel < 23` is available.

## Installation

### Gradle
Step 1 : Add jitpack repository to your project build file
```gradle
allprojects {
    repositories {
        maven { url 'https://jitpack.io' }
    }
}
```
Step 2: Add the dependency
```gradle
dependencies {
    implementation 'com.github.yausername:EncryptedSharedPreferences:master-SNAPSHOT'
}
