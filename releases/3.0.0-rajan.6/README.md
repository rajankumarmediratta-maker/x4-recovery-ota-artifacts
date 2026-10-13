# Original XTEINK X4 — 3.0.0-rajan.6

Restores Settings as a permanent Home destination alongside Library, Anki and
Tools. Minimal/Dashboard also include Settings in their Menu, retaining the
existing third-front-button Settings shortcut. Updates remain under
Settings → System → Check for Updates.

For the installed 3.0.0-rajan.5 build, the existing update route is
Home → Tools → Settings → System → Check for Updates. Minimal/Dashboard use
the Settings front-button label. If that route is inaccessible, this application
image can also be used through the existing SD firmware updater or guarded USB
recovery; publishing it does not install it or contact the device.

- Regular original ESP32-C3 X4 only; not X4 Pro or X4 Classic.
- Source: `b063e220e600340be4a043df152f35a057988a24`.
- Image: 5,671,136 bytes; application slot: 6,553,600 bytes.
- SHA-256: `046ef12122e67a1a3d3852704edace94d7e532d7c13955fba631f6d9ff7fe79d`.
- ELF SHA-256: `275b2b23452786e407e747dced6f85f15b899cb6d5133981ad358eec6c358a81`.

Validation: simulator build; Home → Settings → System → Check for Updates
selection assertions in Lyra, Classic, Three Covers, Carousel and RoundedRaff;
physical-slot keyboard simulation and visual checks in Minimal/Dashboard;
Home with a current book; update action restart into OtaUpdate/WiFi selection;
original-X4 production build and offline image/version/board/ELF validation.
Physical-device installation and acceptance remain pending.

The cached SDK application descriptor retains its earlier project/version/date;
the runtime release version is `3.0.0-rajan.6`. The image and ELF hashes above
identify this candidate. The private updater uses the runtime release version.

All prior Library, reading, Anki and signed-OTA features are retained. This
package contains no bootloader, partition-table write, full-flash image,
private signing key or personal Anki settings. Prior releases remain available.
