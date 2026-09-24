# BLWS

BLWS is a voxel building game for macOS. It was formerly named **BlockWorlds**; that older name is used by Alpha 0.1–0.4 and some legacy files.

## BLWS Alpha 0.5 release status

- DMG released: September 24, 2026
- Windows EXE: in development
- Official release: announced after the Windows EXE is released

## Download and install on macOS

1. Open `index.html` or visit the download website.
2. Select the version you want and drag its App to Applications.
3. Before first launch, open Terminal and run the following. Enter `0.1`, `0.2`, `0.3`, `0.4`, or `0.5` when asked:

```bash
read "VERSION?Enter BLWS/BlockWorlds version (0.1, 0.2, 0.3, 0.4, or 0.5): "
if [ "$VERSION" = "0.5" ]; then APP="BLWS Alpha 0.5.app"; else APP="Alpha $VERSION.app"; fi
mkdir -p "$HOME/Applications"
ditto --norsrc --noextattr --noqtn --noacl \
  "/Applications/$APP" \
  "$HOME/Applications/$APP"
codesign --force --deep --sign - "$HOME/Applications/$APP"
open "$HOME/Applications/$APP"
```

This makes a clean personal copy, applies a local ad-hoc signature, and opens it. Run this only for BLWS downloaded from this official repository.

## Older releases

Alpha 0.1–0.4 remain available as BlockWorlds releases. Their original naming and download files are kept for compatibility.

## System requirements

- macOS
- Apple silicon Mac
