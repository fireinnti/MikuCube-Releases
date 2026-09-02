<!-- Paste this into the GitHub Release description, then delete this file
     (or keep it — it's small and documents what shipped). -->

Mostly about the two things people kept getting stuck on: the cube not turning up
in the phone's Bluetooth settings, and never being sure whether a screen was
showing the cube's settings or an old copy of them.

Installing over v1.0.0 keeps your paired cube and everything you've set.

## Pairing now pairs with the phone too

Picking your cube in the app adds it to Android's own Bluetooth devices, so the
earbuds work as an audio device without a separate trip through system settings.
Confirm the pairing prompt when it appears.

Everything in the app still works without it — if the pairing fails or you
dismiss it, the connect screen has **Add to Bluetooth** and a shortcut to the
system settings.

## Nothing to save, nothing to sync

- Opening **Alarms**, **Animation Selection** or **System Settings** reads that
  screen off the cube for you. A line at the top says whether you're looking at
  the cube's settings or your saved copy, with a **Refresh** for when you've
  changed something in the Bilibili app since.
- **Danmaku saves itself** a moment after you stop editing, the way alarms
  always have. The Save button is gone; the header just tells you where your
  edits stand. Edits made while disconnected go out as soon as the cube is back.

## Also new

- **Wake Alarm → Use next alarm from Clock** fills in the time from your phone's
  own next alarm, so you don't have to retype it.
- **Press and hold your custom image** in Face Studio to remove it.
- The scan screen now says up front that the cube has to be **turned on with its
  back open**, which is far and away the most common reason a scan finds nothing.

## Fixed

- **Two faces showed the wrong artwork.** *Slacking Off* (摸鱼) and *Fully
  Charged* (充电完毕) were displaying images belonging to two other faces
  entirely. Both now show the real thing — 摸鱼 is the fish, 充电完毕 is the
  sunglasses.

## Still known issues

- **Animation Selection is view-only.** Unchanged from v1.0.0 — the cube appears
  to always play the first slot (Dawn) rather than picking by the time of day,
  so saving stays disabled there until we understand why. You can view what's
  assigned, and it now loads from the cube automatically.
  **If your cube is new or you've only used the Bilibili app, please
  [share your device data](../../#-can-you-help-share-your-cubes-data)** — it
  would help a lot.
- **"Scroll lyrics while music plays"** only works with certain music apps.
  Spotify and YouTube Music don't drive it.
- Alarms are automatically corrected for a firmware timezone bug, so they ring
  when you set them. Side effect: they look shifted if viewed in the Bilibili app.

## Installing

Download the APK below and open it. Android will warn that the source isn't
trusted — allow your browser to install unknown apps. Play Protect may say the
app is unrecognised; that's expected for anything outside the Play Store.

**Open the back of the cube before scanning** — it only advertises over
Bluetooth while the back is open.

For automatic updates, add this repo to
[Obtainium](https://github.com/ImranR98/Obtainium).

## Verifying the download

```
SHA-256 (APK):  <fill in from the built APK>
```

Signing certificate (unchanged since v1.0.0):

```
SHA-256:  12496329e6955991105e1057954ea328198950b06e823fc8415bb30a5d627289
```

Check with `apksigner verify --print-certs MikuCube-v1.0.1.apk`. If the
certificate ever differs, the build did not come from this project.

---

Unofficial and not affiliated with bilibili, Crypton Future Media, or the device
manufacturer. Use at your own risk, particularly firmware flashing.
