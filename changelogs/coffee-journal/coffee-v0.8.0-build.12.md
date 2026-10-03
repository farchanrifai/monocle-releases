# Coffee Journal 0.8.0 — Passport collections

Build 12 · 3 October 2026 · iOS 17 and later

## What’s new

- Gather saved café branches into personal collections such as Jakarta cafés, Weekend finds, or Favorites. A café can belong to several lists; include your Home ritual when you want it alongside your café stamps.
- Use the compact All places menu in Passport to switch collections, create a list, or manage its name and places. The same collection filters both Stamps and Want to try. Your personal filter is remembered, while the sample journal stays separate.
- Add cafés directly to the selected collection, choose lists while adding or editing a café, or update memberships from its details. Save applies the selection; Cancel discards the draft. Reusing an existing café through Add preserves its other lists.
- Rename, edit, or delete a collection. Removing a list keeps your cafés, stamps, logos, usual orders, and coffee memories. Merging duplicate café branches also combines their collection memberships.
- Collections organize your places without changing stamp rules: café stamps still require a recorded physical visit, and Home appears after a home coffee.
- Backups now include collection names, branch memberships, Home choices, and creation dates. Restore previews collection counts, adds missing lists, and keeps existing collections unchanged when either their identity or name matches. Repeated restores do not duplicate lists. Collection names stay out of CSV and shared monthly scrapbooks.

## Data continuity

The current native app keeps its bundle identifier, `com.farchan.CoffeeJournal`. Schema V6 adds collections through an explicit V5→V6 migration, preserving the released coffee, café, usual-order, Home-preference, and monthly-reflection models. Existing journals start with no collections. Native V1–V5 backups remain readable alongside V6 backups.

The separate compatibility prototype uses another bundle identifier, data model, and backup format. It remains available separately; this app has no migration/import path for its data.

## Validation

- All 184 unit tests passed on the iOS 26.5 iPhone 17 Pro simulator, including collection persistence, validation, transaction rollback, merge/deletion preservation, backup round trips, duplicate restore precedence, and malformed archives rejected before data or images change.
- Migration checks cover populated databases generated with unchanged released V1–V5 app code. The new independent V5 database/backup pair retains every record, preference, timestamp, logo, original photo, editable sticker recipe, and monthly reflection before adding, reopening, exporting, and restoring a V6 collection.
- All 19 selected UI flows passed, covering collection creation, exact renaming, membership Save/Cancel, discarded café/list drafts, Home filtering, selected-list café creation, safe deletion, demo isolation, and existing Passport, café-logo, and reflection navigation.
- Dark-mode and accessibility-large-text flows passed for collection filtering, a café earning its first stamp within the same collection, Home choices, and the sample manager/editor. Screenshots were reviewed in light, dark, and enlarged-text appearances.
- All 13 publication-helper tests passed.
- The unsigned arm64 Release IPA passed ZIP-integrity, unsigned-status, bundle-identity, version/build, and minimum-OS checks. All six packaged café-logo assets match their source bytes; DEBUG-only synthetic fixtures are absent from the Release binary.

## Device limitations

This IPA is unsigned. Simulator validation does not confirm SideStore/LiveContainer installation, camera behavior, Vision cutout quality, Photos/Files/share-sheet behavior, or a data-preserving update on a physical phone. Those checks still require the intended device. Save a native backup before updating, uninstalling, or changing containers.

Source: [7f2b400](https://github.com/farchanrifai/coffee-journal/commit/7f2b4004b889d98dda4714f0d6a0bb6fe33bba82).
