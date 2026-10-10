# 3.0.0-rajan.4 — Home and navigation refinement

The main Home menu now has stable Library, Anki Review, Reading Stats and More destinations. Anki opens setup when unconfigured. Reading Stats remains available before the first reading session. More contains Recent Books, available saved items, configured OPDS catalogs, File Transfer and Settings. Back from secondary destinations restores the More selection. Existing Minimal/Dashboard direct-button layouts are preserved.

Lyra Home has a compact white reading panel, crisp focus outlines, quieter author text and known progress/time-left details. Missing covers use the text width instead of a black placeholder. Longer titles wrap. Menu pagination follows available height, and More omits the setting-picker's Selected badge.

Source commit: 31853c80934b79d5fdfb78575e74a680b83a05d9
Runtime version: 3.0.0-rajan.4
Image bytes: 5,648,816
OTA slot headroom: 904,784 bytes
SHA-256: a47976012838904daca89dbffbee1b400fa80dacf7893aa52a8b41e890d3ccea

Validation: simulator build and navigation smoke passed, including Home to Anki setup, Reading Stats, More to Settings, selection restoration and cancellation. Normal, long-title and empty Home screens were visually inspected. 52 focused existing tests passed. Original-X4 production build and image identity/integrity checks passed after resolving temporary build disk pressure.

Application-only firmware for the original ESP32-C3 X4 and existing x4-dual-ota-v1 layout. English UI/hyphenation; Nearby sharing/sync remains omitted. Prior Anki loading repairs are retained; physical confirmation of the previously reported crash is still pending. This candidate has not been installed or accepted on the physical device.

The reused SDK descriptor retains its cached base project/revision; use the runtime version and exact SHA-256 above to identify this image. Published on the established signed test OTA channel, retaining the stable channel and previous releases.
