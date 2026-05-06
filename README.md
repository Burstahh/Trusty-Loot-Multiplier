# Trusty Loot Multiplier

Configurable loot, resource, trust, Pet Abyss Gear, and DropChance mod for **Crimson Desert v1.05.01**.

Created by **Burstahh**.

## Overview

Trusty Loot Multiplier lets you customize how much loot you receive from supported Crimson Desert reward sources.

It supports per-category loot quantity multipliers, per-category DropChance controls, ResourceNodes, NPC Trust Gain, Pet Abyss Gear affection boost, Gear split, and Breakables split.

The mod uses active archive scanning, so it can patch the archive the game is actually reading, including JSON Mod Manager / pre-modded setups when supported.

## Current Version

**Trusty Loot Multiplier v3.3.2**

Built and tested for **Crimson Desert v1.05.01**.

This is the current recommended ASI build.

## Main Features

- Per-category loot quantity multipliers
- Per-category DropChance controls
- ResourceNodes multiplier
- NPC Trust Gain adjustment
- Pet Abyss Gear +10 support
- Gear split for non-stacking equipment drops
- Breakables split for jars, pots, barrels, crates, and clutter
- Expanded Gathering coverage for flowers, herbs, and botany pickups
- Active archive scanning for JSON Mod Manager / pre-modded setups
- Runtime backup and restore on normal game close
- Leftover backup restore on next launch if needed

## DropChance

DropChance raises supported DropSet chance values up to the selected target percent.

DropChance affects how often supported drops happen, not how many items you receive.

In v3.3.2, `[DropChance]` is the master enable / disable section.

Individual DropChance values are now controlled under `[CategoryMultipliers]`.

Example:

- `CombatDropChance=5` raises supported combat drops below 5% up to 5%
- `CombatDropChance=25` raises supported combat drops below 25% up to 25%
- `CombatDropChance=100` makes supported combat drops guaranteed where supported
- `GearDropChance=0` keeps likely non-stacking gear DropChance vanilla
- `BreakablesDropChance=0` keeps breakable clutter DropChance vanilla

Quantity multipliers and DropChance are separate settings.

## ResourceNodes

ResourceNodes are controlled separately from normal loot categories.

This covers supported mining, ore, timber, herbs, wild gathering nodes, and similar direct harvest rewards.

Example:

- `Enabled=1`
- `Multiplier=2`

ResourceNodes affect quantity only.

DropChance category settings do not apply to ResourceNodes.

## Trust and Pet Abyss Gear

NPC Trust Gain can be adjusted from the INI.

Vanilla Trust Gain is `5`.

Pet Abyss Gear support boosts compatible Pet Abyss Gear affection / friendliness effects up to the game capped +10 value.

You still need the correct Companionship Abyss Gear equipped for the Pet Abyss Gear effect to matter.

## Known Not Covered

These are currently not fully covered:

- Bugs and insects
- Fish
- Some camp crops
- Some fixed pickups
- Some scripted quest rewards
- Some scripted puzzle rewards
- Some common alchemy pickup paths

Some Abyss rewards are supported, but fixed or scripted Abyss puzzle rewards may stay vanilla.

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

The ASI is the recommended version for full INI control.
