ATAK Plugin — Kestrel Wx

**Download Kestrel Wx 0.2** (pick the one matching your ATAK-CIV version, sideload, then load it in ATAK's Plugins manager):

- **ATAK-CIV 5.6:** https://github.com/mighkel/ATAK-Plugin-KestrelWx/releases/download/v0.2/ATAK-Plugin-KestrelWx-0.2--5.6.0-civ-release.apk
- **ATAK-CIV 5.7:** https://github.com/mighkel/ATAK-Plugin-KestrelWx/releases/download/v0.2/ATAK-Plugin-KestrelWx-0.2--5.7.0-civ-release.apk
- **ATAK-CIV 5.8:** https://github.com/mighkel/ATAK-Plugin-KestrelWx/releases/download/v0.2/ATAK-Plugin-KestrelWx-0.2--5.8.0-civ-release.apk

All releases: https://github.com/mighkel/ATAK-Plugin-KestrelWx/releases

**User guide: [docs/USER_GUIDE.md](docs/USER_GUIDE.md)**
(https://github.com/mighkel/ATAK-Plugin-KestrelWx/blob/main/docs/USER_GUIDE.md)

_________________________________________________________________
PURPOSE AND CAPABILITIES

Kestrel Wx puts live readings from a Kestrel 5500FWL fire weather meter on the
ATAK map and shares them with the team, for wildland fire crews taking spot
weather. Without it, readings are copied off the meter's screen and passed by
voice. Inside ATAK the plugin is listed as "Kestrel Weather".

Capabilities:

  - Scan for and connect to the meter over Bluetooth LE from inside ATAK. No
    pairing in Android's Bluetooth settings.
  - Live weather pane: temperature, relative humidity, wind speed and
    direction, pressure, dewpoint and the other values the meter reports.
  - A station marker with a wind barb at the observer's position.
  - Readings shared to the team as CoT, and stations shared by other Kestrel
    Wx users shown on your map.
  - Trend history, and trigger points that alert when a value crosses a
    threshold (for example, relative humidity dropping below a limit).

_________________________________________________________________
STATUS

Version 0.2: the first release that loads on official ATAK. Version 0.1 was
signed but never loaded; see CHANGELOG.md.

Verified on official ATAK with a Kestrel 5500FWL: the 5.6 build on Play Store
ATAK 5.6.0.12 (Galaxy S8+) connects to the meter and shares readings, and the
5.8 build on ATAK 5.8.0.4 (Galaxy S24+) receives them.

Data Sync feed publishing is not implemented yet and shows as "future release"
in the plugin.

_________________________________________________________________
POINT OF CONTACTS

Mike Underwood
https://github.com/mighkel/ATAK-Plugin-KestrelWx/issues

_________________________________________________________________
PORTS REQUIRED

(This is important for ATO, networking, and other security concerns)

  None. The plugin opens no sockets, listens on no ports and makes no HTTP
  requests. It talks to the meter over Bluetooth LE only.

  Shared readings are handed to ATAK and travel over whatever connections
  ATAK already has (TAK Server, local network). The plugin adds no
  connection of its own. With no network, the meter, pane, marker, history
  and triggers still work; sharing waits for ATAK to have a connection.
  Works in airplane mode with Bluetooth on.

_________________________________________________________________
EQUIPMENT REQUIRED

  Android device supported by ATAK-CIV 5.6, 5.7 or 5.8, with Bluetooth LE.
  A Kestrel 5500FWL (Fire Weather with LiNK) meter on the phone that takes
  readings. Phones that only receive shared readings need no meter.

_________________________________________________________________
EQUIPMENT SUPPORTED

  Kestrel 5500FWL. Other Kestrel LiNK meters may work but have not been
  tested.

_________________________________________________________________
COMPILATION

  Not applicable to this repository. The plugin's source is private under a
  non-disclosure agreement with Nielsen-Kellerman. Builds published here are
  compiled and signed by the TAK Product Center's third-party pipeline.

_________________________________________________________________
DEVELOPER NOTES

  - Releases, the user guide and issue tracking live here. Report problems
    with the Issues tab.
  - One APK per ATAK version. Install the one that matches your ATAK; a build
    for another version installs but ATAK will not load it.
  - Every release carries a higher version code on every ATAK version, so an
    MDM or the TAKwerx Market can push it as an update.

_________________________________________________________________
LICENSE

  The signed builds published here are free to install and use. The plugin's
  source is not published. Kestrel, Kestrel LiNK and Nielsen-Kellerman are
  trademarks of Nielsen-Kellerman Co. This project is not affiliated with or
  endorsed by the TAK Product Center.
