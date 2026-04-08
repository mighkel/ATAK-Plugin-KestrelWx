# Changelog

## v0.1.0 — 2026-04-08

First signed release. Pre-alpha. Suitable for initial self-testing and trusted-collaborator review.
Not yet ready for broad distribution.

### Features

- BLE scan and connect to a single Kestrel weather device.
- Live weather panel inside ATAK showing temperature, relative humidity, wind speed, wind direction, and derived fire-weather values.
- Wind barb map icon rendered at the sensor location with a concise T/RH label.
- Auto-detection of Server+Client mode (Kestrel connected) and Client-only mode (no Kestrel).
- CoT generation and transmission of sensor telemetry over TAK Server.
- Data Sync mission publish/subscribe workflow for sharing weather with other EUDs.
- Receive and display remote Kestrel station data on client EUDs.
- Trend charts for temperature, relative humidity, and wind over the operational period.
- Configurable trigger points with optional notifications and temporary alert icon overlay.
- Optional suppression of the server EUD marker on client EUDs.
- Battery indicator for the connected Kestrel device.
- Radial menu integration for quick access to the full weather detail view from any station marker.

### Known Limitations

- Single Kestrel device only. Multi-sensor support is a non-goal for this release.
- Field validation of Data Sync mission setup and group/channel UX is ongoing.
- See `KNOWN_ISSUES.md` for device-specific and network-condition notes.

### Requirements

- ATAK CIV 5.6.0 or compatible.
- Android device with Bluetooth LE.
- TAK Server reachable from all EUDs for network sharing features.
