# Known Issues

## Open

- **Data Sync feed publishing is not implemented.** The option shows as
  "Data Sync Feed (future release)" and cannot be selected. Readings are shared
  as CoT to your ATAK network instead.
  - Affects: 0.2, 0.3
  - Planned for 0.4.
- **After updating the plugin, ATAK can keep running the old copy.** Dialogs
  such as the meter list may not appear.
  - Affects: all versions (ATAK behavior)
  - Workaround: fully close ATAK and reopen it, then load the plugin.
- **No screenshots in the user guide yet.**
  - Planned for a later version, with a user manual inside ATAK.
- **Phones still on 0.2 show values twice in the label of a 0.3 station.**
  0.3 sends the formatted label as the station's callsign, and 0.2 adds its
  own temperature and humidity to it.
  - Affects: 0.2 receivers of 0.3 senders
  - Fix: update the receiving phone to 0.3.

## Fixed

- The wind barb could disappear on receiving phones (ATAK's default icon,
  frozen position) until ATAK was restarted. Fixed in 0.3.
- With no wind direction the barb pointed north. 0.3 draws a circled X.
- After a Bluetooth drop the plugin waited for a manual Scan. 0.3 reconnects.
- 0.1 does not load on official ATAK (`ClassNotFoundException`). Fixed in 0.2.
