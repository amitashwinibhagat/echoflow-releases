# Echo Flow Releases

Public DMG distribution for Echo Flow (https://echoflow.one).

- Source code stays private in `echo-flow-smart-dictation`.
- Website repo stays private in `echoflow-website`.
- This repo holds **only** GitHub Releases (`.dmg` assets) for Sparkle (`appcast.xml`) and direct download (`/api/download`).

## Current release

- `v1.5.0` — Echo Flow 1.5.0 (build 160)

## Adding a release (maintainer)

```bash
gh release create vX.Y.Z /path/to/EchoFlow-X.Y.Z-BUILD.dmg \
  --repo amitashwinibhagat/echoflow-releases \
  --title "Echo Flow X.Y.Z (BUILD)" \
  --notes-file notes.md
```
