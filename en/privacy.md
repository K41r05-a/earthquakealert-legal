---
layout: null
title: "Privacy Policy"
lang: en
permalink: /en/privacy/
date: 2026-06-13
---

# Privacy Policy

Last updated: 2026-06-13

TerraWatch — Android app.

## Who we are

This Privacy Policy applies to the TerraWatch Android application ("the App"). The App is maintained by the TerraWatch project. Contact: alertsystems@atomicmail.io.

## Scope

This policy explains how the App handles information. The App has no backend and no user accounts. The only user data sent off your device is the approximate map area shared with Google to render map tiles when you open the map — see "Map tiles" below. Everything else stays on your device.

## What we don't collect

- We do not collect analytics, usage statistics, or telemetry.
- We do not include crash reporting SDKs (Firebase Crashlytics, Sentry, Bugsnag, AppCenter — none).
- We do not include advertising SDKs or third-party trackers.
- We do not require accounts, login, or any personal information from you.
- We do not offer in-app purchases.
- We do not collect user-generated content.
- We do not access your contacts, photos, files, calendar, messages, audio, or other personal device data.

## Permissions and what they do

- **`INTERNET`** — required to fetch earthquake data from USGS, EMSC, and GEOFON, tsunami bulletins from NOAA, and map tiles from Google.
- **`ACCESS_NETWORK_STATE`** — required to detect connectivity.
- **`ACCESS_COARSE_LOCATION`** (optional, runtime) — used to compute distance from your saved home location and to apply the radius filter. These coordinates are not sent to us and are not used for tracking. However, if you open the Map screen or Zone map picker with a home zone set, your approximate area is sent to Google to load map tiles — see "Map tiles" below.
- **`POST_NOTIFICATIONS`** (Android 13+, runtime) — used to deliver **local** notifications. No remote push notifications.
- **`RECEIVE_BOOT_COMPLETED`** — to re-schedule periodic refresh after device reboot. No data is sent.

## Network requests

The App makes HTTPS requests to the following destinations. None include a request body, account, or user identifier; servers may log the originating IP address and User-Agent as part of standard server operations, which is outside our control and not used by us.

- **USGS** — public earthquake data from the U.S. Geological Survey GeoJSON feeds. Example endpoint: `https://earthquake.usgs.gov/earthquakes/feed/v1.0/summary/all_hour.geojson`. USGS privacy: <https://www.usgs.gov/privacy>.
- **EMSC** — public earthquake records from the European-Mediterranean Seismological Centre FDSN event service at `https://www.seismicportal.eu`.
- **GEOFON** — public earthquake records from the GFZ Potsdam GEOFON service at `https://geofon.gfz.de`.
- **NOAA** — public tsunami bulletins from the U.S. National Oceanic and Atmospheric Administration tsunami warning centers (PTWC, NTWC) at `https://www.tsunami.gov`.
- **Google Maps** — map tiles, only while the Map screen or Zone map picker is open (see "Map tiles").

These requests carry no analytics, advertising, or telemetry payload. If transmitting your IP address to these public sources is a concern, you may use a VPN.

### Map tiles

When you open the Map screen or the Zone map picker, the app uses the Google Maps SDK to download map tiles. Each tile request includes the current camera viewport — that is, an approximate geographic area. When you have configured a home watch zone, the camera starts centred on that zone, so the first tile requests carry approximate coordinates of your home (rounded to ~1.1 km before storage, then used as the camera centre). No other personal data is sent. Google processes these requests under the Google Maps Platform Privacy Notice (<https://policies.google.com/privacy>). If you never open the Map screen or the Zone map picker, no location data leaves your device.

## On-device data

- Cached earthquake records (Room database) — public USGS, EMSC, and GEOFON data, retained for short-term offline access.
- User preferences (DataStore) — minimum magnitude, search radius, optional home latitude/longitude, onboarding completion flag, last-seen earthquake IDs.
- **All of this data is stored on your device only.** It is not transmitted anywhere, except that saved coordinates may seed the map camera as described in "Map tiles".
- Uninstalling the App removes all on-device data automatically.
- Manual reset: System Settings → Apps → TerraWatch → Storage → Clear data.

## Children's privacy

The App is not directed to children under 13 (or the equivalent age in your jurisdiction). Because the App does not collect any off-device data beyond the approximate map area described above, there are no children-specific data flows.

## Changes to this policy

We may update this policy. The "Last updated" date at the top reflects the most recent material change. Material changes are also surfaced in Play Store release notes.

## Contact

Questions about this policy: alertsystems@atomicmail.io.

Public issues: <https://github.com/K41r05-a/earthquakealert-legal/issues>.
