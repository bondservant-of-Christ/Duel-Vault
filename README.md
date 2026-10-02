# Duel Vault – build the APK for free (no Android Studio)

1. Make a free account at github.com and create a new **public** repository (any name).
2. Upload everything in this folder to it (drag and drop in the web UI works; make sure the
   hidden `.github` folder goes up too).
3. Open the repo's **Actions** tab. If asked, enable workflows. Pick **Build APK** → **Run workflow**.
4. After ~5 minutes, click the finished run and download **duel-vault-apk** (a zip containing app-debug.apk).
5. Unzip it on your phone, open the .apk, and allow "install unknown apps" when Android asks.
   On first scan, allow Camera.

The app needs internet: it loads the text-reading engine on first scan and looks up cards on YGOPRODeck.

## Building locally instead
Needs Node 20, JDK 17, Android Studio. Run: npm install, npx cap add android, add
`<uses-permission android:name="android.permission.CAMERA" />` to android/app/src/main/AndroidManifest.xml,
then npx cap sync android and npx cap open android.

## Editing the app
All the app code is in www/index.html.
