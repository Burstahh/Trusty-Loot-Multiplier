# Trusty Loot Multiplier

Configurable loot, resource, trust, Pet Gear, Horse Gear, and DropChance ASI mod for **Crimson Desert v1.06.00**.

Created by **Burstahh**.

## Overview

Trusty Loot Multiplier lets you customize supported Crimson Desert reward sources.

It supports per-category loot quantity multipliers, per-category DropChance controls, ResourceNodes, NPC Trust Gain, Pet Abyss Gear, Horse Abyss Gear, Gear split, Breakables split, Chests split, Containers split, TradeGoods split, and v3.4 category cleanup logic.

The ASI version uses active archive scanning, so it can patch the archive the game is actually reading, including supported pre-modded / overlay setups.

## Current Version

**Trusty Loot Multiplier v3.4.0**

Built and tested for **Crimson Desert v1.06.00**.

This is the current recommended ASI build.

The ASI version is the main supported version going forward.

## Main Features

- Per-category loot quantity multipliers
- Per-category DropChance controls
- ResourceNodes multiplier
- NPC Trust Gain adjustment
- Pet Abyss Gear / Pet Trust Gear +10 support
- Horse Abyss Gear / Horse EXP Gear +10 support
- Master Trainer’s Touch support
- Supported riding gear Horse EXP +10 support
- Gear split for likely non-stacking equipment drops
- Breakables split for jars, pots, barrels, boxes, crates, and clutter
- Chests split for actual chest loot
- Containers split for supported non-chest container loot
- TradeGoods split for trade-good-style rewards
- Furniture/Housing safety
- Provision/Goods clutter safety
- Unique/Special reward safety
- Expanded Gathering coverage for flowers, herbs, and botany pickups
- Active archive scanning for supported pre-modded / overlay setups
- Runtime backup and restore on normal game close
- Leftover backup restore on next launch if needed

## DropChance

DropChance raises supported DropSet chance values up to the selected target percent.

DropChance affects how often supported drops happen.

DropChance does not control how many items you receive.

Quantity multipliers and DropChance are separate settings.

`[DropChance]` is the master enable / disable section.

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

## Trust, Pet Gear, and Horse Gear

NPC Trust Gain can be adjusted from the INI.

Vanilla Trust Gain is `5`.

Pet Abyss Gear / Pet Trust Gear support boosts compatible Pet affection / friendliness effects up to the game capped +10 value.

Horse Abyss Gear / Horse EXP Gear support boosts supported Horse EXP gear effects up to the game capped +10 value.

Horse Gear support includes supported Abyss Gear, Equestrian gear, Master Trainer’s Touch, and supported riding gear that already has Horse EXP Gain on it.

You still need the correct Abyss Gear or supported gear equipped for these effects to matter.

## Chests, Containers, Breakables, and TradeGoods

v3.4.0 expands category cleanup so different reward sources can be controlled more safely.

Chests are separated from normal Containers and Breakables.

- `Chests` controls supported actual chest loot quantity
- `ChestsDropChance` controls supported actual chest DropChance
- `Containers` controls supported non-chest container loot
- `ContainersDropChance` controls supported non-chest container DropChance
- `Breakables` controls supported jars, pots, barrels, boxes, crates, and clutter
- `BreakablesDropChance` controls supported breakable clutter DropChance
- `TradeGoods` controls supported trade-good-style rewards
- `TradeGoodsDropChance` controls supported trade-good-style DropChance

This helps reduce accidental loot explosions from breakables while still allowing actual chests and supported rewards to be boosted separately.

## Category Cleanup and Safety

v3.4.0 adds updated category cleanup logic.

The goal is not to nerf loot. The goal is to route rewards into safer categories so users can control what gets boosted.

Safety cleanup includes:

- Furniture/Housing rewards stay vanilla to avoid permanent housing/deco reward issues
- Provision/Goods clutter rewards stay vanilla where needed
- Unique/Special rewards stay vanilla where needed
- Keys, maps, quest documents, recipes/manuals, and similar special rewards stay protected
- Gear is separated from normal stackable loot
- Breakable-source rewards stay controlled by Breakables where possible
- Chests and non-chest containers are separated

## ALL TEH Loot

ALL TEH Loot is the chaos preset.

It is intentionally aggressive.

However, the v3.4.0 ALL TEH Loot logic still keeps important furniture/provision/unique safety fixes in place. This is to avoid breaking permanent housing/deco rewards or other special reward paths.

Use ALL TEH Loot at your own risk.

## Known Not Covered

v3.4.0 covers the main reward paths I wanted to support.

Some smaller or more scripted reward paths may still stay vanilla.

Known examples:

- Bugs and insects
- Fish
- Bait or unknown bait-related paths
- Some camp crops, such as Abyss Trees / Apple Trees
- Some fixed pickups
- Some scripted quest rewards
- Some scripted puzzle rewards
- Some common alchemy pickup paths
- Some fixed/scripted/skill-menu/level-up/puzzle/counter-style Abyss reward paths

AbyssRewards means supported Abyss/AbyssGear DropSet reward paths, not every scripted Abyss Artifact or special Abyss reward path.

Additional niche coverage is not currently planned unless a future game update or serious issue makes more work necessary.

## Installation

Download the latest release ZIP from the GitHub Releases page.

Extract these files into your game folder:

- `TrustyLootMultiplier.asi`
- `TrustyLootMultiplier.ini`

This mod does not include an ASI loader.

If `TrustyLootMultiplier.log` is not created after launching the game, install the Win64 Ultimate ASI Loader as `version.dll` from here:

https://github.com/ThirteenAG/Ultimate-ASI-Loader/releases

Use the Win64 `version.dll` build if possible.

## Important

Only use one version of Trusty Loot Multiplier at a time.

Using multiple versions together can cause conflicts, duplicated patches, crashes, broken load order behavior, or confusing results.

## Notes

This mod temporarily patches supported game archives while the game is running.

On normal game close, the mod restores the original files.

If the game crashes before restore completes, remove the ASI and run Steam Verify if needed.

The mod also checks for leftover backups on the next launch and attempts to restore them automatically.
