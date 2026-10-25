# Musike — AltStore / SideStore source

An **unofficial** [AltStore](https://altstore.io) / [SideStore](https://sidestore.io) source for
[Musike](https://github.com/Ernani1234/musike), the open-source YouTube Music player by
[Ernani1234](https://github.com/Ernani1234).

Upstream publishes unsigned iOS `.ipa` files on its release page but ships no store source, so
this repository serves one: it lets SideStore/AltStore show Musike under **Browse** with
Get/Update instead of re-sideloading each build by hand.

## Add the source

In SideStore (or AltStore) go to **Sources → +** and paste:

```
https://raw.githubusercontent.com/macblizzard/musike-altstore/main/altstore.json
```

Then open **Browse**, pick Musike and tap **Get**.

- Bundle ID: `app.musike.ios` · minimum iOS **15.0**
- Audio only, standalone: the app needs **no server** — it resolves and plays from YouTube
  Music on the device
- Builds are **unsigned**: SideStore/AltStore re-sign them with *your* Apple ID, so the usual
  free-account rules apply (7-day certificate, refreshed automatically by the store; enable
  **Developer Mode** on iOS 16+ the first time)

## Updates

`altstore.json` is regenerated automatically whenever upstream publishes a release that
contains an `*-iOS.ipa` asset, so a new Musike build appears in the store on its own. All
release assets are referenced directly from upstream — nothing is re-hosted here.

## Disclaimer

Not affiliated with or endorsed by Ernani1234, Google, or YouTube. Musike itself is MIT
licensed; see the upstream repository for its source and licence.
