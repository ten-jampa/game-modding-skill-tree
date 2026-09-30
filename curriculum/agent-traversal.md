# Agent Traversal Guide

This repo is intentionally structured as a learning DAG, not a linear blog series.

Machine-readable graph: [`skill-tree-dag.json`](skill-tree-dag.json)

## How an agent should traverse this repo

1. Start at `README.md`.
2. Load this file.
3. Load `skill-tree-dag.json`.
4. Find the learner's current completed nodes from `progress/progress-tracker.md` or the user's statement.
5. Select the next node whose `requires` are all complete.
6. Read that node's `file`.
7. Produce only the next smallest action, not the whole curriculum.
8. Ask for real verification output when a node requires in-game testing.

## Default traversal order

```text
orientation
  ├─ mac-setup
  └─ mod-journal
      ↓
csharp-basics
  ↓
items-recipes
  ↓
projectiles-combat
  ├─ modplayer-progression
  │   └─ npcs-enemy-ai
  │       └─ drops-loops
  └─ buffs-status
      ↓
ui-skill-tree
  ↓
data-driven-skill-tree
  ├─ agent-workflow
  └─ boss-design
      ↓
debugging-release
  ↓
capstone-novice-realms
  ├─ minecraft-fabric
  ├─ rimworld
  ├─ unity-games
  ├─ bethesda-games
  └─ universal-modder
```

## What counts as complete

A node is not complete because the learner read a doc.

A node is complete when its `done_when` conditions in `skill-tree-dag.json` are satisfied, usually with one of:

- a working in-game artifact
- a saved journal entry
- a verified setup command
- a checked log file
- a committed working slice

## Agent behavior rules

- Do not skip prerequisites unless the user explicitly says they already have the skill.
- Do not jump to `capstone-novice-realms` before the skill tree/UI/progression/boss pieces exist.
- Do not treat `universal-modder` as a starting point.
- Prefer small named repos/projects: `debug-apple`, `training-arsenal`, `projectile-lab`, `training-rank`, `enemy-pack`, `skill-tree-prototype`, then `novice-realms`.
- If the learner is stuck, route backward to the nearest missing prerequisite.

## Next-action template

When guiding the learner, answer with:

```markdown
## Current node
<node id + title>

## Why this node
<which prerequisites are complete>

## Next smallest action
<one concrete task>

## Verification
<command, in-game observation, log, or screenshot needed>

## If it fails
<first debugging step>
```
