# Changelog

## 0.2 — 2026-09-27

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

Verified with the tak.gov-signed builds on official ATAK: the 5.6 build on
Play Store ATAK 5.6.0.12 (Galaxy S8+) connects to a Kestrel 5500FWL and shares
readings; the 5.8 build on ATAK 5.8.0.4 (Galaxy S24+) receives them.

## 0.1 — 2026-04-08 (does not work)

Signed by tak.gov, but it does not load on official ATAK (fixed in 0.2).
It was never published as a GitHub Release. Do not install it.
