# Kerala Bus Finder
Android (Kotlin/Compose) + responsive web app sharing one Firebase backend.

## Status: Stage 1
- web-app: homepage, demo direct-bus search, swap, recent/popular routes, About page.
- android-app: Compose home screen with demo search.
- All schedules are labelled DEMO. No real timetable data or live GPS is shown.

## Run the web app
`cd web-app && python3 -m http.server 8080`, then open http://localhost:8080 (ES modules need http, not file://).

## Next
Stage 2 Firebase, Stage 3 Maps and Places (keys in git-ignored `web-app/js/config.js`), Stage 4 real search.

## Build the APK with GitHub (no Android Studio needed)
1. Create a GitHub repo and push this project to the `main` branch.
2. Open the repo's **Actions** tab, choose **Build Android APK**, click **Run workflow** (it also runs on every push).
3. When it turns green, open the run and download **kerala-bus-finder-apk** under Artifacts.
4. Unzip, copy `app-debug.apk` to your phone and install it (allow "install unknown apps").
The APK wraps `web-app/` using Capacitor. It is a debug build for testing; a signed release build for the Play Store comes later.
