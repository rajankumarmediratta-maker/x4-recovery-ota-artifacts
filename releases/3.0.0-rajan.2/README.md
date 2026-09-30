# 3.0.0-rajan.2 — original XTEINK X4 test candidate

Original ESP32-C3 X4 application firmware for the existing x4-dual-ota-v1 layout. This release includes the Claude features reintegrated onto the CrossInk 1.6.0/Rajan base and subsequent correctness repairs.

Includes the Today/Week/Month/Year/Books/Habits dashboard, 14 achievement tracks with levels, adjustable daily reminders and a yearly books goal, Anki deck selection/undo/session summaries, and sharper vector PDF zoom through 300%.

Anki answer-side controls: Confirm = Good, hold Confirm = Easy, Left = Again, Right = Hard; Back returns to the question. Undo holds one grade until the next grade or session end. Desktop Anki remains authoritative; uncertain network replies are not blindly retried. Pictures/audio in Anki cards remain references only.

Repairs: dashboard index processing stays within its 150-candidate budget; PDF zoom rasterization requires a durable attempt marker; pending Anki grades flush in order on exit; confirmed-review counters update under the render lock. The original-X4 profile uses English UI/hyphenation and omits Nearby reader-to-reader sharing and sync.

Source branch: feat/x4-claude-reintegrated
Source commit: 27b3f70fbc894fdd0d603ad03025ea2bb7cb2afd
Runtime version: 3.0.0-rajan.2
Image bytes: 5,646,592
OTA slot headroom: 907,008 bytes
SHA-256: d34d12d69e7b2593a5a9ca2e39d5799eab025585cbbdf1b4aa18e8bfbd334672

Validated by the original-X4 production build, 84 focused host tests, simulator build/smoke, image checksum/digest, board tag, runtime version and partition-size checks. Physical boot/UI and live Anki/OTA acceptance remain pending. Keep SD backups before installing or downgrading; older builds may not preserve newer statistics/goal/achievement fields. Not all old settings/bookmarks/annotations have migration support.

The reused ESP-IDF SDK descriptor shows its cached base project x4-reading-dashboard and revision ffa98aa4; the runtime version is 3.0.0-rajan.2. Identify this exact image by the SHA-256 above.

The signed manifest is published on the existing test OTA channel. Firmware URLs pin an immutable artifact commit. Stable channel and previous releases are retained. Publication does not install the firmware on a device.
