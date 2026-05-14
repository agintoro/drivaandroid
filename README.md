# DRIVA Processing Log Android APK Project

This is an offline Android WebView wrapper for the DRIVA Processing Log static app.

## What this is

- Android APK project
- Offline-first
- Loads the app from `android_asset/index.html`
- Uses Android WebView local storage
- No internet required after installation
- Good for field logging on Android devices

## Important warning

This is a single-device local-storage app. If the app is uninstalled or app data is cleared, local records can disappear. Export CSV regularly.

## Build the APK using GitHub Actions

1. Create a new GitHub repository.
2. Upload all files from this folder.
3. Go to the repository's **Actions** tab.
4. Open **Build Android APK**.
5. Click **Run workflow**.
6. After it finishes, download the artifact named `driva-processing-log-debug-apk`.
7. Inside it, you will find `app-debug.apk`.
8. Install it on Android.

## Build locally using Android Studio

1. Open this folder in Android Studio.
2. Let Gradle sync.
3. Choose **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
4. Find the APK at:

`app/build/outputs/apk/debug/app-debug.apk`

## Production note

The debug APK is fine for internal testing. For formal distribution, generate a signed release APK or AAB.
