# Marathi2English AI — Android starter project

## What it does
- Uses Android's speech recognition service with Marathi (mr-IN) as the requested language.
- Lets the user speak and converts recognized speech into Marathi text.
- Sends that text to the MyMemory translation endpoint for Marathi-to-English translation.
- Provides a copy button for the translated English.
- Includes a 2-minute stop timer.

## Important limitations
- This is a starter Android Studio source project, not a signed APK.
- Speech recognition behavior depends on the speech service installed on the phone. Some services may stop after a pause or return only one segment, so a 1–2 minute recording is not guaranteed to be transcribed as one continuous passage on every device.
- Translation uses a public third-party endpoint. Availability, rate limits, language-pair quality, and privacy terms can change. Do not send confidential content.
- The MyMemory endpoint may not reliably support Marathi (`mr`) in all cases. If it fails, replace the translation request with a supported translation provider/API.
- Naturalness and grammar quality may vary. A dedicated AI translation API can improve results, but needs a backend and API credentials. Do not hardcode private API keys in a public Android app.

## Build in Android Studio
1. Download and unzip this folder.
2. Install Android Studio and a JDK 17 (Android Studio usually provides one).
3. Open the `Marathi2EnglishAI` folder in Android Studio.
4. Allow Gradle sync to complete; install Android SDK Platform 35 if prompted.
5. Connect an Android phone with Developer Options > USB debugging enabled, or use an emulator.
6. Press Run. On first use, allow microphone permission.
7. Make sure the phone has a speech recognition service and internet access.

## Demo sentence
Marathi: मला विद्यार्थ्यांना इंग्रजी व्याकरण शिकवायचे आहे.
Expected natural English: I want to teach English grammar to students.
