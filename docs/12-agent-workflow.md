# 12 — AI-Agent Workflow

## Goal

Use AI agents as power tools, not drunk interns with filesystem access.

## Good uses

- Explain compile errors.
- Summarize tModLoader docs or ExampleMod patterns.
- Draft one class at a time.
- Generate small sprites/placeholders.
- Review diffs for obvious mistakes.
- Turn logs into hypotheses.

## Bad uses

- “Make me a full boss mod.”
- “Rewrite the whole skill tree system.”
- Letting the agent invent APIs.
- Letting the agent edit many files without a plan.
- Running unknown executables.
- Touching online/anti-cheat games.

## Productive loop

1. State the game, loader, version, and goal.
2. Give the agent relevant files only.
3. Ask for a tiny plan.
4. Ask it to edit one slice.
5. Run build/reload.
6. Check logs.
7. Review git diff.
8. Commit if good.
9. Widen scope.

## Reusable prompts

See [`prompts/`](../prompts/).

## The anti-slop constraint

Every AI-generated change must answer:

- What file changed?
- What behavior should I see in-game?
- How do I roll it back?
- What log/build output proves it worked?
