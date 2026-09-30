# Game Modding Skill Tree

A Mac-first, agent-assisted curriculum for climbing from “I have no idea where to start” to building real game mods: items, projectiles, enemies, progression systems, skill trees, bosses, and eventually more ambitious AI-assisted workflows.

The first main path is **Terraria with tModLoader** because it gives fast feedback, real code, visual payoff, and a sane progression from tiny content mods to full systems.

## Who this is for

- You can code a bit, but game modding feels like an impossible wall.
- You primarily hack on a **MacBook**.
- You use Cursor, Claude Code, Codex, or similar agents.
- You want a ladder, not a pile of random tutorials.

## What this repo is not

- Not a piracy guide.
- Not an anti-cheat bypass guide.
- Not a multiplayer cheat guide.
- Not “just ask AI to make a mod” slop.
- Not reverse-engineering-first. Judgment first, god tools later.

## The core climb

```text
Orientation
  → Mac setup
  → C# for Python-minded programmers
  → Items and recipes
  → Projectiles and combat behavior
  → Player state and progression
  → Enemies and AI
  → Loot loops
  → Buffs and status systems
  → UI
  → Mini skill tree
  → Data-driven skill tree
  → Boss
  → Release hygiene
  → Agent-assisted scaling
```

## Start here

1. Read [`docs/00-map-of-tmodloader.md`](docs/00-map-of-tmodloader.md).
2. Do [`docs/01-mac-setup.md`](docs/01-mac-setup.md).
3. Use [`progress/progress-tracker.md`](progress/progress-tracker.md) as your save file.
4. Pick the first milestone: [`milestones/milestone-0-orientation.md`](milestones/milestone-0-orientation.md).

## Agent-traversable DAG

For humans, follow the docs below.

For AI agents, use:

- [`curriculum/agent-traversal.md`](curriculum/agent-traversal.md)
- [`curriculum/skill-tree-dag.json`](curriculum/skill-tree-dag.json)

The JSON graph names each node, prerequisite, unlocked branch, target artifact, and `done_when` criteria.

## Main path

The primary curriculum lives in [`docs/`](docs/):

- `00` — map of tModLoader
- `01` — Mac setup
- `02` — C# for Pythonistas
- `03` — items, recipes, tooltips
- `04` — projectiles and combat
- `05` — ModPlayer and progression
- `06` — NPCs and enemy AI
- `07` — drops and loops
- `08` — buffs/status effects
- `09` — UI skill tree prototype
- `10` — data-driven skill trees
- `11` — boss design
- `12` — AI-agent workflow
- `13` — debugging and release hygiene

## Later branches

After the Terraria path, branch into:

- [`paths/minecraft-fabric.md`](paths/minecraft-fabric.md)
- [`paths/rimworld.md`](paths/rimworld.md)
- [`paths/unity-games.md`](paths/unity-games.md)
- [`paths/bethesda-games.md`](paths/bethesda-games.md)
- [`docs/later-stage-tools/universal-modder.md`](docs/later-stage-tools/universal-modder.md)

## Capstone

Build **NoviceRealms**, a compact Terraria mod containing:

- 5 weapons
- 2 accessories
- 1 material chain
- 4 enemies
- 1 debuff
- 1 mini skill tree
- 1 boss
- 1 summon item
- saved player progression
- a basic custom UI
- a release checklist

See [`projects/08-capstone-novice-realms.md`](projects/08-capstone-novice-realms.md).

## The rule

Do not start by designing the giant skill tree.

Start by making **one unlock do one thing**.

## Contributors

This repo is intentionally AI-assisted. See [`CONTRIBUTORS.md`](CONTRIBUTORS.md) for the human + Hermes collaboration note.
