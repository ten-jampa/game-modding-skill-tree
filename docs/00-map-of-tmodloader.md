# 00 — Map of tModLoader

## Goal

Understand what you are actually hacking on before you write code.

Terraria modding with tModLoader is not “build a game engine.” It is extending Terraria through a mod loader that gives you classes, hooks, assets, recipes, localization, and lifecycle methods.

## Core concepts

### `ModItem`

A custom item: weapons, tools, accessories, materials, summon items, consumables.

You usually define size, damage, use time, rarity, value, recipe, and projectile behavior if any.

### `ModProjectile`

A moving thing spawned by an item, NPC, or system.

Projectiles are where combat starts getting interesting: movement, collision, light, dust, hit behavior, lifetime, penetration, and custom AI.

### `ModNPC`

A custom enemy, critter, boss, or town NPC.

This is where you define stats, drops, spawn rules, behavior, and visual details.

### `ModPlayer`

Custom state attached to a player.

Use it for XP, skill points, unlocked skills, rank, per-player bonuses, and save/load logic.

### `ModSystem`

Global-ish mod systems.

Use carefully for world-level state, UI loading, keybind registration, recipes, and systems that do not belong to one item/NPC/player.

## Your first mental model

```text
Item
  can shoot Projectile
  can apply Buff
  can use Recipe

Projectile
  can hit NPC
  can draw effects
  can run AI every frame

NPC
  can move via AI
  can drop Items
  can apply Buffs

Player
  owns state via ModPlayer
  earns XP / skill points
  gets bonuses from unlocked skills

UI
  displays Player state
  lets player spend skill points
```

## First rule

Do not start with a boss. Do not start with a giant skill tree.

Start with one item. Then one projectile. Then one saved player value. Then one enemy.
