# WiFi Security Audit PoC

Android application for automated Wi-Fi security auditing and connectivity testing.

## Features

- **Wi-Fi Scanner**: Detects nearby access points including hidden SSIDs
- **Pattern Matching**:
  - **Type A**: Networks starting with `ADSL_INWI` or named `Wifi_Perso`
    - Password: BSSID without colons in uppercase (e.g., `AABBCC112233`)
  - **Type B**: Hidden networks matching `SSID_[2-5]`
    - Password: Hardcoded constant `CONST_PASS`
- **Auto-Connect**: Uses WifiNetworkSpecifier (Android 10+) for automatic connection attempts
- **Modern UI**: Built with Jetpack Compose and Material 3

## Requirements

- Android 10 (API 29) or higher
- Location permission (required for Wi-Fi scanning)
- Wi-Fi and network state permissions

## Project Structure

```
app/src/main/java/com/wifiaudit/poc/
├── MainActivity.kt           # Entry point
├── WiFiScanner.kt           # Core scanning and connection logic
├── WiFiScannerScreen.kt     # Compose UI
└── ui/theme/Theme.kt        # Material theme
```

## Key Components

### WiFiScanner.kt
- Scans and analyzes networks
- Generates passwords based on vulnerability patterns
- Handles network connection via WifiNetworkSpecifier

### WiFiScannerScreen.kt
- Permission handling with Accompanist
- LazyColumn displaying networks
- Vulnerable networks highlighted with red indicators
- Connect/Test buttons for vulnerable networks

## Security Note

This is a Proof of Concept for educational and authorized security testing only. Use responsibly and only on networks you own or have explicit permission to test.

## Build Instructions

1. Open project in Android Studio
2. Sync Gradle dependencies
3. Run on device or emulator (Android 10+)
4. Grant location and Wi-Fi permissions when prompted
5. Tap "Scan" to detect networks

## License

Educational use only.
