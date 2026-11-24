# AIMDS Agent Releases

Downloads for **AIMDS Agent**, the AI assistant of the AIMDS Suite by IAMDS GmbH.
Up to version 0.7.17 the app was called "Hermes".

This repository holds releases only, with no source code, issues or discussions.

## Install

Download the installer for your computer from the
[latest release](https://github.com/IAMDS-GMBH/AIMDS-Agent-Releases/releases/latest):

| Computer | File | How |
|---|---|---|
| macOS 13 (Ventura) or newer | `HermesSetup.dmg` | Open the file, drag "AIMDS Agent" into Applications and start it from there. |
| Windows 10/11 (64-bit) | `HermesSetup.exe` | Double-click the file. |
| Linux (64-bit) | `HermesSetup.AppImage`, `HermesSetup.deb` or `HermesSetup.rpm` | Make the AppImage executable and start it, or install the package with your package manager. Setup builds the app on your computer, which takes a few minutes longer. |

During setup you enter your company's AIMDS Suite address and sign in with your
IAMDS account. IAMDS gives you the Suite address once your company's AIMDS Suite
is set up.

After that the app offers updates itself, so you never need to download anything
here again. To remove the app, open Settings → About in the app. From 0.8.0 on,
Windows also lists it under Settings → Apps.

## Channels

| Tag | Channel | GitHub Release |
|---|---|---|
| `vX.Y.Z` | `stable` | latest, not a pre-release |
| `vX.Y.Z-rc.N` | `preview` | pre-release |

The stable channel resolves via `releases/latest`; the preview channel takes
the highest release including candidates.

## Assets per release

| Asset | Purpose |
|---|---|
| `HermesSetup.dmg`, `HermesSetup.exe`, `HermesSetup.AppImage`, `HermesSetup.deb`, `HermesSetup.rpm` | Installers for the first installation |
| `HermesSetup-debug.dmg`, `HermesSetup-debug.exe` | Debug builds of the installers, for support |
| `HermesSetup.dmg.sha256`, `HermesSetup.exe.sha256`, `HermesSetup.AppImage.sha256` | SHA-256 checksums of the installers |
| `AIMDS-Agent-<version>-mac-arm64.zip`, `AIMDS-Agent-<version>-win-x64.zip` (each with `.sha256`) | The prebuilt desktop app the in-app update installs. Up to 0.7.17 these were named `Hermes-<version>-…`. |
| `hermes-source-<version>.zip` (with `.sha256`) | Agent package: Python agent, desktop app sources and skills. Root folder `hermes-agent-<version>/`. |
| `hermes-release.json` | Release manifest: version, tag, commit, checksum and size of the agent package, build time, release notes, desktop app and installer entries |

Download URL scheme:

```
https://github.com/IAMDS-GMBH/AIMDS-Agent-Releases/releases/download/<tag>/<asset>
```

Verify a download, for example the agent package:

```bash
curl -fsSLO https://github.com/IAMDS-GMBH/AIMDS-Agent-Releases/releases/download/v0.7.17/hermes-source-0.7.17.zip
curl -fsSLO https://github.com/IAMDS-GMBH/AIMDS-Agent-Releases/releases/download/v0.7.17/hermes-source-0.7.17.zip.sha256
shasum -a 256 -c hermes-source-0.7.17.zip.sha256   # Linux: sha256sum -c
```

Releases are published automatically by the AIMDS Agent release workflow.

© 2026 IAMDS GmbH. AIMDS Agent is based on Hermes Agent by Nous Research (MIT).
Support: <https://iamds.com>
