# Cineflix Updates (public OTA channel)

This repository is **public on purpose**.

- **Source code** lives in the private repo: [vighnya777/Cineflix-music](https://github.com/vighnya777/Cineflix-music)
- **This repo** only publishes **GitHub Releases** (APK + changelog) so installed apps can check for updates without accessing the private source.

## How the app checks updates

Cineflix calls:

```text
https://api.github.com/repos/vighnya777/Cineflix-updates/releases/latest
```

Then downloads the `.apk` asset from that release.

## Publishing a new version (maintainers)

1. Build a **signed** release APK from the private `Cineflix-music` repo (CI or local).
2. Create a **Release** on **this** repo (`Cineflix-updates`):
   - Tag: `v1.2.6` (must match app `versionName`, with optional `v` prefix)
   - Title: `Cineflix v1.2.6`
   - Upload:
     - `Cineflix-v1.2.6-universal-release.apk` (required)
     - `changelog.json` (optional but recommended)
3. Mark the release as **latest**.
4. On an older install: **Settings → System update** → should show **Update available**.

## changelog.json format

```json
{
  "description": "Short summary",
  "image": "",
  "changelog": [
    {
      "title": "What's New",
      "items": ["Feature A", "Feature B"]
    },
    {
      "title": "Fixes",
      "items": ["Bug fix"]
    }
  ]
}
```

## Privacy

Do **not** push full app source here. Only release assets and this README.
