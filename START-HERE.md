# Start Here

If you just clicked this GitHub repo and thought “okay, but what do I *do* first?” — start here.

This repo is the **course/control tower**. Your actual mod code should live in separate repos as you build projects.

## The first-week path

Do these in order:

1. Read [`docs/00-map-of-tmodloader.md`](docs/00-map-of-tmodloader.md)
2. Set up your Mac with [`docs/01-mac-setup.md`](docs/01-mac-setup.md)
3. Create a journal with [`projects/00-first-mod-journal.md`](projects/00-first-mod-journal.md)
4. Learn just enough C# with [`docs/02-csharp-for-pythonistas.md`](docs/02-csharp-for-pythonistas.md)
5. Build your first tiny mod with [`docs/02-your-first-mod-debug-apple.md`](docs/02-your-first-mod-debug-apple.md)
6. Mark progress in [`progress/progress-tracker.md`](progress/progress-tracker.md)

## What you are trying to produce first

Not `NoviceRealms`. That is the capstone.

Your first project is:

```text
debug-apple
```

It should prove only this:

- tModLoader sees your mod
- your C# compiles
- one custom item appears or can be crafted
- you can build/reload/test/read logs
- you can commit a working slice

## Where things live

Recommended Mac layout:

```text
~/src/game-modding-skill-tree/   # this curriculum repo
~/src/debug-apple/               # your first real mod source
~/src/training-arsenal/          # later mod source
~/src/novice-realms/             # capstone mod source
```

If you keep the curriculum in `~/Documents`, that is okay too. But active mod code is cleaner in `~/src` or `~/dev`.

## What if I do not know C#?

That is fine. You need enough to read one tiny tModLoader class, not enough to write enterprise C#.

Use:

- [`docs/02-csharp-for-pythonistas.md`](docs/02-csharp-for-pythonistas.md)
- Microsoft C# beginner path in [`docs/resources.md`](docs/resources.md)
- compiler errors as teaching feedback

## What if I get stuck?

Use [`docs/troubleshooting.md`](docs/troubleshooting.md).

When asking an AI agent for help, paste:

- exact tModLoader version
- your OS
- the file you changed
- the full first compiler error
- what you expected to see
- what actually happened

Do not ask: “make me a mod.”

Ask: “help me make this one item compile.”
