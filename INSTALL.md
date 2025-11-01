# GeoSnap-Industridykk v2 - Installation Guide

## Table of Contents
- [Overview](#overview)
- [System Requirements](#system-requirements)
- [Installation for Developers](#installation-for-developers)
- [Installation for End Users](#installation-for-end-users)
- [Troubleshooting](#troubleshooting)

## Overview

GeoSnap-Industridykk v2 is an application that allows you to take photos with automatically embedded text showing:
- Street/road/bridge names
- Compass direction
- GPS coordinates
- Geographic position

## System Requirements

### For Android
- Android 8.0 (API level 26) or newer
- Minimum 2 GB RAM
- Camera access
- GPS/Location access
- Internet access (for map data)

### For iOS
- iOS 12.0 or newer
- Minimum 2 GB RAM
- Camera access
- Location access
- Internet access (for map data)

## Installation for Developers

### Prerequisites

#### For Android Development
```bash
# Install Node.js (version 16 or newer)
# Download from https://nodejs.org/

# Install Android Studio
# Download from https://developer.android.com/studio

# Install Java Development Kit (JDK) 11 or newer
```

#### For iOS Development (macOS only)
```bash
# Install Xcode from App Store
# Install CocoaPods
sudo gem install cocoapods
```

### Development Environment Setup

1. **Clone the repository**
```bash
git clone https://github.com/lillekim88/GeoSnap-Industridykkv2.git
cd GeoSnap-Industridykkv2
```

2. **Install dependencies**
```bash
npm install
# or
yarn install
```

3. **Configure environment variables**

Create a `.env` file in the root directory:
```
# Replace with your actual API keys
MAPS_API_KEY=your_google_maps_api_key_here
LOCATION_SERVICE_URL=https://api.example.com/location
```

4. **Run the application**

For Android:
```bash
npm run android
# or
yarn android
```

For iOS:
```bash
cd ios && pod install && cd ..
npm run ios
# or
yarn ios
```

### Build for Production

#### Android APK/AAB
```bash
cd android
./gradlew assembleRelease
# APK located at: android/app/build/outputs/apk/release/

# For Android App Bundle (AAB):
./gradlew bundleRelease
# AAB located at: android/app/build/outputs/bundle/release/
```

#### iOS IPA
```bash
# Open Xcode
open ios/GeoSnap.xcworkspace

# Select Product > Archive
# Follow the export wizard to generate IPA file
```

## Installation for End Users

### Android

#### Method 1: Google Play Store (when available)
1. Open Google Play Store
2. Search for "GeoSnap Industridykk"
3. Tap "Install"
4. Accept required permissions

#### Method 2: APK File
1. Download the APK file from [Releases](https://github.com/lillekim88/GeoSnap-Industridykkv2/releases)
2. Enable "Unknown sources" in Android settings:
   - Go to Settings > Security
   - Enable "Unknown sources" or "Install unknown apps"
3. Open the downloaded APK file
4. Follow the installation wizard
5. Accept required permissions

### iOS

#### Method 1: App Store (when available)
1. Open App Store
2. Search for "GeoSnap Industridykk"
3. Tap "Download"
4. Accept required permissions

#### Method 2: TestFlight (for beta testing)
1. Install TestFlight from App Store
2. Open the invitation link you received
3. Accept the invitation
4. Download the app from TestFlight

### Required Permissions

The application requires the following permissions:
- **Camera**: To take photos
- **Location/GPS**: To fetch GPS coordinates and place names
- **Storage**: To save photos
- **Internet**: To fetch map data and place names

## First Time Setup

1. Open the GeoSnap app
2. Accept permissions when prompted
3. Calibrate the compass by moving the phone in a figure-eight motion
4. The app is ready to use!

## Using the Application

1. **Take a photo**:
   - Open the app
   - Point the camera at the desired object
   - GPS coordinates, direction, and place name are displayed automatically
   - Press the shutter button

2. **Saved photos**:
   - Photos are automatically saved to the device's photo gallery
   - Photos contain embedded text with location information

## Troubleshooting

### GPS data not showing
- Check that location permissions are enabled
- Verify that GPS is enabled on the device
- Try going to an open area for better GPS signal

### Compass shows wrong direction
- Calibrate the compass by moving the phone in a figure-eight motion
- Keep the device away from magnetic objects

### Place names not showing
- Check internet connection
- Verify that the app has permission to use internet

### App crashes on startup
- Uninstall and reinstall the app
- Check that the device meets system requirements
- Clear cache and data (Android: Settings > Apps > GeoSnap > Storage)

### Camera not working
- Check that camera permission is granted
- Restart the device
- Verify that no other apps are using the camera

## Updates

### Android
- Automatic updates via Google Play Store (if installed from there)
- Manual update: download new APK and install

### iOS
- Automatic updates via App Store (if installed from there)
- Manual update: download new version from App Store

## Support

For questions or issues:
- Create an issue on [GitHub](https://github.com/lillekim88/GeoSnap-Industridykkv2/issues)
- See [README.md](README.md) for more information

## License

See [LICENSE](LICENSE) file for license details.

## Contributing

We appreciate contributions! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

---

Made with ❤️ for industrial divers and field workers
