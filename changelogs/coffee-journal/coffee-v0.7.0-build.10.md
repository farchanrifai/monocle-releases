# Coffee Journal 0.7.0 (build 10)

Released 3 October 2026. Make an occasional memory photo into a personal cup sticker, for iOS 17 and later.

## New

- Open **Frame photo sticker** from the Log sheet or a saved coffee's photo section. Preview your design on warm dotted paper before applying it.
- Choose Original, Square, Portrait, or Circle shapes, with None, Slim, or Wide white paper borders. Drag to position, pinch or use the Zoom slider, and use labeled position sliders for adjustment without gestures. Reset framing restores the default design.
- Apply uses the framed photo as your cup sticker. In Log, it remains a draft until the coffee saves. In a saved coffee, Apply commits the new design; Cancel retains the previous one. The original memory photo stays unchanged, and the existing toggle returns your collection to its illustrated cup.
- Reopen a framed sticker with its saved shape, border, zoom, and position. Each adjustment starts from the original memory photo, avoiding repeated crops or borders. The same artwork appears in your journal and shared scrapbook.
- Keep the previous design after an unsuccessful save. If a photo changes or the coffee is deleted while a sticker is being prepared, the result is rejected and unused new artwork is cleaned up. Referenced photos and café logos remain protected. The temporary sample journal keeps photo changes disabled.

Manual framing crops the full memory photo. It replaces the derived sticker rather than adding an outline around an automatic Vision subject cutout.

## Privacy and backups

Framing runs on-device and adds no network requests or permissions. The new PNG stores only the validated framing recipe; it does not copy the original image's EXIF/GPS metadata or journal writing. The saved memory photo's bytes remain unchanged. This photo is the journal's normalized memory image, not a full-resolution camera archive.

The released schema and native backup format remain version 5. Backups retain both original and sticker images, and the framing controls reopen after restore even when conflicting image filenames are renamed. Existing coffees, reflections, café logos, and personalization keep their current formats. Native backups from the current app's versions 1–4 remain readable.

## Validation

All 165 native data, migration, backup, image, and rendering tests passed on the iOS 26.5 iPhone 17 Pro simulator. New coverage checks crop bounds, image orientation and mirroring, transparent masks, borders, preview/save pixel limits, recipe privacy, malformed settings, draft cancellation and ownership, stale edits, actual storage-save failures, shared-image protection, and editable-sticker backup roundtrips with filename conflicts.

Three new UI flows and five affected logging, journal/share, Passport, and reflection flows passed, bringing the total to 173 distinct native tests. The new flows verify applying and saving a sticker, reopening its recipe, returning to the illustrated cup and back, editing the memory note without changing the design, cancelling draft and saved changes, and read-only sample controls. Editing and cancellation also passed in dark mode, and the complete create/save/edit/reopen flow passed with accessibility-large text. Light, dark, and larger-text screenshots were reviewed.

The unsigned arm64 Release IPA was validated for ZIP integrity, unsigned status, stable bundle identity, version 0.7.0 (build 10), and iOS 17 minimum OS. Packaged café catalog artwork matches the source; synthetic UI fixtures are excluded from the Release binary. The publication helper's 13 tests passed.

## Installation

This IPA is unsigned and keeps the existing `com.farchan.CoffeeJournal` app identity. Keep a journal backup before updating. SideStore/LiveContainer installation, data-preserving updates, camera, photo cutout quality, and Photos/Files/share sheets still require physical-device verification.

The older Coffee Journal Prototype remains a separate app. Its journal and backup format do not transfer to this app.

Source: [770a675](https://github.com/farchanrifai/coffee-journal/commit/770a675efcca0302142d49f0caf27eb20284c6ae).
