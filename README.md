# Cineflix Updates (public OTA channel)

This repository is **public on purpose**.

- **Source code** (private):
- **This repo**: GitHub **Releases only** (APK + changelog) so installed apps can check updates without private-repo access.

## How the app checks updates

```text
https://api.github.com/repos/vighnya777/Cineflix-updates/releases/latest
```

Then downloads the `.apk` asset from that release (if present).

## Current target release

| Field | Value |
|-------|--------|
| Latest tag | **v1.3.1** |
| App versionName | 1.3.1 |
| versionCode | 160 |

## Publishing a release (maintainers)

1. Build a **signed** release APK from private `Cineflix-music`.
2. On **this** repo → **Releases** → **New release**:
   - Tag: `v1.3.1` (or next version)
   - Title: `Cineflix v1.3.1`
   - Upload:
     - `Cineflix-v1.3.1-universal-release.apk` (**required** for install)
     - `changelog.json` (optional)
3. Publish as **latest**.
4. Older installs (with OTA URL pointing here) → **Settings → System update** → **Update available**.

## changelog.json format

See `changelog.json` in this repo.
