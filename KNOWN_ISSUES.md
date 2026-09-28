# Known Issues

## Open

- **No wind barb on receiving phones running ATAK 5.8.** The phone connected
  to the meter shows the barb, and receiving phones on ATAK 5.6 show it too,
  but receiving phones on ATAK 5.8 show the station with ATAK's default marker
  icon, which can be hidden under the sending phone's own marker. Readings
  still arrive: find the station in Overlay Manager (listed under the station's
  callsign) to see its values.
  - Affects: 0.2 on ATAK 5.8
  - Workaround: on receiving phones, tick **Enabled** beside **Hide Server EUD
    (Client)** so the sending phone's marker does not cover the station.
  - Planned fix: next version.
- **Data Sync feed publishing is not implemented.** The option shows as
  "Data Sync Feed (future release)" and cannot be selected. Readings are shared
  as CoT to your ATAK network instead.
  - Affects: 0.2
  - Planned for a later version.
- **After updating the plugin, ATAK can keep running the old copy.** Dialogs
  such as the meter list may not appear.
  - Affects: all versions (ATAK behavior)
  - Workaround: fully close ATAK and reopen it, then load the plugin.
- **No screenshots in the user guide yet.**
  - Planned for the next version, with a user manual inside ATAK.

- **With no wind direction, the barb points north.** When the meter reports
  no direction (shown as `--`), the barb is drawn pointing up, which looks like
  a north wind. Check the direction in the weather pane.
  - Affects: 0.2
  - Planned fix: next version.

## Fixed

- 0.1 does not load on official ATAK (`ClassNotFoundException`). Fixed in 0.2.
