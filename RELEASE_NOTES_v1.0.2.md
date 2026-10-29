Animation scheduling is working again, with a repair option for affected cubes.
You can also choose how many times a face animation plays. Thanks to everyone
who shared device dumps and helped test these fixes.

Install over v1.0.1 to keep your paired cube and app settings.

## Animation scheduling

- **Animation Selection is editable again.** Choose 1–5 animations per time slot.
- Community dumps revealed numeric timing fields missing from schedules written
  by earlier versions. If your cube is affected, **Restore default times** keeps
  your animation selections and repairs the timing. Custom time ranges reset.
- Normal selection saves preserve the schedule's existing timing and other data.
- Tested on V6.4.12: the cube selected the correct local-time slot, and selected
  the next slot after waking across a test boundary. It did not visibly switch
  while idle during that test.

## Choose GIF playback counts

Tap a face in **Face Studio** to preview it and choose a playback count:

- **1–1000:** a set number of plays.
- **0:** unlimited playback.
- **Cancel:** leave the current face unchanged.

Three-play playback was confirmed on the cube. This control applies to Face
Studio; scheduled animation selections remain separate.

## Connection, alarms and clock

- Fixed authentication and device-address discovery races that could cause
  intermittent connection failures.
- Verified saved reconnection with the back closed. Initial setup still needs
  the back open.
- Fixed a one-hour alarm display/save error when an alarm's stored date and the
  current date were in different daylight-saving seasons. The existing firmware
  timezone correction remains enabled; a correctly timed alarm was confirmed.
- Added **System Settings → Cube clock → Open Bluetooth settings**. Connect the
  **earbuds** there to synchronize the cube's clock with the phone. If needed,
  check the phone's date/time/timezone, then disconnect and reconnect the earbuds.
  Connecting only the app does not synchronize the displayed clock.

## Installing

Download **MikuCube-v1.0.2.apk** below and install it over the previous version.
The APK supports arm64-v8a, armeabi-v7a, x86 and x86_64. For automatic updates,
add [this repository](https://github.com/fireinnti/MikuCube-Releases) to Obtainium.

## Known limitations

- Alarms created here may appear shifted in Bilibili because this app corrects
  the firmware's alarm timezone handling.
- Music-to-danmaku support depends on the music app; Spotify and YouTube Music
  do not drive it in the tested setup.
- Device verification used V6.4.12. Behaviour on other firmware may differ.

## Verification

All 26 automated tests, TypeScript checks and the signed release build passed.
Experimental clock probes, alarm sweeps and animation test controls are hidden
in this release.

APK SHA-256:

```text
04244ae9be66ed01b99115df018c91d291604e1d84b60fcab419343631edf1de
```

Signing certificate SHA-256 (unchanged):

```text
12496329e6955991105e1057954ea328198950b06e823fc8415bb30a5d627289
```
