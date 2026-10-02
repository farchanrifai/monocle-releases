# Coffee Journal 0.1.3 (build 4)

Released 2 October 2026. A refinement of navigation and the Log sheet for iOS 17 and later.

## Improved

- Native Journal, Passport, and Search tabs, with system navigation bars and Liquid Glass on iOS 26. Settings and Log use native toolbar controls.
- Search has its own space for finding drinks, cafés, and memories across all months. Searching no longer changes the monthly Journal view.
- Cup artwork stays a paper sticker. Only its small dropdown control uses glass; popular drink choices still select matching cups, and manual cup choices remain available.
- Add photo and the memory note sit together in an optional Memory section, with the preview and photo-sticker option available before saving.
- A compact source menu replaces the crowded Later/Home/Café/Delivery strip. Café names and saved-place suggestions remain inline.
- Passport uses a balanced Stamps / Want to try picker, with Add café moved to the navigation toolbar.
- Improved Save button text contrast in dark appearance.

## Validation

46 tests passed on the iOS 26.5 iPhone 17 Pro simulator: 35 data, backup, photo, and rendering tests plus 11 user-flow tests. The dark Log flow was rerun after the final contrast correction. Light and dark previews were reviewed. The unsigned arm64 device Release build succeeded; IPA integrity, bundle identity, version 0.1.3 (build 4), and iOS 17 minimum OS were verified.

## Installation

This IPA is unsigned and uses the existing `com.farchan.CoffeeJournal` app identity. Camera, photo cutout quality, Files/share sheets, and SideStore/LiveContainer installation and update behavior still require physical-device verification.

The older Coffee Journal Prototype remains a separate app. Its journal and backup format do not transfer to this app.

Source: [2e601d4](https://github.com/farchanrifai/coffee-journal/commit/2e601d4a00a7db062cc205f862f3c1f32fc183d9).
