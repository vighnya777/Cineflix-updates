# Cineflix Updates (public OTA channel)

This repository is **public on purpose**.

- **Source code** (private): https://github.com/vighnya777/Cineflix-music
- **This repo**: GitHub **Releases only** (APK + changelog) so installed apps can check updates without private-repo access.

## How the app checks updates

```text
https://api.github.com/repos/vighnya777/Cineflix-updates/releases/latest
```

Then downloads the `.apk` asset from that release (if present).

## Current target release

| Field | Value |
|-------|--------|
| Latest tag | **v1.2.7** |
| App versionName | 1.2.7 |
| versionCode | 157 |

## Publishing a release (maintainers)

1. Build a **signed** release APK from private `Cineflix-music`.
2. On **this** repo → **Releases** → **New release**:
   - Tag: `v1.2.7` (or next version)
   - Title: `Cineflix v1.2.7`
   - Upload:
     - `Cineflix-v1.2.7-universal-release.apk` (**required** for install)
     - `changelog.json` (optional)
3. Publish as **latest**.
4. Older installs (with OTA URL pointing here) → **Settings → System update** → **Update available**.

## changelog.json format

See `changelog.json` in this repo.

## Privacy

Do **not** push full app source here. Only release assets and docs.
