# Oxo Tracker Releases

This repository is the official binary distribution channel for [Oxo Tracker](https://github.com/Oxo-AI-Security/Oxo-Tracker).

## Downloads

Download installers from the [Releases](https://github.com/Oxo-AI-Security/Oxo-Tracker-Releases/releases) page. Large binaries are stored as GitHub Release assets and are not committed to Git history.

Each Windows release should include:

- the x64 NSIS installer;
- its Tauri updater signature (`.sig`);
- its SHA-256 checksum (`.sha256`);
- updater metadata (`latest.json`);
- release notes, build information, an SPDX SBOM, and third-party notices.

Preview builds are marked as **Pre-release**. A build should only be marked stable after Windows Authenticode signing and release validation are configured.

## Verify a download

```powershell
Get-FileHash .\Oxo-Tracker_0.2.0_x64-setup.exe -Algorithm SHA256
Get-Content .\Oxo-Tracker_0.2.0_x64-setup.exe.sha256
```

The two SHA-256 values must match. The application updater separately verifies the `.sig` value embedded in the published update manifest.

## Security

Updater private keys and credentials must never be stored in this repository. Report security issues through the contact process in the source repository rather than a public issue containing sensitive details.
