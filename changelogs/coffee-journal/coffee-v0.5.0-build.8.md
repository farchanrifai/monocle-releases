# Coffee Journal 0.5.0 (build 8)

Released 3 October 2026. A curated café logo library for your coffee passport, for iOS 17 and later.

## Improved

- Choose full café logos from an offline library instead of using website icons. The starter collection includes Fore Coffee, Kopi Kenangan, and Janji Jiwa, with reviewed artwork from their official brand sites.
- Search café names and aliases as you type, or browse every logo. Select a logo to preview it, then confirm before it becomes part of your stamp. The library has one search field and no city or website-selection step.
- Upload artwork from Photos or Files for other cafés or a personal alternative. Your stamp icon remains available when you prefer it.
- Artwork keeps its full proportions, colors, and transparency. Previously saved website icons and uploads stay unchanged until you replace or remove them. Selecting a library logo copies it into your journal, so future library changes do not alter existing stamps.
- Cancelling a preview keeps your existing logo. Chosen artwork continues to appear in Passport, café details, and Want to try, and travels with native backups. Journal schema and backup format remain version 4.

## Privacy

Logo search, browsing, previews, and selection now work entirely on-device. This release removes the Apple Maps and business-website icon requests. No location permission, account, or logo service is needed.

## Validation

119 distinct native tests passed on the iOS 26.5 iPhone 17 Pro simulator: all 111 data, migration, backup, image, and rendering tests plus seven logo flows and the affected Passport edit flow. Twelve catalog tests cover bundled artwork, aliases and branch suffixes, ambiguous matches, invalid metadata and images, recoverable library errors, and read-only preview versus staged import. Existing logo coverage continues to check saved references, replacement/removal, cancellation, shared assets, café merges, and backup roundtrips.

Library browsing/search and preview/confirmation also passed in dark mode and with accessibility-large text. Light, dark, and larger-text screenshots were reviewed. The unsigned arm64 Release IPA was validated for ZIP integrity, unsigned status, bundle identity, version 0.5.0 (build 8), iOS 17 minimum OS, and the packaged catalog/artwork. The publication helper's 13 tests passed.

## Installation

This IPA is unsigned and keeps the existing `com.farchan.CoffeeJournal` app identity. Keep a journal backup before updating. SideStore/LiveContainer installation, data-preserving updates, camera, photo cutout quality, and Photos/Files/share sheets still require physical-device verification. The library is a small starter collection; uploads remain available for other cafés.

The older Coffee Journal Prototype remains a separate app. Its journal and backup format do not transfer to this app.

Source: [935df16](https://github.com/farchanrifai/coffee-journal/commit/935df1660067dca99fc340e89b365e24ffb598a0).
