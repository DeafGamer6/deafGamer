# Swiper No Swiping v1.2.1 (Android)

Everything runs on the phone. The app has no internet permission and nothing is uploaded anywhere.
Photos, bios, prompts and notes are stored in the app's own storage on the device.

## Get the APK (about 5 minutes, free)
1. Make a free GitHub account and create a new **private** repository.
2. Upload everything in this folder to it (drag the files into the repo page).
   Keep the hidden `.github` folder. If your browser hides it, use GitHub Desktop or `git push`.
3. Open the repo's **Actions** tab. The "Build APK" run starts by itself. Wait for the green tick.
4. Open the finished run, scroll to **Artifacts**, download `swipe-v1-apk`, unzip it.
5. Send `app-debug.apk` to your phone and tap it. Allow "install unknown apps" when asked.

## Updating later
Change `www/index.html`, push it, download the new APK and install it over the old one.
Your photos and notes are kept, because every build uses the same signing key.
Raise `versionCode` in `android/app/build.gradle` for each release.

## What's new in 1.2.1
- Code cleanup only. No new features. See the notes below.

## What's new in 1.2
- Profile page has a joke Report button and a Block button that fails in a cute way.

## What's new in 1.1
- Android back button goes back a screen. On the main screen, press it twice to exit.
- Manage photos: remove single photos from the setup screen.
- Heart app icon and the name "Swiper No Swiping".
- Photos are reshuffled every time you tap Start swiping.

## Notes
- Uninstalling the app deletes all its data. In the app, "Show my data as text" backs up bios, prompts and notes. Photos are not included.
- Android backup is switched off on purpose, so nothing goes to Google's cloud. It also means data does not follow you to a new phone.
- The signing key in this repo is for personal sideloading only. Do not publish this app to the Play Store with it.
- If the app opens blank, add `<uses-permission android:name="android.permission.INTERNET" />` back in `android/app/src/main/AndroidManifest.xml`.
