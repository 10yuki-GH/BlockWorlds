# BlockWorlds

BlockWorlds is a voxel building game for macOS. Explore generated worlds, collect building items, and create structures with blocks, pine materials, plants, stairs, doors, sand, and water.

## Release dates

- DMG release: September 3, 2026
- Official release: September 6, 2026

## Available versions

### Alpha 0.4

The latest release. It introduces infinite worlds, Flat and Normal world types, oceans, water, sand, sandstone, biome information, coordinates, and streamed chunk generation.

### Alpha 0.3

Adds world seeds, Plains and Forest biomes, pine trees, improved stairs, faster movement, and a more complete building experience.

### Alpha 0.2

Adds pine wood building materials, plants, doors, saplings, bone meal, flowerpots, and pine needle decay.

### Alpha 0.1

The first Alpha release, featuring the original BlockWorlds building experience.

## Download and install

1. Open `index.html` or visit the BlockWorlds download website.
2. Choose a version and download its DMG.
3. Open the DMG.
4. Double-click the included App ZIP.
5. Move the extracted app to the macOS Applications folder.
6. Before the first launch, complete the required terminal fix below.

The extracted application keeps the matching version name, such as `Alpha 0.4.app`.

## Required first-launch fix for all versions

This fix applies to every BlockWorlds release: Alpha 0.1, Alpha 0.2, Alpha 0.3, and Alpha 0.4.

BlockWorlds Alpha is distributed outside the Mac App Store and is not notarized by Apple. The downloaded app may not open until this fix is completed. After moving the app to `/Applications`, open Terminal, paste the entire command below, and enter the downloaded version number when asked.

```bash
read "VERSION?Enter BlockWorlds version (0.1, 0.2, 0.3, or 0.4): "
mkdir -p "$HOME/Applications"
ditto --norsrc --noextattr --noqtn --noacl \
  "/Applications/Alpha ${VERSION}.app" \
  "$HOME/Applications/Alpha ${VERSION}.app"
open "$HOME/Applications/Alpha ${VERSION}.app"
```

For example, enter `0.1` for Alpha 0.1 or `0.4` for Alpha 0.4. The command creates a launchable copy in your personal Applications folder and opens it. Do not use `sudo xattr`; on some Macs it fails with `Operation not permitted`.

If the app still does not open, verify the copied app with:

```bash
read "VERSION?Enter BlockWorlds version (0.1, 0.2, 0.3, or 0.4): "
exe="$(plutil -extract CFBundleExecutable raw "$HOME/Applications/Alpha ${VERSION}.app/Contents/Info.plist")"
test -x "$HOME/Applications/Alpha ${VERSION}.app/Contents/MacOS/$exe"
codesign --verify --deep --strict --verbose=2 "$HOME/Applications/Alpha ${VERSION}.app"
```

Only use these commands for BlockWorlds downloaded from the official repository.

## System requirements

- macOS
- Apple silicon Mac
