# How to get your installable APK — Diabetes Care Tracker (Gigal Prayer House)

The app code is ready. Building it into an `.apk` needs Google's Android
build servers, which this assistant's sandbox cannot reach. The easiest way
to get a real `.apk` WITHOUT installing anything on your computer is to let
GitHub build it for you, free. It takes about 10 minutes the first time.

====================================================================
METHOD 1 (RECOMMENDED) — Free cloud build with GitHub Actions
====================================================================
You only need a free GitHub account. No coding, no Android Studio.

1. Create a free account at https://github.com  (skip if you have one).

2. Create a new repository:
   - Click the "+" (top right) → "New repository".
   - Name it: diabetes-care-tracker
   - Set it to Private (or Public, your choice) → "Create repository".

3. Upload this project:
   - On the new repo page click "uploading an existing file".
   - Unzip the project on your computer first, then drag in ALL of its
     contents (the package.json, capacitor.config.json, the www, android,
     and .github folders). 
   - IMPORTANT: make sure the hidden ".github" folder is included — it
     contains the build instructions GitHub needs.
   - Click "Commit changes".

4. GitHub builds the APK automatically:
   - Go to the "Actions" tab of your repo.
   - You'll see a run called "Build Android APK" (it starts on its own).
     If it doesn't, click it → "Run workflow".
   - Wait ~5-8 minutes until it shows a green check.

5. Download your APK:
   - Click the finished run → scroll to "Artifacts" at the bottom.
   - Download "DiabetesCareTracker-APK". Unzip it → app-debug.apk

6. Install on your Android phone:
   - Send app-debug.apk to the phone (email / WhatsApp / USB / Drive).
   - Tap it. Allow "Install from unknown sources" when asked. Done.

====================================================================
METHOD 2 — Build locally in Android Studio
====================================================================
1. Install Android Studio (free) AND Node.js (https://nodejs.org).
2. Unzip this project. Open a terminal in the project folder and run:
       npm install
       npx cap sync android
3. In Android Studio: Open → select the "android" folder → let it sync.
4. Build → Build Bundle(s)/APK(s) → Build APK(s).
   Result: android/app/build/outputs/apk/debug/app-debug.apk

====================================================================
App details
====================================================================
- App name : Diabetes Care Tracker
- Package  : com.gigalprayerhouse.diabetescare
- Version  : 1.0
- Founder  : Hepsiba (MCA)

Notes:
- The debug APK installs fine for personal use. For the Google Play Store you
  must make a SIGNED release build (Android Studio: Build → Generate Signed
  Bundle/APK).
- The app loads Bootstrap & Chart.js from the internet, so the first launch
  needs a connection. Ask if you want a fully offline version.
