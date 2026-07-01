# Flutter WebView App Builder 📱🌐

A simple, fast, and customizable Flutter template to easily convert any responsive website into a native Android and iOS mobile application using the `webview_flutter` widget.

## 🚀 Features

- **Cross-Platform Compatibility:** Builds natively for both Android and iOS from a single codebase.
- **Easy Configuration:** Just replace the target URL and App Title to get your web app running on mobile.
- **SafeArea Support:** Keeps your web content neatly constrained within device screen boundaries (avoids notches and system UI overlapping).
- **JavaScript Enabled:** Fully supports rich JavaScript web experiences, web applications, and frameworks.

## 🛠 Prerequisites

To run this project, make sure you have the following installed on your machine:
- [Flutter SDK](https://flutter.dev/docs/get-started/install) (latest stable version)
- **Android Studio** (for Android development)
- **Xcode** (for iOS development, requires a Mac)
- An emulator/simulator or physical device connected

## 💻 How to Use

1. **Clone the repository:**
   ```bash
   git clone https://github.com/alokydv9045/App-builder.git
   cd App-builder
   ```

2. **Install dependencies:**
   Fetch the necessary Flutter packages:
   ```bash
   flutter pub get
   ```

3. **Configure your Website URL & App Title:**
   Navigate to `lib/src/app.dart`. 
   
   Locate the `WebViewContainer` and change the arguments:
   ```dart
   class App extends StatelessWidget {
     @override
     Widget build(BuildContext context) {
       return MaterialApp(
         // Change the URL to your website's URL & the Title to your App's Title
         home: WebViewContainer('https://yourwebsite.com', 'Your App Name'),
       );
     }
   }
   ```

4. **Run the App:**
   ```bash
   flutter run
   ```

## 🎨 Customizing your App

### 1. App Name
- **Android:** Edit `android/app/src/main/AndroidManifest.xml` and change the `android:label` value.
- **iOS:** Edit `ios/Runner/Info.plist` and modify the value of `<key>CFBundleName</key>` and `<key>CFBundleDisplayName</key>`.

### 2. App Icon
To update the app icon, simply replace the image in `lib/assets/icon/icon.png` with your own 512x512 logo. Then, use the `flutter_launcher_icons` package to generate the native icons:
```bash
flutter pub run flutter_launcher_icons:main
```

## 📦 Building for Production

When you are ready to publish your app to the Play Store or App Store, run the following commands to generate the release builds:

**For Android (App Bundle):**
```bash
flutter build appbundle
```

**For iOS:**
```bash
flutter build ipa
```

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
