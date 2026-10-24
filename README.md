# Journey Tracker for Android

Personal journey tracking, route history and drive replay, with optional dashcam recording.

**[Download the latest APK](https://github.com/chaitanyak1708/Mobile-Car-Releases/releases/latest/download/JourneyTracker.apk)** · **[Releases and notes](https://github.com/chaitanyak1708/Mobile-Car-Releases/releases)**

This public repository contains signed installation files and documentation. The application source is maintained privately. No source license is granted by this repository; third-party components retain their respective licenses and map attribution.

## Install

Requires Android 8.0 or later. Google Play services are needed for location and automatic detection. Download JourneyTracker.apk, open it and allow installation from your browser/file manager if Android asks.

Public release installations check for new releases about once daily. You can also use **Settings > App updates**. Select Download, then confirm installation with Android. Updating with the same signing certificate preserves the app's journeys and settings. Development builds use a different signing certificate and need a separate data migration before switching; do not uninstall a development build containing journeys you want to keep.

SHA256SUMS.txt and release-metadata.json accompany every release. The app verifies the APK checksum, package, version and signing certificate before installation. APKs install directly; this is not a Play Store listing.

## Features

- Manual and automatic tracking; personal statistics with date filters and interactive leaderboards linking to journeys.
- Interactive route history, journey search, dark/light/terrain maps and optional start/end markers.
- Google Timeline import, individually estimated roads worldwide, optional Mauritius batch estimation, and manual route tracing.
- Smooth drive replay with speed, incident badges, custom playback speeds and a final route summary.
- Editable highway and other-road review speed thresholds, with optional speed alerts.
- Portable backups of journeys, saved routes, review events, videos and settings; verified restore into an empty installation.
- Optional compressed rear-camera dashcam, optional microphone audio, synchronized playback and on-demand recap video export.

## Automatic tracking

Complete location/activity permissions in Settings, allow background location and enable detection. On Samsung, use Unrestricted battery and remove the app from sleeping/deep-sleeping lists. Open the app again after an Android Force stop. Detection depends on Android and the activity classifier, and can miss journeys. It cannot distinguish a driver from a passenger. Background camera recording may require opening Live Drive.

## Imported routes

Historical Timeline imports have only the supplied locations, dates and distance information. Estimated roads and manual traces are illustrative, not proof of the roads taken; measured speed, incidents and video cannot be recovered from missing data. Individual road estimation works worldwide. Optional bulk estimation is restricted to Mauritius and requires your own PC router.

For bulk estimation, install Docker Desktop with its Linux engine and Android platform-tools. Connect the phone with USB or paired wireless debugging, then run the attached **setup-mauritius-router.ps1** using PowerShell. The script downloads Mauritius OpenStreetMap data, builds a local OSRM graph, binds the router to localhost, and forwards the connected phone through ADB. Keep the PC, router and ADB connection running while the batch runs. This is optional and unnecessary for recording drives or individual worldwide requests.

## Privacy and maps

Journeys and dashcam clips are stored locally. Map providers receive tile requests for the viewed area. Explicit individual road estimation sends selected coordinates to FOSSGIS/OSRM; road-class checks use Overpass. GitHub receives ordinary release checks and downloads, without journey records. Maps and routing need internet; recording and stored history work offline. Map and third-party credits remain visible in the app.

Please report bugs using Issues without posting private Timeline exports, location histories or camera footage. See each release's notes for known limitations.
