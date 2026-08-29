<!-- Paste this into the GitHub Release description, then delete this file
     (or keep it — it's small and documents what shipped). -->

First public release. An Android app for the Hatsune Miku CUBEFACE that works
**without the Bilibili app** — no account, no login, no network needed to pair.

## What works

- **Face Studio** — change the cube's face, or upload and crop your own image
- **Wake Alarm** — alarms with repeat days and a scrolling message
- **Danmaku** — custom scrolling messages and reminders
- **System Settings** — read the real firmware version, switch themes
- Face artwork is bundled, so browsing works offline

## Known issues

- **Animation Selection is view-only.** The cube appears to always play the first
  slot (Dawn) rather than picking by the time of day, and we don't yet know why.
  Saving is disabled there so a write can't corrupt your settings.
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

**Open the cube's case before scanning** — it only advertises over Bluetooth
while open. This is the most common reason a scan finds nothing.

For automatic updates, add this repo to
[Obtainium](https://github.com/ImranR98/Obtainium).

## Verifying the download

```
SHA-256 (APK):  c2cca359c6fe29a6371d9b8d3289b1ec46207dab2af370df271d236e53539e9d
```

Signing certificate (stays the same across all future releases):

```
SHA-256:  12496329e6955991105e1057954ea328198950b06e823fc8415bb30a5d627289
```

Check with `apksigner verify --print-certs MikuCube-v1.0.0.apk`. If the
certificate ever differs, the build did not come from this project.

---

Unofficial and not affiliated with bilibili, Crypton Future Media, or the device
manufacturer. Use at your own risk, particularly firmware flashing.
