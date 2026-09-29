# Changelog

## 0.3 — 2026-09-29

- **Fixed:** the wind barb could disappear on phones receiving a station,
  replaced by ATAK's default icon at a frozen position, until ATAK was
  restarted.
- **Fixed:** a slow Bluetooth link could produce readings stitched together
  from two read cycles, and they were published as live.
- **New:** reconnects to the meter by itself after the link drops (out of
  range, Bluetooth off, meter off); shows "Reconnecting to …". Disconnect ends
  it for good.
- **New:** station labels include wind (`W:5mph SW`). The sender chooses the
  label format, which WinTAK and phones without the plugin also show; each
  receiving phone can show it as sent, use its own format, show the name only,
  or turn labels off, and can rename individual stations.
- **New:** Center on Station button.
- **Changed:** Hide Server EUD (Client) is on by default.
- **Changed:** no wind direction is shown as a circled X instead of a barb
  pointing north; barbs now sit exactly on the station's position.
- **Changed:** new icons that show on light backgrounds (Android, market).

Verified with the tak.gov-signed builds on official ATAK: a Galaxy S24+ on
ATAK 5.8.0.4 connected to a Kestrel 5500FWL and sent readings; a Galaxy S8+ on
5.6.0.12 and a Galaxy S20 Ultra on 5.8.0.5 received them and drew the barb.

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
