# Trusty Loot Multiplier

Configurable loot, resource, trust, Pet Abyss Gear, Horse Abyss Gear, and DropChance mod for **Crimson Desert v1.05.01**.

Created by **Burstahh**.

## Overview

Trusty Loot Multiplier lets you customize supported Crimson Desert reward sources.

It supports per-category loot quantity multipliers, per-category DropChance controls, ResourceNodes, NPC Trust Gain, Pet Abyss Gear, Horse Abyss Gear, Gear split, Breakables split, and Chests split.

The mod uses active archive scanning, so it can patch the archive the game is actually reading, including supported JSON Mod Manager / pre-modded setups.

## Current Version

**Trusty Loot Multiplier v3.3.3**

Built and tested for **Crimson Desert v1.05.01**.

This is the current recommended ASI build.

v3.3.3 is considered the stable feature-complete build.

Future updates will mainly be compatibility updates if Crimson Desert patches break the mod, or fixes for serious issues if needed.

## Main Features

- Per-category loot quantity multipliers
- Per-category DropChance controls
- ResourceNodes multiplier
- NPC Trust Gain adjustment
- Pet Abyss Gear +10 support
- Horse Abyss Gear +10 support
- Master Trainer’s Touch support
- Gear split for likely non-stacking equipment drops
- Breakables split for jars, pots, barrels, boxes, crates, and clutter
- Chests split for actual chest loot
- Expanded Gathering coverage for flowers, herbs, and botany pickups
- Active archive scanning for supported JSON Mod Manager / pre-modded setups
- Runtime backup and restore on normal game close
- Leftover backup restore on next launch if needed

## DropChance

DropChance raises supported DropSet chance values up to the selected target percent.

DropChance affects how often supported drops happen.

DropChance does not control how many items you receive.

Quantity multipliers and DropChance are separate settings.

In v3.3.3, `[DropChance]` is the master enable / disable section.

Individual DropChance values are controlled under `[CategoryMultipliers]`.

Example:

- `CombatDropChance=5` raises supported combat drops below 5% up to 5%
- `CombatDropChance=25` raises supported combat drops below 25% up to 25%
- `CombatDropChance=100` makes supported combat drops guaranteed where supported
- `GearDropChance=0` keeps likely non-stacking gear DropChance vanilla
- `BreakablesDropChance=0` keeps breakable clutter DropChance vanilla
- `ChestsDropChance=5` controls supported actual chest DropChance separately from Containers and Breakables

High DropChance values can create large loot piles.

For normal gameplay, lower values are recommended.

## ResourceNodes

ResourceNodes are controlled separately from normal loot categories.

This covers supported mining, ore, timber, herbs, wild gathering nodes, and similar direct harvest rewards.

Example:

- `Enabled=1`
- `Multiplier=2`

ResourceNodes affect quantity only.

DropChance category settings do not apply to ResourceNodes.

## Trust, Pet Abyss Gear, and Horse Abyss Gear

NPC Trust Gain can be adjusted from the INI.

Vanilla Trust Gain is `5`.

Pet Abyss Gear support boosts compatible Pet Abyss Gear affection / friendliness effects up to the game capped +10 value.

Horse Abyss Gear support boosts supported Horse EXP gear effects up to the game capped +10 value.

Horse Abyss Gear support includes Equestrian gear and Master Trainer’s Touch.

You still need the correct Abyss Gear or supported gear equipped for these effects to matter.

## Chests, Containers, and Breakables

Chests are separated from normal Containers and Breakables.

- `Chests` controls supported actual chest loot quantity
- `ChestsDropChance` controls supported actual chest DropChance
- `Containers` controls supported non-chest container loot
- `ContainersDropChance` controls supported non-chest container DropChance
- `Breakables` controls supported jars, pots, barrels, boxes, crates, and clutter
- `BreakablesDropChance` controls supported breakable clutter DropChance

This helps reduce loot explosions from breakables while still allowing actual chests to be boosted separately.

## Known Not Covered

v3.3.3 already covers the main reward paths I wanted to support.

Some smaller or more scripted reward paths may still stay vanilla.

Known examples:

- Bugs and insects
- Fish
- Some camp crops
- Some fixed pickups
- Some scripted quest rewards
- Some scripted puzzle rewards
- Some common alchemy pickup paths

Some Abyss rewards are supported, but fixed or scripted Abyss puzzle rewards may stay vanilla.

These are not currently planned unless a future game update or major issue makes more work necessary.

## Installation

Download the latest release ZIP from the GitHub Releases page.

Extract these files into your game folder:

- `TrustyLootMultiplier.asi`
- `TrustyLootMultiplier.ini`

This mod does not include an ASI loader.

If `TrustyLootMultiplier.log` is not created after launching the game, install the Win64 Ultimate ASI Loader as `version.dll` from here:

https://github.com/ThirteenAG/Ultimate-ASI-Loader/releases

Use the Win64 `version.dll` build.

## Important

Do not use the ASI version together with the DMM version or JSON preset version.

Only use one version of Trusty Loot Multiplier at a time.

Using multiple versions together can cause conflicts, duplicated patches, crashes, or broken load order behavior.

## Notes

This mod temporarily patches supported game archives while the game is running.

On normal game close, the mod restores the original files.

If the game crashes before restore completes, remove the ASI and run Steam Verify if needed.

The mod also checks for leftover backups on the next launch and attempts to restore them automatically.
