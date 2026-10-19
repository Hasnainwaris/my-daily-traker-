# EduRoutine (web + Android)

## Get the APK (no Android Studio needed)
1. Create a free GitHub repository and upload everything in this folder (keep the `.github` folder).
2. Open the repo's **Actions** tab, run **Build APK**, wait about 5 minutes.
3. Download **EduRoutine-apk** from the finished run, unzip, and install `app-debug.apk` on your phone (allow "install unknown apps").
4. On first launch, allow notifications. If Android asks for "Alarms & reminders", allow it, or alarms may arrive late.

Alarm sounds (chime, bell, triple beep, rising siren) are real Android notification sounds, so they ring with the app closed. "Voice announcement" falls back to the chime on Android, and "Vibration" uses a silent sound with vibration. Phones in Do Not Disturb or with battery saver may mute or delay them.

## Web app with its own URL (installable)
Upload the `www` folder to Netlify Drop (app.netlify.com/drop) or GitHub Pages. You get an https URL; open it in Chrome and choose Install app. Browser alarms only ring while the page is open.

## Local build
`npm install && npx cap add android`, copy `resources/raw/*.wav` into `android/app/src/main/res/raw/`, add the permissions from the workflow to AndroidManifest.xml, then `npx cap sync android` and open in Android Studio.
