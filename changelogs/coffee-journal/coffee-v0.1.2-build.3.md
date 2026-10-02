# Coffee Journal 0.1.2 (build 3)

Released 2 October 2026. Full journal preview for iOS 17 and later.

## Added and improved

- Warm dotted-paper design, five original cup illustrations, Cup collection and Daily stories layouts, month navigation, search, and favorites.
- Café Passport with visit stamps, branch history, a Home stamp, and a Want to try list.
- Saved usual orders, quick logging with Undo, entry editing and deletion, and monthly coffee and spending reflections.
- One drink field with popular choices and matching cup artwork. Change the cup from the sticker's dropdown; Save remains visible while details scroll.
- Enter café names directly in Log, or choose a saved-place suggestion. Branch details are optional, and new cafés save together with the coffee.
- Add photos before saving, with preview, removal, and an optional photo sticker. Cancelled drafts clean up pending files; saved-photo cleanup respects shared attachments.
- Native Liquid Glass for floating navigation, Log/Save, photo actions, and compact controls, with solid accessibility and older-iOS fallbacks.
- Fixed duplicate Log controls, sticky journal controls, tab touch areas, and returning to the title when switching tabs.
- Monthly scrapbook PNG sharing, versioned journal/photo backups, validated restore, and CSV export. Journal data stays on the device.

## Validation

44 tests passed across simulator verification runs. Light and dark screens and scrapbook output were reviewed. The unsigned arm64 device Release build succeeded; IPA integrity and version metadata were verified.

## Installation and prototype data

This IPA is unsigned and requires your existing SideStore/LiveContainer installation setup. Camera, photo cutout quality, Files/share sheets, and installation/update behavior still need physical-device verification.

Install the new **Coffee Journal** entry with identifier `com.farchan.CoffeeJournal`. The old prototype remains separately available as **Coffee Journal Prototype** with identifier `com.farchanrifai.coffeejournal`.

The two apps use different data and backup formats. This build does not import the prototype's journal or backups. Keep the prototype and an exported copy of its data if you have memories stored there.
