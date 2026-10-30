# Journey Tracker for Android

Personal journey tracking, route history and drive replay, with optional dashcam recording.

**[Download the latest APK](https://github.com/chaitanyak1708/Mobile-Car-Releases/releases/latest/download/JourneyTracker.apk)** · **[Releases and notes](https://github.com/chaitanyak1708/Mobile-Car-Releases/releases)**

This public repository contains signed installation files and documentation. The application source is maintained privately. No source license is granted by this repository; third-party components retain their respective licenses and map attribution.

## Install

Requires Android 8.0 or later. Google Play services are needed for location and automatic detection. Download JourneyTracker.apk, open it and allow installation from your browser/file manager if Android asks.

From v1.5.0, public installations prompt when you enter the app if an update is available, with **Download**, **Later** and **Install** actions. Prompts wait during live journeys, and recent checks are reused for 15 minutes. Daily background checks and **Settings > App updates** remain available. Downloads start only when you choose; Android confirms installation. Older versions can use Settings > App updates for this first upgrade. Updating with the same signing certificate preserves the app's journeys and settings. Development builds use a different signing certificate and need a separate data migration before switching; do not uninstall a development build containing journeys you want to keep.

SHA256SUMS.txt and release-metadata.json accompany every release. The app verifies the APK checksum, package, version and signing certificate before installation. APKs install directly; this is not a Play Store listing.

## Features

- Manual and automatic tracking; personal statistics with date filters and interactive leaderboards linking to journeys.
- Interactive route history, journey search, dark/light/terrain maps and optional start/end markers.
- Google Timeline import, individually estimated roads worldwide, optional Mauritius batch estimation, and manual tracing with ordered, road-snapped waypoints.
- Smooth drive replay with speed, incident badges, custom playback speeds and a final route summary.
- Editable highway and other-road review speed thresholds, with optional speed alerts.
- Weekly/monthly comparisons, frequent route groups and counts, saved places and driving trends.
- Search and filter history, mark passenger journeys, trim drives reversibly and combine consecutive trips with undo.
- Separate Export progress / Restore progress actions, optional recordings and password encryption enabled by default. Use compatible cloud providers in Android's file picker or save/upload/download the archive yourself. Restore previews and verifies data into an empty library, including saved places, groups and reversible edits.
- A video storage manager that keeps journeys when deleting recordings.
- Optional compressed rear-camera dashcam, optional microphone audio, synchronized playback and on-demand recap video export.
- Compact date selectors across Dashboard, Journeys and Routes; contextual tracking health and interrupted-recording recovery.
- Swipeable Personal and Community dashboard tabs with shared date controls, pinned own rank and sync status. Choose private friend/family groups, public rankings, both, or no sharing. Select which KPIs to share; top speed defaults off for new profiles.
- Invite-only groups with owner controls, member removal, invite reset and a private, single-use Community recovery code for reinstalling.

## Automatic tracking

Complete location/activity permissions in Settings, allow background location and enable detection. On Samsung, use Unrestricted battery and remove the app from sleeping/deep-sleeping lists. Open the app again after an Android Force stop. Detection depends on Android and the activity classifier, and can miss journeys. It cannot distinguish a driver from a passenger. Background camera recording may require opening Live Drive.

## Imported routes

Implausible imports over 100 minutes and at most 4 km of supplied distance are omitted from normal views and statistics; Settings > Journey data > Omitted imports lets you restore legitimate entries. Original data is retained.

Historical Timeline imports have only the supplied locations, dates and distance information. Estimated roads and manual traces are illustrative, not proof of the roads taken; measured speed, incidents and video cannot be recovered from missing data. Individual road estimation works worldwide. From v1.2.0, optional Mauritius bulk estimation uses router.ametheusgroup.com over HTTPS without a PC or debugging connection. The home-hosted service depends on power and internet availability.

No Docker setup or debugging connection is needed on users' phones. Mauritius routing is hosted separately; worldwide individual estimation remains available.

## Privacy and maps

Journeys and dashcam clips are stored locally. Map providers receive tile requests for the viewed area. Requested road estimation sends selected coordinates to the chosen routing service: router.ametheusgroup.com for hosted Mauritius requests, FOSSGIS/OSRM for worldwide requests. Hosted Mauritius requests pass through Cloudflare to the home server. Road-class checks use Overpass. GitHub receives ordinary release checks and downloads, without journey records. Maps and routing need internet; recording and stored history work offline. Map and third-party credits remain visible in the app.

Community comparisons require joining the relevant audience. Sharing is optional and starts after the privacy notice and explicit agreement. Supabase stores an anonymous authentication identity, nickname, chosen country/area and recent daily figures you select: distance, journey count, active days and optional highest recorded speed. Private-only profiles are excluded from public rankings. Only members of a private group can compare its scores. Hidden distance, journey count and speed values are removed from stored comparison totals; hidden active-day counts are excluded from output. Related information can still be inferred from figures you share and date filters.

Community does not upload routes, coordinates, speed traces, incidents, videos or saved places. Only eligible recorded driver journeys qualify; imports and passenger journeys are excluded. Stop sharing removes your profile, scores, memberships and groups you own, with a pending state if offline. Scores and areas are self-reported, not independently verified.

Save a private Community recovery code outside your phone before uninstalling. Anyone with a valid code can take over your Community profile. Codes are single-use and can be replaced or disabled. Recovery moves your profile, shared scores, memberships and group ownership to a new installation; owned group invites reset. Uploads pause until you explicitly resume them, so an empty phone cannot overwrite your shared history. Restore journeys and recordings separately from a progress backup. If you have no recovery code, stop sharing before uninstalling or clearing app data.

App usage reporting is a separate optional choice, disabled until you explicitly agree. It uses a random installation identity, app version and server UTC activity days to count active participating installations, including users outside Community. Routes, locations, speeds, recordings, nickname and journey records are excluded. You can turn it off in Settings > Privacy; usage history removal retries when connected. Counters are private to the maintainer. Reports reflect foreground use rather than background tracking. Reporting uses a recent 90-day window; older records are cleared as new reports arrive. Usage consent and credentials are not included in progress exports.

Share app is a standalone button at the top of Settings and shares the latest public release link.

Please report bugs using Issues without posting private Timeline exports, location histories or camera footage. See each release's notes for known limitations.
