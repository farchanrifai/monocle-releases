# Coffee Journal 0.3.0 (build 6)

Released 2 October 2026. More cup stickers and personal colors for iOS 17 and later.

## New

- Five new illustrated stickers: a latte bowl, foamy cappuccino cup, cortado glass, cold brew bottle, and iced takeaway cup. The original five illustrations remain available.
- Choose Automatic, Sage, Terracotta, Cream, or Blue from the small dropdown on your sticker. Colors change the vessel or its accents while keeping the coffee's natural appearance. The sticker stays opaque; glass remains on its dropdown.
- Latte, flat white, cappuccino, cortado, cold brew, mocha, and iced mocha now select a matching illustration. Common typed names, accents, and hyphens are recognized. A manual illustration choice stays selected while typing; choosing a popular drink applies its match. Your color stays selected through either change.

## Improved

- Cup illustration and color carry through saved memories, usual orders, one-tap logging, repeat, both journal layouts, entry details, and scrapbook exports.
- Backups preserve cup colors, and CSV export includes a Cup color column. Earlier backups from this native app remain readable, with Automatic colors for records without a saved color.
- Explicit journal migration adds cup colors while preserving existing illustrations, photos, café notes, personalized stamps, Home settings, and Want to try state. Existing memories retain their original palettes.

## Validation

93 distinct tests passed on the iOS 26.5 iPhone 17 Pro simulator: 76 data, migration, backup, photo, and rendering tests plus 17 user-flow tests. Both new cup flows passed a focused rerun after correcting a test navigation action. Compatibility tests migrate and reopen populated databases created by the shipped v0.1.3 and v0.2.0 code, and restore their photo backups. Cup coverage includes every illustration/palette, storage reopening, usuals and repeat, duplicate imports, malformed color/style rejection before writes, CSV export, and precise visit timestamps.

Light and dark previews were reviewed, including all ten cup styles in a monthly scrapbook. Both new cup flows also passed in dark appearance, and cup matching, palette selection, manual overrides, saving, and editing passed with larger accessibility text.

The unsigned arm64 device Release build succeeded. IPA archive integrity, unsigned status, bundle identity, version 0.3.0 (build 6), and iOS 17 minimum OS were verified. The publication helper's 13 tests passed.

## Installation

This IPA is unsigned and keeps the existing `com.farchan.CoffeeJournal` app identity. Keep a journal backup before updating. SideStore/LiveContainer installation, data-preserving updates, camera, photo cutout quality, and Files/share sheets still require physical-device verification.

The older Coffee Journal Prototype remains a separate app. Its journal and backup format do not transfer to this app.

Source: [ee797f0](https://github.com/farchanrifai/coffee-journal/commit/ee797f0ead3921c7b9b813ceb1b42b973254b13f).
