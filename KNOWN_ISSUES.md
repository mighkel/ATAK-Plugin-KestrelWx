# Known Issues

## Open

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

## Fixed

- 0.1 does not load on official ATAK (`ClassNotFoundException`). Fixed in 0.2.
