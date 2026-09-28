# Known Issues

## Open

- **The wind barb can disappear on phones that receive a station.** The
  station then shows with ATAK's default marker icon, may stop moving, and can
  be hidden under the sending phone's own marker. Readings still arrive (the
  station's values in its detail view keep updating).
  - Affects: 0.2, any ATAK version
  - Workaround: fully close ATAK (swipe it away in Android's recent apps) and
    reopen it. The barb comes back. Old copies of the station fade out once
    they go stale. Ticking **Enabled** beside **Hide Server EUD (Client)** keeps
    the sending phone's marker from covering the station.
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
