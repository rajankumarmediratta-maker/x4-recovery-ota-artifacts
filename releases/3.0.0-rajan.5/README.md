# Original XTEINK X4 — 3.0.0-rajan.5

OTA application image for the regular ESP32-C3 X4. Not X4 Pro or X4 Classic.

- Source: `4e6d048c8c631cf581b0ac186d4ab71e842dd2bb`
- Image: 5,671,104 bytes; application slot: 6,553,600 bytes.
- SHA-256: `dd5e60f9850b6b8207d724f90734dc9f7449adc04f4a407b3ea94e6373125624`
- Final ELF SHA-256: `f907386150cfd79546200ec755d7e4754673f4434659fba90630f8dbe6dab5ac`

Library becomes usable during discovery, keeps 24 records in RAM, and pages
through a temporary SD index beyond 150 books. It adds title/author search and
Title/Author/Recent sorting. Unchanged folder browsing reuses its view; file or
reading-data changes refresh it. Anki fetches and grade saves use one owned
worker. Canceling a fetch remains responsive while its current HTTP request
finishes; grades remain serialized and uncertain saves are never blindly retried.
The earlier Ink-inspired Home, nested Tools navigation, button guide, cloze
emphasis, media warnings, reading statistics and signed OTA safeguards remain.

Validation: simulator build and normal smoke test, 26 Anki tests, 200-book
search/paging, Recent-view Author ordering, delayed-fetch cancellation, grade
summary/exit, original-X4 production build, board tag, image checksum/hash,
runtime release version and final ELF digest. Physical-device acceptance pending.

The cached SDK application descriptor still reports `x4-reading-dashboard` /
`ffa98aa4` with its SDK build date. The runtime release version is
`3.0.0-rajan.5`; the checked image and ELF hashes above identify this candidate.
The private updater compares that runtime release version, not the cached SDK
descriptor. English UI/hyphenation are compiled; Nearby remains disabled.

Install through the reader's existing **Check for Updates** flow. This package
does not contain a bootloader, partition-table write, full-flash image, private
signing key or personal Anki settings. Prior release directories remain available.
