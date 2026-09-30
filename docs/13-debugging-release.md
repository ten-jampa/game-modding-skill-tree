# 13 — Debugging and Release Hygiene

## Goal

Stop treating “it worked once on my machine” as done.

## Debug loop

1. Reproduce the problem.
2. Read the log.
3. Form one hypothesis.
4. Change one thing.
5. Test again.
6. Write down what happened.

## tModLoader release checklist

- [ ] Builds cleanly.
- [ ] Mod enables without errors.
- [ ] No missing textures.
- [ ] No missing localization keys.
- [ ] Recipes work.
- [ ] Projectiles die correctly.
- [ ] Enemies spawn under intended conditions.
- [ ] Player data saves and loads.
- [ ] UI opens and closes reliably.
- [ ] Boss can be summoned and defeated.
- [ ] Fresh character/world tested.
- [ ] Logs checked after test session.
- [ ] README has install instructions.
- [ ] Known issues documented.

## Debugging mantra

The running game is the oracle. Your theory is not.
