# 11 — Boss Design Fundamentals

## Goal

Climb one rung of the modding ladder without skipping prerequisite muscles.

## Outcomes

- Create a boss NPC.
- Build readable phase-based AI.
- Add summon item, loot, and telegraphs.

## Project: The Training Construct

- Phase 1: slow shots.
- Phase 2: radial burst.
- Phase 3: dash + minions.

## Done means

- The change builds or reloads in tModLoader.
- It works in a fresh test world or a controlled dev world.
- You wrote a short journal entry about what changed and what broke.
- You committed a working slice before widening scope.

## Pitfalls

- Asking an AI agent to do the whole module at once.
- Ignoring compiler errors instead of learning from them.
- Skipping logs.
- Changing multiple systems before testing one.
- Keeping placeholder behavior vague instead of verifying one specific effect.

## Agent prompt

```text
I am working on a tModLoader mod. Current module: Boss Design Fundamentals.
Goal: implement one tiny working slice: <describe slice>.
Use existing project conventions. Do not invent APIs. If unsure, point me to the exact tModLoader docs or ExampleMod pattern to verify.
After editing, tell me how to build, reload, and test in-game.
```
