# Glossary

## Mod

A change or extension to a game.

## Mod loader

A tool/layer that loads mods into a game. tModLoader is Terraria's community mod loader.

## API

The functions/classes a system exposes so your code can interact with it.

## Hook

A place where tModLoader calls your code, usually through a method you override.

## Class

A C# blueprint for an object or behavior. `DebugApple : ModItem` defines a custom item class.

## Method

A function inside a class.

## Override

Replacing/customizing behavior from a base class. tModLoader calls overridden methods like `SetDefaults`.

## Namespace

A C# naming/grouping system that keeps classes organized.

## Build / compile

Turn source code into something the game/mod loader can run. Compiler errors happen before the game runs.

## Runtime error

An error that happens while the game/mod is running.

## Asset

A non-code file used by the mod: texture, sound, localization file, etc.

## Localization

Text shown to players: item names, tooltips, UI labels.

## Recipe

A rule that turns ingredients into an item at a crafting station.

## NPC

Non-player character. In Terraria this includes enemies, critters, townsfolk, and bosses.

## Projectile

A moving entity such as an arrow, magic bolt, bullet, beam, or boss attack.

## Buff / debuff

A timed status effect. Buffs usually help; debuffs usually hurt.

## Save data

Data that persists after quitting/reloading, like XP or unlocked skills.

## Client / server

In multiplayer, the client is the player's game and the server is the authority coordinating the world. Ignore this at first unless you build multiplayer-safe systems.
