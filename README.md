# OGxISAI Mic — Android

Android WebView packaging of the OGxISAI microphone UI/audio-processing JavaScript.

## Build

Open this folder in Android Studio and run the `app` configuration. Or use Gradle:

    ./gradlew assembleDebug

The APK will be in `app/build/outputs/apk/debug/`.

## Important limitation

Android does not let an ordinary app replace the microphone input of Discord/WhatsApp/etc. with a processed microphone stream. This build can capture the microphone and run the Web Audio processing chain inside the app, but system-wide virtual microphone routing requires a separate native audio-routing solution and may not be supported for third-party apps on all Android versions/devices.
