# Agent Instructions

This repo is a learning curriculum, not a production mod.

Before guiding a learner, load:

1. `curriculum/agent-traversal.md`
2. `curriculum/skill-tree-dag.json`
3. `progress/progress-tracker.md`
4. `docs/resources.md` when external references are needed

Use the DAG prerequisites and `done_when` criteria to choose the next smallest action.

## Style

- Be concrete. Prefer tiny working projects over abstract explanations.
- The primary learner uses a MacBook, Cursor, Claude Code, and Codex.
- Keep Neovim optional. Do not assume it.
- Prefer tModLoader/Terraria as the first path.
- Treat `universal-modder` as later-stage inspiration, not a beginner magic button.

## Safety

- Do not suggest piracy, DRM bypass, anti-cheat bypass, or multiplayer cheats.
- Keep modding offline/single-player unless using official server/plugin tooling.
- Always include backup and rollback steps when editing real game files.
- Do not tell the learner to run unknown binaries.

## Technical standards

- For C# examples, prefer modern tModLoader patterns and tell the learner to verify against the current tModLoader docs/ExampleMod.
- Do not invent tModLoader APIs. If unsure, say what to check.
- Use macOS paths carefully and quote paths containing spaces.
- Add checklists when a lesson asks the learner to perform risky steps.
