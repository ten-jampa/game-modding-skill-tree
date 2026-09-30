# 00 — What Are We Even Doing?

## Goal

Get oriented before any code, setup, or jargon.

By the end of this lesson, you should be able to explain:

- what Terraria is in this context
- what a mod is
- what tModLoader is
- why we are starting with Terraria/tModLoader
- what the basic learning loop looks like
- what words like `ModItem` and `ModPlayer` roughly mean, without needing to use them yet

## What is Terraria?

**Terraria** is a 2D sandbox/adventure game. It has items, weapons, enemies, bosses, crafting, biomes, loot, projectiles, status effects, NPCs, and progression.

That makes it a great learning game because mods can start tiny:

- one item
- one weapon
- one enemy
- one recipe
- one status effect

But the same game also supports bigger systems:

- new bosses
- new classes
- progression trees
- custom UI
- large content packs

So Terraria gives us a smooth ramp instead of a cliff.

## What is a mod?

A **mod** is a change or extension to a game.

Examples:

- add a new sword
- add a new enemy
- change a recipe
- add a skill tree
- add a boss
- add a new progression system

Mods can be tiny or huge. The trick is learning to make them tiny first.

## What is tModLoader?

**tModLoader**, often shortened to **tML**, is the community mod loader for Terraria.

Think of it as the layer between your code and Terraria:

```text
Your C# mod code
  ↓
tModLoader APIs/hooks
  ↓
Terraria
```

tModLoader gives you a supported-ish way to add content and behavior without directly hacking Terraria's executable.

It handles things like:

- loading mods
- compiling mod code
- registering items, projectiles, NPCs, recipes, and assets
- enabling/disabling mods
- showing errors/logs
- packaging mods

You install it as a separate Steam app: **tModLoader**.

Installation comes in the next lesson: [`01 — MacBook Setup`](01-mac-setup.md).

## What language are tModLoader mods written in?

Mostly **C#**.

If you know Python, the main difference is that C# is stricter:

- variables and method arguments have explicit types
- classes matter more
- the compiler catches many mistakes before the game runs
- a lot of modding means overriding methods tModLoader calls for you

You do **not** need to become a C# wizard before starting. You need enough C# to read small classes and fix compiler errors.

That bridge comes in [`02 — C# for Pythonistas`](02-csharp-for-pythonistas.md).

## Why not start with Minecraft, Skyrim, or Unity?

We might later. But Terraria/tModLoader is a good first climb because:

- setup is relatively contained
- examples are plentiful
- results are visible fast
- C# is useful beyond Terraria
- simple mods and complex mods live on the same ladder
- a skill tree mod decomposes nicely into items, projectiles, player state, UI, and save/load

## The basic modding loop

Every lesson eventually comes back to this loop:

```text
pick one tiny goal
  ↓
edit one small piece
  ↓
build/reload the mod
  ↓
launch a test world
  ↓
observe what happened
  ↓
read logs if broken
  ↓
write notes
  ↓
commit the working slice
```

This is the whole game. Everything else is detail.

## What will the first actual mod be?

Not the capstone.

The first actual mod should be something like:

```text
debug-apple
```

It might do only this:

- add one item
- give it a recipe
- make it display text or apply a tiny effect when used

That sounds stupid. Good. Stupid is how you get the loop working.

## The vocabulary map

You do **not** need to memorize this yet. This is just a map you will revisit.

### `ModItem`

A custom item: weapon, tool, accessory, material, summon item, consumable.

Example future use:

```text
DebugApple is a ModItem.
SparkWand is a ModItem.
BossSummonCrystal is a ModItem.
```

### `ModProjectile`

A moving thing spawned by an item, enemy, boss, or system.

Example future use:

```text
SparkWand shoots a SparkProjectile.
Boss fires TrainingConstructBolt projectiles.
```

### `ModNPC`

A custom enemy, critter, town NPC, or boss.

Example future use:

```text
TrainingSlime is a ModNPC.
TheTrainingConstruct boss is a ModNPC.
```

### `ModPlayer`

Custom state attached to a player.

Example future use:

```text
The player has training XP.
The player has skill points.
The player has unlocked Warrior Focus.
```

### `ModSystem`

A mod-level system that does not belong to just one item, projectile, NPC, or player.

Example future use:

```text
Registering a skill tree hotkey.
Loading UI.
Managing world-level systems.
```

## The mental model

```text
Item
  can shoot Projectile
  can apply Buff
  can use Recipe

Projectile
  can hit NPC
  can draw effects
  can run behavior every frame

NPC
  can move
  can attack
  can drop Items

Player
  owns saved state
  earns XP / skill points
  gets bonuses from unlocked skills

UI
  displays Player state
  lets player spend skill points
```

## Done when

You are done with this lesson when you can answer, in plain English:

1. What is tModLoader?
2. Why are we using Terraria as the first learning path?
3. What is the basic edit → build → test → log → commit loop?
4. Why is `debug-apple` a better first project than `novice-realms`?

## Next

Go to [`01 — MacBook Setup`](01-mac-setup.md).

Do not install random tools yet. Do not clone giant mods yet. Just get the official path working first.
