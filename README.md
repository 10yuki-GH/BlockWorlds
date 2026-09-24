# BLWS

BLWS is a voxel building game for macOS. It was formerly named **BlockWorlds**; that older name is used by Alpha 0.1–0.4 and some legacy files.

## BLWS Alpha 0.5 release status

- DMG released: September 24, 2026
- Windows EXE: in development
- Official release: announced after the Windows EXE is released

## Download and install on macOS

1. Open `index.html` or visit the download website.
2. Select **BLWS Alpha 0.5** and download `BLWS Alpha 0.5.dmg`.
3. Open the DMG and drag `BLWS Alpha 0.5.app` to Applications.
4. Before first launch, open Terminal and run:

```bash
mkdir -p "$HOME/Applications"
ditto --norsrc --noextattr --noqtn --noacl \
  "/Applications/BLWS Alpha 0.5.app" \
  "$HOME/Applications/BLWS Alpha 0.5.app"
open "$HOME/Applications/BLWS Alpha 0.5.app"
```

This makes a clean personal copy and opens it. Run this only for BLWS downloaded from this official repository.

## Older releases

Alpha 0.1–0.4 remain available as BlockWorlds releases. Their original naming and download files are kept for compatibility.

## System requirements

- macOS
- Apple silicon Mac
