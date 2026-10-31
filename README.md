# Ad Clicker releases

Signed Android APKs and update manifests for Ad Clicker. Source code and portable Windows Diagnostic Studio packages are maintained in a separate private repository.

[Download the latest APK](https://github.com/PHOEN1Xcz/Ad-Clicker-Releases/releases/latest)

## Install or update

Install the APK over the existing Ad Clicker app to preserve rules and settings. Android 14 or newer is required. Version 0.0.3 includes the local OCR model and is larger than earlier builds.

In-app updates: Settings → Check for updates. Version 0.0.2 uses Save and check for updates. Checks run only when requested; the updater verifies SHA-256, package identity, increasing versionCode and matching APK signature. No GitHub login is needed for public APK downloads.

Assets: Ad-Clicker-<version>.apk, ad-clicker-update.json, SHA256SUMS.txt. Source code, diagnostic reports, pairing credentials and signing keys are not published here.

## 0.0.3

Adds accessibility/OCR/shape/pattern recognition, prioritized full-screen search, session-aware recovery across ad popups, scroll-to-close handling, Start next ads rules, free overlay positioning, quick categories and live similarity tuning. Optional detailed diagnostic recordings can be exported or sent to a paired Studio over a local network. Clicker works independently of Studio.

This is an early development build. Host/core tests, real saved-frame recognition checks, APK validation and portable Studio tests passed. The new Android behavior still requires testing on a physical device; no phone or emulator was connected during preparation. Reward eligibility is controlled by the original app and its ad SDK.

## Version levels

Level 1: 1.0.0, 2.0.0. Level 2: 0.1.0, 0.2.0. Level 3: 0.0.1, 0.0.2, 0.0.3. Android versionCode increases with every release.
