# Trusty Loot Multiplier

Configurable loot, resource, trust, Pet Abyss Gear, and DropChance mod for **Crimson Desert v1.05.01**.

Created by **Burstahh**.

## Overview

Trusty Loot Multiplier lets you customize how much loot you receive from supported Crimson Desert reward sources.

It supports per-category loot quantity multipliers, ResourceNodes, NPC Trust Gain, Pet Abyss Gear affection boost, and the new optional DropChance system.

The mod uses active archive scanning, so it can patch the archive the game is actually reading, including JSON Mod Manager / pre-modded setups when supported.

## Current Version

**Trusty Loot Multiplier v3.3.0**

Built and tested for **Crimson Desert v1.05.01**.

## Main Features

- Per-category loot quantity multipliers
- Optional DropChance system
- ResourceNodes multiplier
- NPC Trust Gain adjustment
- Pet Abyss Gear +10 support
- Expanded Gathering coverage for flowers, herbs, and botany pickups
- Active archive scanning for JSON Mod Manager / pre-modded setups
- Runtime backup and restore on normal game close
- Leftover backup restore on next launch if needed

## DropChance

DropChance raises supported DropSet chance values up to the selected target percent.

Example:

- `ChanceBoost=5` raises supported drops below 5% up to 5%
- `ChanceBoost=25` raises supported drops below 25% up to 25%
- `ChanceBoost=100` makes supported drops guaranteed where supported

DropChance affects how often supported drops happen, not how many items you receive.
