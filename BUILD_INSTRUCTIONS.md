# Build Instructions for WiFi Audit PoC

## Prerequisites

To build this Android application, you need:

1. **Android Studio** (recommended) or Android SDK
2. **JDK 17** or higher
3. **Gradle** (included via wrapper)

## Method 1: Build with Android Studio (Easiest)

1. **Install Android Studio**
   - Download from: https://developer.android.com/studio
   - Install with default settings (includes Android SDK)

2. **Open Project**
   - Launch Android Studio
   - Click "Open" and select this project folder
   - Wait for Gradle sync to complete

3. **Build APK**
   - Click **Build → Build Bundle(s) / APK(s) → Build APK(s)**
   - Or use menu: **Build → Generate Signed Bundle / APK**
   - APK location: `app/build/outputs/apk/debug/app-debug.apk`

4. **Install on Device**
   - Enable USB debugging on your Android device
   - Connect device via USB
   - Click the "Run" button (green play icon) in Android Studio

## Method 2: Build via Command Line

### Windows:
```cmd
gradlew.bat assembleDebug
```

### Linux/Mac:
```bash
chmod +x gradlew
./gradlew assembleDebug
```

The APK will be generated at:
```
app/build/outputs/apk/debug/app-debug.apk
```

## Method 3: GitHub Actions (Cloud Build)

If you push this project to GitHub:

1. Push code to GitHub repository
2. Go to **Actions** tab
3. Click **Build Android APK** workflow
4. Click **Run workflow**
5. Download the APK from the **Artifacts** section

## Installing the APK

### On Physical Device:
1. Transfer `app-debug.apk` to your device
2. Enable "Install from Unknown Sources" in Settings
3. Tap the APK file to install

### Via ADB:
```bash
adb install app/build/outputs/apk/debug/app-debug.apk
```

## Troubleshooting

### "Android SDK not found"
- Install Android Studio or set `ANDROID_HOME` environment variable
- Create `local.properties` file with:
  ```
  sdk.dir=C:/Users/YourUsername/AppData/Local/Android/Sdk
  ```

### "Java version mismatch"
- Ensure JDK 17 is installed
- Set `JAVA_HOME` environment variable

### "Gradle sync failed"
- Check internet connection (Gradle downloads dependencies)
- Try: File → Invalidate Caches / Restart in Android Studio

## Build Variants

- **Debug**: `gradlew assembleDebug` (for testing)
- **Release**: `gradlew assembleRelease` (requires signing key)

## Minimum Requirements

- **Build Machine**: Windows/Mac/Linux with 8GB RAM
- **Target Device**: Android 10 (API 29) or higher
- **Disk Space**: ~5GB for Android SDK + dependencies

## Quick Start (No Android Studio)

If you just want to test the app without building:

1. Download a pre-built APK from GitHub Actions artifacts
2. Or use an online build service like:
   - GitHub Actions (free, automated)
   - Bitrise (free tier available)
   - CircleCI (free tier available)

## Security Note

This is a debug build for testing only. For production:
- Use release build variant
- Sign with your keystore
- Enable ProGuard/R8 obfuscation
