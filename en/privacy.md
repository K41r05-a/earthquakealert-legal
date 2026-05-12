---
layout: null
title: "Privacy Policy"
lang: en
permalink: /en/privacy/
date: 2026-05-12
---

# Privacy Policy

Last updated: 2026-05-12

Earthquake Alert — Android app.

## Who we are

This Privacy Policy applies to the Earthquake Alert Android application ("the App"). The App is maintained by the Earthquake Alert project. Contact: alertsystems@atomicmail.io.

## Scope

This policy explains how the App handles information. The App has no backend, no user accounts, and no remote data collection.

## What we don't collect

- We do not collect analytics, usage statistics, or telemetry.
- We do not include crash reporting SDKs (Firebase Crashlytics, Sentry, Bugsnag, AppCenter — none).
- We do not include advertising SDKs or third-party trackers.
- We do not require accounts, login, or any personal information from you.
- We do not offer in-app purchases.
- We do not collect user-generated content.
- We do not access your contacts, photos, files, calendar, messages, audio, or other personal device data.

## Permissions and what they do

- **`INTERNET`** — required to fetch earthquake data from USGS.
- **`ACCESS_NETWORK_STATE`** — required to detect connectivity.
- **`ACCESS_COARSE_LOCATION`** (optional, runtime) — used **on-device only** to compute distance from your saved home location and to apply the radius filter. Never transmitted to us or to third parties.
- **`ACCESS_FINE_LOCATION`** (optional, runtime upgrade) — same purpose as coarse, higher precision when granted. Same on-device-only usage.
- **`POST_NOTIFICATIONS`** (Android 13+, runtime) — used to deliver **local** notifications. No remote push notifications.
- **`RECEIVE_BOOT_COMPLETED`** — to re-schedule periodic refresh after device reboot. No data is sent.

## Network requests

- The App fetches public earthquake data from the U.S. Geological Survey (USGS) GeoJSON feeds. Example endpoint: `https://earthquake.usgs.gov/earthquakes/feed/v1.0/summary/all_hour.geojson`.
- Requests contain only the URL and standard HTTP headers (User-Agent, Accept). **No request body, no user identifiers, no home location** is included in these requests.
- The USGS server may log your IP address and User-Agent as part of standard server operations. USGS is a third party with its own privacy practices: see <https://www.usgs.gov/privacy>.
- If transmitting your IP address to USGS is a concern, you may use a VPN.
- The App makes no other network requests. No analytics endpoints, no advertising endpoints, no telemetry endpoints.

## On-device data

- Cached earthquake records (Room database) — public USGS data, retained for short-term offline access.
- User preferences (DataStore) — minimum magnitude, search radius, optional home latitude/longitude, onboarding completion flag, last-seen earthquake IDs.
- **All of this data is stored on your device only.** It is not transmitted anywhere.
- Uninstalling the App removes all on-device data automatically.
- Manual reset: System Settings → Apps → Earthquake Alert → Storage → Clear data.

## Children's privacy

The App is not directed to children under 13 (or the equivalent age in your jurisdiction). Because the App does not collect any off-device data, there are no children-specific data flows.

## Changes to this policy

We may update this policy. The "Last updated" date at the top reflects the most recent material change. Material changes are also surfaced in Play Store release notes.

## Contact

Questions about this policy: alertsystems@atomicmail.io.

Public issues: <https://github.com/K41r05-a/earthquakealert-legal/issues>.
