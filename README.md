# Ad Clicker releases

Signed Android APKs and update manifests for Ad Clicker. Source code and portable Windows Diagnostic Studio packages are maintained in a separate private repository.

[Download the latest APK](https://github.com/PHOEN1Xcz/Ad-Clicker-Releases/releases/latest)

## Install or update

Install the APK over the existing Ad Clicker app to preserve rules and settings. Android 14 or newer is required. Version 0.0.3 includes the local OCR model and is larger than earlier builds.

In-app updates: Settings → Check for updates. Version 0.0.2 uses Save and check for updates. Checks run only when requested; the updater verifies SHA-256, package identity, increasing versionCode and matching APK signature. No GitHub login is needed for public APK downloads.

Assets: Ad-Clicker-<version>.apk, ad-clicker-update.json, SHA256SUMS.txt. Source code, diagnostic reports, pairing credentials and signing keys are not published here.

## 0.9.0

Hotfix build 24 replaces the original build 23 under this release. It fixes single-line tab layout and highlight alignment, horizontal swiping across card content and immediate language updates on the open page. The displayed version stays 0.9.0; the higher Android versionCode allows an in-place update with the existing signing identity.

Guide adds concise offline help. The language selector beside the app name switches the interface between Czech, English, German, French and Spanish while preserving open forms, list position and scanning. Ad-text recognition supports common controls, scroll hints, timers and reward prompts in these languages independently of UI language. User names and raw diagnostic evidence are preserved. Handler 0.2.0 and Studio 0.3.0 are unchanged. Android versionCode 24, existing signing certificate; real-device testing is still required.

## 0.8.0

Rules combines independently scrolling manual and learned libraries with shared search and filters. Backup/import transfers both libraries, thumbnails, groups, verification and priority in a standalone ZIP. Reports centralizes Off/Compact/Full recording, local storage and delivery, estimates selected input size and shows the final ZIP size before sending. Compact exports retain causal before/problem/after evidence with fewer repetitive frames. The Master administration tab is named Admin. Diagnostic Studio is unchanged; the independent Handler 0.2.0 adds a persistent Windows user profile and notification-area operation.

Android versionCode 22; existing signing certificate. Validated by 346 core checks, 141 Android tests (one optional skip) and lint with no errors. Physical POCO/HyperOS behavior still requires device testing.

## 0.7.7

Level-3 fix for ads that open another app. **Return from apps opened by ads** covers a store, browser or installed game and keeps the original ad source through display changes. After Back, Clicker checks the ad again. An unproductive outbound control can be ignored in the same ad context to prevent repeated store openings. Home labels the app picker **Select ad source apps**.

## 0.7.6

Level-3 fix for rectangle selection. Hold the target while scanning is running or stopped. Clicker waits for the current window and screenshot and pauses automatic actions until the rule is saved or cancelled. Live test only shows the match. Press Play after leaving the editor to resume scanning.

## 0.7.5

Level-3 Clicker fix for scroll-to-close ads and panel responsiveness. Native scroll instructions can start a dedicated scroll flow without waiting for the full OCR pass. Native accessibility reading and click/scroll requests run off the panel thread, and physical touch delegation uses a separate executor. Learned-rule screen context is prepared once per pass instead of repeatedly for each node.

Scroll steps follow completion and fresh observations, resume after a missed header and stop at confirmed page completion even while the instruction remains visible. Scroll headers are evaluated separately from ad countdown bars. New timing events distinguish input delivery, native reads and delayed image results. Existing rules, learned findings, scan switches and the APK signing identity are retained. Handler 0.1.1 and Studio 0.3.0 are unchanged. Real-device timing and touch behavior still need verification on POCO/HyperOS.

## 0.7.4

Level-3 Clicker update. New learned findings stay standalone. Hold a sample or group to open a fixed selection toolbar for deleting, verifying meanings or manually combining findings. Edit meanings and group membership in one form, rename groups, and choose groups with rotating sample previews. Existing multi-sample groups are preserved.

Re-evaluate selected or all unverified findings against manually verified examples, including Ignore and contextual Back. A cancellable comparison shows reference images, similarity and reasons before applying clear matches as Auto confirmed. Ambiguous matches remain for review. This does not automatically create groups or grant user verification. Update downloads now show percentage, MB and the verification phase. These download indicators apply to updates initiated from 0.7.4 onward. Handler 0.1.1 and Studio 0.3.0 are unchanged.

## 0.7.3

Review and combine learned findings into groups with individually managed image samples. User-verified samples are retained outside the automatic limit and pinned on the next visit. Review supports Ignore and contextual Back. Lists update affected rows while preserving the viewport. Teaching rejects empty crops and can use stable foreground across moving backgrounds. Visible system bars are masked, and confirmed app screens use manual app rules.

## 0.7.2

Advanced / Diagnostics has individual switches for progress bars, numeric countdowns, timer rings, countdown scan throttling and heatmap search. Diagnostic reports record the settings and heatmap search results for comparison.

## 0.7.1

Faster fallback to display capture, focused checks for visual controls and fixed 50 ms coordinate taps. The panel stays touchable. Progress bars are tracked without estimating seconds, and close detection checks for adjacent speaker icons. Report Admin groups attempts by report and adds an archive and consolidated connections. Handler 0.1.1 is a separate portable release in the private project repository.

## 0.7.0

Level-2 update for report handling. The tester view shows upload confirmation and the status of the tester's reports. The optional Master pairing unlocks Report Admin, which groups diagnosis attempts by report and submits batches for existing Dropbox ZIPs. Ad Clicker Handler 0.1.0 is a separate portable Windows release in the private project repository. Diagnostic Studio remains at 0.3.0.

## 0.6.2

Level-3 Clicker update. One confirmed progress source controls waiting, with fallback after loss/stagnation; ad ordinals are excluded, edge bars survive color transitions, and small counter arcs have temporal validation. Available Skip/store steps remain usable during a video countdown while premature Close stays protected.

App-window screenshots exclude our accessibility overlays. The shorter panel stays visible with 75% background opacity, temporarily 50% while passing a gesture through; completion, cancellation and a watchdog restore touch input. Reports use smaller context images and original-resolution control crops, with incremental historical learning evidence. Full diagnostics preserves retained originals. Report format 3 and Studio 0.3.0 remain compatible; no Studio update is needed.

Install over the existing application to preserve rules, ordering, learning, heatmap, accounts and pairing. Host checks and saved-image replay do not replace live HyperOS/OCR/gesture or battery testing.

## 0.6.1

Level-3 fix from recorded 0.6.0 diagnostics. An accepted action in the current host's active ad can authorize a short-lived return context for another app, such as Allegro. Actual touch cancels this correlation; the host is retained and Back remains bounded. Unknown destinations require touch monitoring. No automatic edits to the external app list.

Native, visual and rule actions now share countdown/reward protection. Explicit reward countdowns survive short reading gaps, and a contextual early-close warning can resume playback without repeating the destructive close. Progress bars are tracked in parallel so a static stripe cannot monopolize tracking above a moving bottom bar. Confirmed numeric clocks take precedence over approximate bar velocity. Small numeric OCR uses bounded enlarged probes.

Diagnostic rectangles show candidate/tracked/lost/blocked controls, numeric values and progress estimates. Annotations are non-touchable, hidden before capture and retained as geometry/status metadata. Report format 3 and Studio 0.3.0 remain compatible; no Studio update is needed. Existing rules, learning, heatmap, ordering, account and pairing are retained.

293 core checks, 54 Android host tests and 50 Python tests passed. Replay found the bottom bar reliably in 8/17 saved frames versus 0/17 previously, with unchanged top-bar coverage; 11 recorded premature close attempts were blocked and the final reward-ready close allowed. These are recorded-frame/host checks; live HyperOS gestures, OCR and battery use still require phone testing.

## 0.6.0

Level-2 update: compact buttons and tabs with unchanged text sizes, narrow switch hit areas, Home with optional pinned/recent source apps, Auto-continue and a live accessibility repair shortcut. Recent usage uses optional Usage Access or observed apps; it is not the private system Recents task list. Observe only is removed; Live test remains read-only.

Logs now separates compact Events from Reports with selection, deletion and retention. Reports unifies connections, history, transfer status and signed diagnosis results. Incremental immutable batches support selecting multiple previous reports, destination-specific delivery receipts and deduplicated attachments in standalone version-3 ZIPs. An uploaded ZIP can be reused for a new diagnosis request. Managed cloud cleanup protects waiting/active requests and Keep items and verifies signatures and checksums.

Independent Studio 0.3.0 supports report formats 1/2/3 and an optional one-shot read-only Codex CLI worker triggered by a valid new request. Empty queues make no model calls; the old timed chat monitor is not enabled. Studio and cloud remain optional for Clicker operation. Existing rules, learning, heatmap, order and pairing are retained. Update Studio before sending format-3 reports over LAN.

272 core checks, 49 Android host tests, 50 Python tests and packaged Studio checks passed. A repeated unchanged export of the test dataset fell from 115.5 MB to 5.8 MB; this does not predict the size of new recordings. Android 16/HyperOS behavior, live gestures, account transfers and battery use still require phone testing.

## 0.5.0

Level-2 update: preserve the uncommitted rule name, category, action, purpose and similarity when adjusting a selection; show the selection edges inside the magnifier. Track small numeric countdowns with multiple plausible decreases over time. Optional adaptive checks reduce screenshot/OCR frequency during longer confirmed waits, with faster checks near the end and periodic wider exploration. Battery savings require measurement on a phone.

Optional direct Dropbox ZIP uploads to /AdClicker_data use PKCE sign-in, resumable chunks and verified size/content hashes. Signed diagnosis requests are published after upload confirmation. Independent Studio 0.2.0 receives requests for a configured local Codex monitor and returns signed results. Register your own Dropbox app and connect the account before use; the release contains no account credentials. Scanning, teaching and local reports remain independent of PC and cloud. Actual account uploads and Android 16 operation require user verification after setup.

## 0.4.1

Level-3 functional fix: verify Back outcomes inside known ad popups so closing a game-detail sheet can be followed by another Back from Google Play to the original ad. Unchanged popup actions time out and the visit has a bounded attempt limit. Preserve the known host through rule editing and the floating app window; explicit Stop still ends the session.

Rule choices are Click / Back and Ad control / App control / Ignore object, with contextual descriptions. Only in: shows the source app; mandatory scope is checked and locked for App control and Ignore object. Existing rule IDs, images and order remain intact.

Teaching distinguishes store navigation from ad closure. Native popup screenshots and Back-state events support marked-problem analysis without extra OCR in that capture path. Studio remains at 0.1.1. Actual Android gestures and complete ad cycles still need testing on a phone.

## 0.4.0

Level-2 Clicker update: an evolving local heatmap prioritizes focused searches by source app, orientation, ad phase and control role. Confirmed actions and verified teaching strengthen locations; no-effect outcomes and age weaken them. Misses trigger broad fallback, and periodic exploration still looks for new locations. Priors survive restarts and updates and never authorize clicks on their own.

Fix Vungle/Liftoff and known native close context, preserve the actual host across ad popups and teaching, mask the overlay for OCR, and identify a demonstrated target by its original window and area. Keep evidence of brief host returns before the next ad. Uncertain old examples are not enabled automatically.

Verify each dispatched action separately. A fresh unchanged target can receive bounded 45/90/140 ms gesture retries, including fallback after an accepted native click has no observed effect. Remember successful gesture duration locally and expand diagnostic action/coordinate/timing details. Rule cards reserve a smaller area around the Enabled switch for easier tab swipes.

Studio stays at 0.1.1. Existing rules, settings and pairing are preserved. Host tests and recorded-frame checks verify the code paths; actual gestures, latency, ad cycles and rewards need testing on a phone. Language expansion and cloud reporting remain planned separately.

## 0.3.0

Level-2 Clicker update: persistent tap teaching with manual finish, fresh pre-touch snapshots and observed outcomes. Learned actions are separate from your own rules, can be reviewed/disabled and have previous-version recovery. Context-aware ad launch learning handles changing counts in button text and verifies that an ad actually starts.

Marked problems are analyzed locally using retained events and image replay. Evidence can adjust inspection timing or suppress repeatedly unconfirmed built-in targets in a matching ad context. Uncertain discoveries need review or a demonstration; this is bounded local learning, not a general self-programming model.

Rule cards are compact, have inline yellow/gray Enabled switches and a left drag handle with animated reordering. Saved order determines priority among eligible own rules. Edits, toggles, usage and rule export/import preserve order. The Home indicator is drawn on the first layout without a swipe.

Studio remains at 0.1.1 and is optional. Existing rules/settings/pairing remain available. Android touch delegation, speed, full ad cycles and rewards require testing on a real device.

## 0.2.0

Level-2 Clicker update: continuous ad-scene tracking, action outcome verification and bounded local action history. Recognized ad activities retain their context until a real return to the host app. Popup return limits reset per visit. Timer bars and generic contrast-based close/skip symbols reduce reliance on saved samples; an optional single reveal touch can expose hidden controls in a recognized ad canvas.

Animated yellow tabs, preserved rule viewport, selection magnifier and opposite-corner rectangles, aligned category picker, persistent accessibility settings links, uninterrupted problem marking with REC countdown, and local diagnostic storage management. Rules, pairing and protected/in-use reports are preserved during cleanup.

Diagnostic Studio stays at 0.1.1 and does not need an update. Report/rule formats are compatible. Host tests and saved-frame recognition checks passed; the new UI, touch behavior, timing and complete ad cycles still need testing on a phone.

## 0.1.1

Level-3 update: swipe between main tabs, live accessibility connection checks, screenshot pacing and retry, contextual Ignore rules, and a separate category picker. ADVERTISEMENT starts a rapid comparison of newly appearing edge controls, including recognized crosses drawn inside WebViews. Anonymous small icons use a narrower side gutter to reduce false taps inside ad artwork. Pairing with the optional Studio uses its QR directly inside Clicker, without typing an address or PIN.

Studio 0.1.1 is a separate private release for a sharp compact QR and Ignore rule editing. Ordinary rules retain schema 1; Ignore bundles use schema 2, supported by Clicker and Studio 0.1.1. The app works without Studio. Host tests and packaged-app checks passed; the new Android behavior and the 0.5-second inspection target still require testing on a phone.

## 0.1.0

Level-2 update: fixes Play after Live test, maps selection/live overlays to original screen coordinates, and adds automatic initial similarity with a configurable margin. Uses generic SDK control IDs and native-bound icon geometry, stops extra swipes at the end of scrolling ads, and avoids semantic taps on non-actionable text. OCR now focuses on the top/bottom screen regions. Repeated unresponsive targets receive a temporary cooldown while scanning continues.

Clicker and optional Windows Diagnostic Studio have independent versions, packages and release tags. Clicker-only updates do not require a new Studio download; existing Studio 0.0.3 remains format-compatible.

## 0.0.3

Adds accessibility/OCR/shape/pattern recognition, prioritized full-screen search, session-aware recovery across ad popups, scroll-to-close handling, Start next ads rules, free overlay positioning, quick categories and live similarity tuning. Optional detailed diagnostic recordings can be exported or sent to a paired Studio over a local network. Clicker works independently of Studio.

This is an early development build. Host/core tests, real saved-frame recognition checks, APK validation and portable Studio tests passed. The new Android behavior still requires testing on a physical device; no phone or emulator was connected during preparation. Reward eligibility is controlled by the original app and its ad SDK.

## Version levels

Level 1: 1.0.0, 2.0.0. Level 2: 0.1.0, 0.2.0. Level 3: 0.0.1, 0.0.2, 0.0.3. Android versionCode increases with every release.
