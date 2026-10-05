# Local Tourism Audio Guide - Android APK Client

This folder is an Android WebView client for the Local Tourism Audio Guide hackathon project. It contains a responsive tourism interface, six sample destinations, search, state filtering, favorites using localStorage, multilingual audio placeholders, and Google Maps directions.

## Important
The full hackathon architecture specified in the project documentation uses a React.js frontend + Spring Boot REST API + MySQL backend. This APK is a mobile client/demo package. It is intentionally self-contained so it can demonstrate the core visitor experience without requiring a backend server.

## Build on GitHub
1. Create a GitHub repository.
2. Upload the contents of this folder.
3. Commit to `main`.
4. Open **Actions** in GitHub.
5. Run **Build APK** (or push to main and let it run).
6. Open the completed workflow run and download the artifact named `local-tourism-audio-guide-apk`.

## Build locally
Install Android Studio/SDK and Gradle 8.10+, then run:

    gradle assembleDebug

APK output:

    app/build/outputs/apk/debug/app-debug.apk

## Replace demo audio
The bundled WAV files are short audio placeholders used to prove the playback flow. Replace them with your own royalty-free narration files while keeping the same filenames, or update the URLs in `app/src/main/assets/index.html`.

## Backend integration
For the complete submission, keep the Spring Boot/MySQL backend from the project documentation and connect the production React frontend to `/api/sites` and `/api/sites/{id}/audio`. This APK is the mobile packaging/demo layer.
