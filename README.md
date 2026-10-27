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
- Google Timeline import, individually estimated roads worldwide, optional Mauritius batch estimation, and manual tracing with ordered, road-snapped waypoints.
- Smooth drive replay with speed, incident badges, custom playback speeds and a final route summary.
- Editable highway and other-road review speed thresholds, with optional speed alerts.
- Weekly/monthly comparisons, frequent route groups and counts, saved places and driving trends.
- Search and filter history, mark passenger journeys, trim drives reversibly and combine consecutive trips with undo.
- Backup previews and optional password encryption, including saved places, groups and reversible edits; verified restore into an empty installation.
- A video storage manager that keeps journeys when deleting recordings.
- Optional compressed rear-camera dashcam, optional microphone audio, synchronized playback and on-demand recap video export.
- Optional Community rankings for weekly/monthly distance, journey count and active days, using a chosen nickname and home country/area.

## Automatic tracking

Complete location/activity permissions in Settings, allow background location and enable detection. On Samsung, use Unrestricted battery and remove the app from sleeping/deep-sleeping lists. Open the app again after an Android Force stop. Detection depends on Android and the activity classifier, and can miss journeys. It cannot distinguish a driver from a passenger. Background camera recording may require opening Live Drive.

## Imported routes

Implausible imports over 100 minutes and at most 4 km of supplied distance are omitted from normal views and statistics; Settings > Journey data > Omitted imports lets you restore legitimate entries. Original data is retained.

Historical Timeline imports have only the supplied locations, dates and distance information. Estimated roads and manual traces are illustrative, not proof of the roads taken; measured speed, incidents and video cannot be recovered from missing data. Individual road estimation works worldwide. From v1.2.0, optional Mauritius bulk estimation uses router.ametheusgroup.com over HTTPS without a PC or debugging connection. The home-hosted service depends on power and internet availability.

No Docker setup or debugging connection is needed on users' phones. Mauritius routing is hosted separately; worldwide individual estimation remains available.

## Privacy and maps

Journeys and dashcam clips are stored locally. Map providers receive tile requests for the viewed area. Requested road estimation sends selected coordinates to the chosen routing service: router.ametheusgroup.com for hosted Mauritius requests, FOSSGIS/OSRM for worldwide requests. Hosted Mauritius requests pass through Cloudflare to the home server. Road-class checks use Overpass. GitHub receives ordinary release checks and downloads, without journey records. Maps and routing need internet; recording and stored history work offline. Map and third-party credits remain visible in the app.

Community sharing is optional. Read the privacy notice and explicitly agree before activation. After agreement, Supabase stores an anonymous authentication identity, nickname, manually selected country/area, and daily distance/journey totals used for public weekly/monthly rankings. Community does not upload routes, coordinates, speeds, incidents, videos or saved places. Only eligible recorded driver journeys qualify; imports and passenger journeys are excluded. Stop sharing removes the public profile/scores, with an explicit pending state if offline. The anonymous identity is installation-specific: stop sharing before uninstalling or clearing app data. Scores and areas are self-reported; they are not independently verified.

Please report bugs using Issues without posting private Timeline exports, location histories or camera footage. See each release's notes for known limitations.
