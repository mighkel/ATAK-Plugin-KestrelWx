# Changelog

## 0.2 — unreleased (submitted to tak.gov 2026-09-27)

The first version that loads on official ATAK.

- **Fixed:** 0.1 failed to load on official ATAK-CIV with
  `ClassNotFoundException: gov.tak.api.plugin.IServiceController`. The release
  build did not apply ATAK's class-name mapping; it does now.
- **New:** builds for ATAK-CIV 5.6, 5.7 and 5.8. Install the one matching your
  ATAK.
- **New:** each build carries its own rising version code, so an MDM or the
  TAKwerx Market can push it as an update.
- **Changed:** sharing defaults to **Auto-send on Connect**. The Data Sync
  option is shown greyed out as a future release: in 0.1 it only uploaded a
  one-time data package to the TAK Server and never published to a Data Sync
  feed. Anyone with Data Sync selected is moved to Auto-send.
- **Fixed:** sharing to the TAK Server failed with "Unable to create the …
  directory" when a feed ID was set.

Tested with a Kestrel 5500FWL on ATAK-CIV 5.6: meter connection, live
readings, the station marker, and sharing between two phones.

## 0.1 — 2026-04-08 (does not work)

Signed by tak.gov, but it does not load on official ATAK (fixed in 0.2).
It was never published as a GitHub Release. Do not install it.
