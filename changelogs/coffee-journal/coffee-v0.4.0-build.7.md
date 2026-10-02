# Coffee Journal 0.4.0 (build 7)

Released 2 October 2026. Café logos for your personal coffee passport, for iOS 17 and later.

## New

- Find a café logo using its name and area. Choose the matching café and website, preview its website icon, then use it in your stamp. No location permission or account is needed. Availability depends on Apple Maps business listings and the café's website; an icon may differ from its full brand artwork.
- Upload your own logo from Photos or Files when a result is missing or unsuitable. Images already on your device can be used offline. Artwork keeps its original colors, transparency, and complete proportions. Wide logos fit within the stamp; transparent white marks receive a readable dark backing.
- Logos appear in Passport stamps, café details, and Want to try. Replace or remove them in Edit café. Your frame, ink, café name, branch, and visit date stay part of the stamp, and the personal icon returns when a logo is removed or unavailable. Home keeps its personal illustration.

## Improved

- Native backups now include referenced café logos. Earlier backups from this app remain readable, and existing cafés keep their personal stamp icons after updating.
- An explicit journal migration preserves saved coffees, cup choices, photos, usuals, café notes, stamp designs, Home preferences, and Want to try state while adding optional logo references.
- Cancelling an import or café edit cleans up pending artwork; failed replacements keep the saved logo. Café merges retain the destination's logo, or adopt the source logo when the destination has none. Shared images remain protected until their last reference is removed.
- Settings describes the new backup contents and displays the installed app version and build.

## Privacy

Logging and your saved collection continue to work offline. Find logo sends the entered café name and area to Apple Maps, then requests the business website you select and its advertised icon URLs, including redirects. A confirmed image is saved locally and remains available offline. Uploads are processed on-device; no journal account or custom backend is used.

## Validation

136 distinct native tests passed on the iOS 26.5 iPhone 17 Pro simulator: 114 data, migration, backup, image, and rendering tests plus 22 app-flow tests. A focused rerun passed all data tests, all five logo flows, and the affected Passport flow after correcting a logo editor button interaction and test scrolling. Compatibility checks migrate and reopen populated journals created by the shipped v0.1.3, v0.2.0, and v0.3.0 code, and restore their native backups.

Logo coverage includes persistence, replacement/removal, draft cancellation, shared image cleanup, café merges, backup collisions, duplicate imports, and malformed/missing assets. Lookup tests cover HTML icon links, redirects, ICO/WebP normalization, bounded responses/attempts, cancellation, and upload fallback. A separate live simulator check passed business search for Fore Coffee in Jakarta and real website icon retrieval from Fore and Kopi Kenangan.

Light and dark previews were reviewed, including wide transparent white wordmarks. All five logo flows passed in dark mode. Upload, earned stamps, and lookup preview/confirmation also passed with larger accessibility text.

The unsigned arm64 device Release build succeeded. IPA integrity, unsigned status, bundle identity, version 0.4.0 (build 7), and iOS 17 minimum OS were verified against the final artifact. The publication helper's 13 tests passed.

## Installation

This IPA is unsigned and keeps the existing `com.farchan.CoffeeJournal` app identity. Keep a journal backup before updating. SideStore/LiveContainer installation, data-preserving updates, camera, photo cutout quality, and Photos/Files/share sheets still require physical-device verification. Website coverage and icons vary by café; manual uploads remain available.

The older Coffee Journal Prototype remains a separate app. Its journal and backup format do not transfer to this app.

Source: [fc9485f](https://github.com/farchanrifai/coffee-journal/commit/fc9485f218174500237d2b197d27564b035e2441).
