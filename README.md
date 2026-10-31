# Ad Clicker releases

Signed Android APKs and update manifests for Ad Clicker. Source code and PC diagnostic packages are maintained in a separate private repository.

[Download the latest release](https://github.com/PHOEN1Xcz/Ad-Clicker-Releases/releases/latest)

## Install or update

Download the APK from Releases and install it over the existing Ad Clicker app to preserve rules and settings. Android 14 or newer is required.

For in-app updates, use **Settings → Updates** with repository `PHOEN1Xcz/Ad-Clicker-Releases`. Version 0.0.1 requires entering this name manually; version 0.0.2 supplies it by default. Checks run only when requested. Android asks for installation permission if needed.

Release assets:

- `Ad-Clicker-<version>.apk` — signed Android application.
- `ad-clicker-update.json` — versionName, versionCode, apkUrl, sha256 and notes for the updater.
- `SHA256SUMS.txt` — APK checksum.

The updater verifies the checksum, package identity, increasing versionCode and matching APK signature. No GitHub account or access token is needed for public downloads.

## Version levels

Level 1: 1.0.0, 2.0.0. Level 2: 0.1.0, 0.2.0. Level 3: 0.0.1, 0.0.2. The Android versionCode increases for every release.

## Current development status

0.0.2 adds a compact vertical overlay, floating settings/rules, full screenshot selection with zoom and pan, an English interface and system light/dark themes. It is an early development build: host tests and APK validation passed, but the new UI and gestures still require testing on a physical Android device.

Recognition and rule storage run locally. Reports and screenshots are exported only by the user. This repository does not collect diagnostic reports.
