# Coffee Journal 0.7.1 (build 11)

Released 3 October 2026. More reviewed café artwork for your coffee passport, for iOS 17 and later.

## New

- The offline logo library now includes **Tomoro Coffee**, **Tanamera Coffee**, and **Toko Kopi Tuku**, alongside Fore Coffee, Kopi Kenangan, and Janji Jiwa.
- Search the new names and their aliases, including a branch suffix, or clear the search to browse all six brands. Preview the full artwork before choosing it. Your saved café name and branch stay as you entered them.
- Tuku's original white cup and wordmark use the existing readable espresso backing. Tomoro's orange cat and complete wordmark and Tanamera's red mountain and wordmark retain their original colors and proportions. These are authentic complete brand marks, rather than website icons.
- Photos and Files remain available for other cafés, alternative artwork, and personal logos. Point Coffee and Excelso await suitable official artwork with adequate resolution.

## Privacy and saved artwork

The library ships with the app and works offline. Browsing, searching, and choosing a logo add no network requests, accounts, location access, or permissions. The original three catalog records and artwork are unchanged.

The journal schema and native backup format remain version 5. Selecting a logo copies its artwork into your journal; later catalog additions do not replace saved stamps. Existing uploaded logos, selected artwork, coffees, reflections, and photo stickers keep their current formats. Native backups from this app's versions 1–4 remain readable.

## Validation

All 165 native data, migration, backup, image, and rendering tests and all nine café-logo UI flows passed on the iOS 26.5 iPhone 17 Pro simulator, for 174 distinct native tests. The publication helper's 13 Python tests also passed.

New UI coverage checks reaching the final alphabetical brand, cancelling a preview without importing, explicitly choosing and saving Tomoro without changing the personal café name or branch, and selecting Tuku and Tanamera through aliases with branch suffixes. Existing upload, missing-brand fallback, preview cancellation, replacement/removal, and earned-stamp flows passed. The new flows also passed in dark mode and with accessibility-large text. Screenshots were reviewed in each appearance.

The unsigned arm64 Release IPA was validated for ZIP integrity, unsigned status, stable bundle identity, version 0.7.1 (build 11), and iOS 17 minimum OS. The catalog and all six packaged PNGs match source resources byte for byte; source/provenance hashes and Tuku's lossless RGBA conversion were independently reviewed. Original catalog records and artwork remain unchanged. DEBUG-only synthetic fixtures are absent from the Release binary.

## Installation

This IPA is unsigned and keeps the existing `com.farchan.CoffeeJournal` app identity. Keep a journal backup before updating. SideStore/LiveContainer installation, data-preserving updates, camera, Vision extraction quality, and Photos/Files/share sheets still require physical-device verification.

The older Coffee Journal Prototype remains a separate app. Its journal and backup format do not transfer to this app.

Source: [90fc973](https://github.com/farchanrifai/coffee-journal/commit/90fc9733402dc79a7c3f7f05b4dd93d42a0565c1).
