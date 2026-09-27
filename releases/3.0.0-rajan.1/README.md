# 3.0.0-rajan.1 — original XTEINK X4 test candidate

CrossInk 1.6.0 base with integrated InkPointX-derived features and Rajan Anki/OTA functionality. ESP32-C3 original X4 only; not X4 Pro. Application-only image for the existing x4-dual-ota-v1 layout; no bootloader or partition-table update.

Includes Anki cloze emphasis, paging and Again/Hard/Good/Easy grading; reading history, WPM, daily goals and achievements; native PDF/FB2 conversion and PDF image zoom; timezone detection; optional delayed power-off; and signed private OTA with battery gating and flash readback verification.

Source: b21ea74376ad5f9e4c5c7574d0768eacc6dcd131. Binary: 6,403,904 bytes. SHA-256: eea29ae89dd4c5eb79a21d7f1de6e9b4f20428c117ff0c3a8618cb3382dbb438.

Validation: original-X4 release build and 90 focused host tests passed; image checksum, embedded digest, board tag, runtime version and partition fit verified. Physical boot, UI, SD/Wi-Fi lifecycle and OTA installation remain unverified. Anki media references are preserved, but full card-image/audio playback is not included. Legacy reading statistics/positions import without modifying their source files; not every old setting, bookmark or annotation format is migrated.

Runtime version is 3.0.0-rajan.1. The reused ESP-IDF SDK application descriptor still reports its cached base revision b25beb13-dirty; use the exact binary SHA-256 above to identify this candidate.

Published to the existing test channel only. Publication does not install the firmware. Retain SD backups and the prior firmware before testing or downgrading; older versions may not preserve newly written statistics fields.
