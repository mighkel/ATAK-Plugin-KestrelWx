# Kestrel Wx — User Guide

**Download Kestrel Wx 0.3** (pick the one matching your ATAK-CIV version, sideload, then load it in ATAK's Plugins manager):

- **ATAK-CIV 5.6:** https://github.com/mighkel/ATAK-Plugin-KestrelWx/releases/download/v0.3/ATAK-Plugin-KestrelWx-0.3--5.6.0-civ-release.apk
- **ATAK-CIV 5.7:** https://github.com/mighkel/ATAK-Plugin-KestrelWx/releases/download/v0.3/ATAK-Plugin-KestrelWx-0.3--5.7.0-civ-release.apk
- **ATAK-CIV 5.8:** https://github.com/mighkel/ATAK-Plugin-KestrelWx/releases/download/v0.3/ATAK-Plugin-KestrelWx-0.3--5.8.0-civ-release.apk

All releases: https://github.com/mighkel/ATAK-Plugin-KestrelWx/releases

Kestrel Wx reads a Kestrel 5500FWL fire weather meter over Bluetooth, shows
the readings in ATAK, puts a wind-barb station marker on the map, and shares
the readings with everyone else on your ATAK network. Inside ATAK it is listed
as **Kestrel Weather**.

Screenshots will be added in the next version.

## Before you start

- **ATAK-CIV 5.6, 5.7 or 5.8**, installed from tak.gov or the Play Store.
  Builds are published for those three versions only. Install the APK that
  matches your ATAK version. To check it, open ATAK's Settings, then About.
- **The TAK Product Center's own ATAK builds only.** The APKs here are signed
  by the TAK Product Center and will not load on a developer build of ATAK.
- **A Kestrel 5500FWL** for the phone taking readings. Phones that only receive
  readings need no meter.
- **Bluetooth on**, and **location permission** for ATAK. Android requires
  location permission for Bluetooth scanning.

## Install

1. Download the APK for your ATAK version from the links above.
2. Open it on the phone and allow the install. Android may ask you to allow
   installs from your browser or file manager first.
3. Open ATAK. If it asks whether to load the new plugin, tap **Yes**.
   Otherwise open ATAK's **Plugins** manager, find **Kestrel Weather** and
   load it.
4. The Kestrel Weather button appears on ATAK's toolbar.

ATAK's plugin list may say the plugin is **not officially signed**. That is
normal for plugins built through the TAK Product Center's third-party signing
process: they are signed by the TAK Product Center, with the certificate it uses
for plugins it did not write. ATAK has checked the signature before loading it.

**Updating:** install the new APK over the old one, then fully close ATAK
(swipe it away in Android's recent apps) and reopen it before loading the
plugin. ATAK can keep running the old copy until it is restarted.

## Connect the meter

**Do not pair the Kestrel in Android's Bluetooth settings.** The plugin finds
and connects to the meter itself.

1. Turn the meter on and make sure its Bluetooth is on.
2. Open Kestrel Weather from the toolbar and tap **Scan**.
3. A few seconds after the meter is found, a list of meters appears. Pick
   yours.
4. The pane shows **SERVER** and readings start arriving, every few seconds by
   default.

**If the link drops** (the phone moves out of range, Bluetooth is switched off,
the meter is turned off), the pane shows **Reconnecting to** *meter*… and the
plugin reconnects by itself as soon as the meter is back. The station stays on
the map meanwhile. Tap **Stop** to give up waiting.

**Disconnect** ends the connection, and the plugin does not reconnect. If the
meter does not show up in a scan, check its battery and that its Bluetooth is
on, then scan again.

**After changing the meter's battery, recalibrate its compass** (in the
meter's own menu). Until you do, the meter reports no wind direction: the pane
shows `--` and the station's symbol on the map is a circle with an X instead of
a barb.

## Server and client

The plugin picks its role on its own:

- **SERVER**: this phone is connected to a meter. It takes readings and shares
  them.
- **CLIENT**: no meter connected. The phone shows readings shared by others.

Every phone running the plugin shows the other stations on its map, with a
wind barb.

**Hide Server EUD (Client)** is on by default: on a phone without a meter, it
hides the marker of the phone that owns the meter, so only the weather station
is shown at that spot. Untick **Enabled** beside it to show both.

**Center on Station** moves the map to the station shown in the pane: your own
meter when connected, otherwise the station you are receiving.

### Station labels

Each station is labelled on the map, by default like
`Kestrel-WX T:72°F RH:23% W:5mph SW`.

- **Label Format (sent)** (on the phone with the meter): the label this station
  sends. Build it from `{name}`, `{temp}`, `{rh}`, `{wind}` and `{dir}`; a
  value with no reading is left out along with its prefix. Phones and WinTAK
  without the plugin show this label too.
- **Station Labels (this phone)**: **As sent by each station** (default),
  **Name only**, **Custom format** (your own format, same tokens, for every
  station), or **Off** (no text on the map).
- **Rename on this phone**: in a station's detail view (tap the station, then
  the detail button). Gives that station a shorter name on this phone only;
  leave it empty to go back to the sender's name.

## Sharing readings

Under **Sharing**:

- **Auto-send on Connect** (default): every reading is sent to your ATAK
  network while a meter is connected.
- **Manual Only**: nothing is sent until you tap **Share Weather Now**.
- **Data Sync Feed (future release)**: shown greyed out. Publishing to a TAK
  Server Data Sync feed is planned for a later version.

Readings go wherever ATAK's own traffic goes: to your TAK Server if you are
connected to one, and to other phones on the same local network. The plugin
makes no connections of its own.

**CoT Stale Time (min)** sets how long a shared reading stays on other
phones' maps without an update.

## Station settings

- **Callsign**: the name the station is shared under.
- **Label Format (sent)**: see *Station labels* above.
- **Poll Interval**: how often the plugin reads the meter.

## The weather pane

The pane shows temperature (**TEMP**), relative humidity (**RH**) and **WIND**
in large type, then **Pressure**, **Dewpoint**, **Heat Index**, **Wind Chill**,
**WBGT**, **Altitude** and the meter's **Battery**.

Tap a station marker on the map to open the radial menu. From there you can
open the full detail view for that station.

## Weather trend

**Weather Trend** charts temperature, relative humidity or wind speed over
the last 1, 4, 8 or 12 hours, or the operational period.

## Trigger points

Trigger points alert you when a value crosses a limit. For example, relative
humidity dropping below 15%, or wind rising above a speed. They run on client
phones and watch readings as they arrive.

1. Under **Trigger Points**, tap **+ Add**.
2. Give it a name, then pick the value (temperature, relative humidity, wind
   speed, dewpoint, heat index or WBGT) and the condition.
3. Enter the threshold. Conditions are greater or less than a value, or a
   rate: the value rising or falling by more than the threshold within the
   time window you set.

Tick **Enabled** beside **Trigger Notifications** to get an Android
notification when a trigger fires. A temporary alert icon is also shown on the station's marker.

## Getting help

Open an issue at [github.com/mighkel/ATAK-Plugin-KestrelWx/issues](https://github.com/mighkel/ATAK-Plugin-KestrelWx/issues).
Include your ATAK version, Android version, phone model and the plugin version.
The plugin version is shown in ATAK's Plugins manager.
