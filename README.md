# AIMDS-Agent Releases

Release artifacts for **Hermes**, the AIMDS-Agent client. This repository
contains no source code, issues or workflows — only GitHub Releases. Source,
development and issue tracking live in the internal `AIMDS-Agent` repository.

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
| `hermes-source-<version>.zip` | Hermes source package (Python CLI, desktop app sources, skills). Root folder `hermes-agent-<version>/`. |
| `hermes-source-<version>.zip.sha256` | SHA-256 checksum (`sha256sum -c` format) |
| `hermes-release.json` | Release manifest: `format`, `version`, `tag`, `commit_sha`, `source_archive`, `sha256`, `size`, `built_at` |
| `install.sh`, `install.ps1` | Install scripts matching this release |
| `HermesSetup.dmg`, `HermesSetup.exe`, `HermesSetup.AppImage`, `HermesSetup.deb`, `HermesSetup.rpm` | Bootstrap installers (`-debug` variants included) |

Download URL scheme:

```
https://github.com/IAMDS-GMBH/AIMDS-Agent-Releases/releases/download/<tag>/<asset>
```

Verify a source package:

```bash
curl -fsSLO https://github.com/IAMDS-GMBH/AIMDS-Agent-Releases/releases/download/v0.7.5/hermes-source-0.7.5.zip
curl -fsSLO https://github.com/IAMDS-GMBH/AIMDS-Agent-Releases/releases/download/v0.7.5/hermes-source-0.7.5.zip.sha256
sha256sum -c hermes-source-0.7.5.zip.sha256
```

Releases are published automatically by the AIMDS-Agent release workflow.
Support: <https://iamds.com>
