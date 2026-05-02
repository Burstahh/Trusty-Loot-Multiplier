# Trusty Loot Multiplier

Configurable loot multiplier for **Crimson Desert v1.05.00**.

Created by **FlyByDerp aka Burstahh**.

## Features

- Per-category loot multipliers
- 2x to 10x multiplier support
- ResourceNodes multiplier
- NPC Trust Gain adjustment
- Pet Abyss Gear +10 support
- Expanded Gathering coverage for flowers, herbs, and botany pickups
- Active archive scanning
- Automatic backup and restore on normal game close
- Supports normal `bin64` install or `OptiScaler/plugins` install

## Current Version

**Trusty Loot Multiplier v3.2.1**

Built for: **Crimson Desert v1.05.00**

## Installation

1. Download the latest release zip.
2. Extract the files.
3. Place `TrustyLootMultiplier.asi` and `TrustyLootMultiplier.ini` into your game's `bin64` folder.
4. Install an ASI loader if you do not already have one.
5. Launch the game.
6. Check `TrustyLootMultiplier.log` if you need to confirm the mod loaded correctly.

## ASI Loader

This mod requires an ASI loader.

If you need an ASI loader, use the official Ultimate ASI Loader release page (x64 Versions only):

https://github.com/ThirteenAG/Ultimate-ASI-Loader/releases

## Notes

The ASI version temporarily patches supported local game archive data at runtime.
The mod creates backups before patching and restores the original files when the game closes normally.
If the game crashes before restore finishes, remove the ASI and run Steam Verify Integrity.

## Known Not Covered Yet

- Insects
- Fish
- Some camp crops
- Some fixed pickup rewards
- Some common alchemy pickup paths

These may use separate game logic and are still being researched.
