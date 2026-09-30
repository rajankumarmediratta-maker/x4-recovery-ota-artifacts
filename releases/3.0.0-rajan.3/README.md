# 3.0.0-rajan.3 — original XTEINK X4 test candidate

Prioritizes a reproduced Anki loading allocation failure. The previous HTTP receive callback grew a std::string; a refused allocation threw std::bad_alloc in the host test and can abort the exception-disabled X4 firmware. This build allocates one bounded response workspace with a fallible allocation, performs no growing allocation in receive callbacks, and reports low memory instead of aborting when the workspace/JSON allocation fails. Opening Anki from Home also releases rebuildable cover/carousel buffers before Wi-Fi and card loading. The exact reported physical crash has not yet been matched to a device log or confirmed repaired on the device.

Adds a visible Filter row in Reading Stats > Books: All, In progress, Finished. An empty result retains the picker, and book details keep the correct original record. The filter uses a bounded index projection; it does not change totals, goals, scheduling or saved book records.

Source commit: 79239f9a35c8184d0cda1421cb9b841a67ff553f
Runtime version: 3.0.0-rajan.3
Image bytes: 5,648,016
OTA slot headroom: 905,584 bytes
SHA-256: 9f9dd89f3de9934a55cb951d9acb2aaeb7fac1b1b0347f378412aea84ba40414

Validation: 52 focused tests passed, including the real Anki client's constrained-allocation, missing-workspace, network-failure and oversized-reply paths. The simulator passes the loading-error/retry/Back flow and the Books-filter picker/empty-result/cancel flow. Original-X4 production build, board/chip identity, runtime version, partition fit and embedded image digest passed.

Application-only image for the original ESP32-C3 X4 and existing x4-dual-ota-v1 layout. English UI/hyphenation; Nearby sharing/sync remains omitted. Anki media references remain text-only. Physical boot, UI, live Anki and OTA installation acceptance remain pending. Keep SD backups before testing or downgrade.

The SDK descriptor still reports its cached base project/revision; the runtime version above and exact binary SHA-256 identify this candidate. The signed manifest is published on the established test OTA channel; the stable channel and previous releases are retained. Publication does not install the image on a device.
