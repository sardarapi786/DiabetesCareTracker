# Diabetes Care Tracker — Android App (Gigal Prayer House)

This folder is a complete, standalone Android Studio project that wraps the
Diabetes Care Tracker web app. The full app is already bundled inside
(`app/src/main/assets/public/index.html`) — no internet/hosting needed to build.

- App name: Diabetes Care Tracker
- Package: com.gigalprayerhouse.diabetescare
- Version: 1.0 (versionCode 1)

------------------------------------------------------------
## Option A — Build the APK in Android Studio (easiest)
------------------------------------------------------------
1. Install Android Studio (free): https://developer.android.com/studio
2. Open Android Studio → "Open" → select THIS folder (the one with this file).
3. Wait for "Gradle sync" to finish (it auto-downloads what it needs the first time).
4. Menu: Build → Build Bundle(s) / APK(s) → Build APK(s).
5. When done, click "locate" in the popup. The file is at:
      app/build/outputs/apk/debug/app-debug.apk
6. Copy app-debug.apk to your Android phone and tap it to install.
   (Enable "Install unknown apps" for your file manager / browser when prompted.)

------------------------------------------------------------
## Option B — Build from the command line
------------------------------------------------------------
Requires the Android SDK + JDK 17 installed, and ANDROID_HOME set.

   # Windows
   gradlew.bat assembleDebug
   # Mac/Linux
   ./gradlew assembleDebug

Output: app/build/outputs/apk/debug/app-debug.apk

------------------------------------------------------------
## Installing on the phone
------------------------------------------------------------
- Transfer the .apk via USB, email, or cloud drive.
- On the phone, open the .apk and allow installation from this source.
- The debug APK is fine for personal/testing use. For Google Play you must
  generate a SIGNED release APK/AAB (Build → Generate Signed Bundle / APK).

------------------------------------------------------------
## Notes
------------------------------------------------------------
- The app uses Bootstrap & Chart.js from a CDN, so the FIRST launch needs
  internet. To make it 100% offline, those two libraries can be downloaded
  into the app and the index.html links pointed to local copies — ask and
  this can be done.
- To change the app icon: in Android Studio right-click `app/res` →
  New → Image Asset, and replace the launcher icon.
- Founder: Hepsiba (MCA).
