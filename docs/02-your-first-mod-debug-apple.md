# 02 — Your First tModLoader Mod: DebugApple

## Goal

Create the smallest possible real mod: one item called `DebugApple`.

This lesson is the bridge between “reading the curriculum” and “actually modding.”

## What you will prove

- tModLoader can see your mod.
- Your editor can open the source.
- Your C# can compile.
- You can build/reload the mod.
- You can test in a fresh world.
- You can read logs when something breaks.

## Prerequisites

- [`00 — What Are We Even Doing?`](00-map-of-tmodloader.md)
- [`01 — MacBook Setup`](01-mac-setup.md)
- A test character and test world in tModLoader
- A mod journal from [`projects/00-first-mod-journal.md`](../projects/00-first-mod-journal.md)

Helpful external references:

- [tModLoader Wiki](https://github.com/tModLoader/tModLoader/wiki)
- [tModLoader API docs](https://docs.tmodloader.net/)
- [tModLoader ExampleMod](https://github.com/tModLoader/tModLoader/tree/stable/ExampleMod)

## Step 1 — Create a new mod source

Open tModLoader from Steam.

Look for the development/mod creation area. The exact UI changes over time, but the route is usually around:

```text
Workshop / Develop Mods / Create Mod
```

Create a mod named something like:

```text
DebugApple
```

Use a simple internal name with no spaces if tModLoader asks for one.

## Step 2 — Find the source folder on macOS

Common path:

```bash
open "$HOME/Library/Application Support/Terraria/tModLoader/ModSources"
```

You should see a folder for your mod.

If you do not, check:

- Did you launch tModLoader once?
- Did you actually create the mod source, not just enable a workshop mod?
- Are you looking under `~/Library/Application Support`, not the Steam install folder?

## Step 3 — Open the mod in your editor

From Terminal:

```bash
cd "$HOME/Library/Application Support/Terraria/tModLoader/ModSources"
open .
```

Then open the `DebugApple` folder in Cursor, VS Code, or Rider.

You are looking for files like:

```text
DebugApple/
  DebugApple.csproj
  build.txt
  description.txt
  icon.png
  ...source folders...
```

The exact generated layout can vary by tModLoader version. That is okay.

## Step 4 — Before editing, commit the generated baseline

If you are comfortable with Git:

```bash
cd "$HOME/Library/Application Support/Terraria/tModLoader/ModSources/DebugApple"
git init
git add .
git commit -m "Initial tModLoader generated mod"
```

If Git is too much today, skip it once — but do not make that a habit.

## Step 5 — Add the tiniest item

Create an item class using the current tModLoader patterns. The exact folders are convention, not magic. A common layout is:

```text
Content/Items/DebugApple.cs
```

A tiny item class will look conceptually like this:

```csharp
using Terraria;
using Terraria.ID;
using Terraria.ModLoader;

namespace DebugApple.Content.Items;

public class DebugApple : ModItem
{
    public override void SetDefaults()
    {
        Item.width = 20;
        Item.height = 20;
        Item.maxStack = 30;
        Item.value = Item.buyPrice(copper: 5);
        Item.rare = ItemRarityID.White;
        Item.useStyle = ItemUseStyleID.EatFood;
        Item.useTime = 20;
        Item.useAnimation = 20;
        Item.consumable = true;
    }

    public override bool? UseItem(Player player)
    {
        if (Main.myPlayer == player.whoAmI)
        {
            Main.NewText("Debug apple used. The loop works.");
        }

        return true;
    }

    public override void AddRecipes()
    {
        Recipe recipe = CreateRecipe();
        recipe.AddIngredient(ItemID.Apple, 1);
        recipe.AddTile(TileID.WorkBenches);
        recipe.Register();
    }
}
```

Important: tModLoader APIs change. If this fails, compare against [ExampleMod](https://github.com/tModLoader/tModLoader/tree/stable/ExampleMod) and the [API docs](https://docs.tmodloader.net/), then update the code.

## Step 6 — Add localization if your tModLoader version expects it

Modern tModLoader projects often use localization files. Look for a `Localization` folder or ExampleMod localization patterns.

Conceptually, you want entries for:

```text
DisplayName: Debug Apple
Tooltip: A tiny test item. If you can use this, your modding loop works.
```

Do not panic if the exact `.hjson` key format differs. Use the generated files or ExampleMod as the source of truth.

## Step 7 — Texture placeholder

Items usually need a texture at the expected path.

For the first run, you have options:

1. Use a placeholder copied from your own generated template assets if permitted.
2. Draw a tiny original 20x20 or 16x16 PNG.
3. If missing texture errors happen, treat that as the next debugging lesson.

Do not copy Terraria sprites into your repo as if they are yours.

## Step 8 — Build/reload in tModLoader

Go back to tModLoader and build/reload the mod.

You should see either:

- success: the mod builds and reloads
- failure: compiler errors or missing asset/localization errors

Failure is not a disaster. It is the curriculum.

## Step 9 — Test in-game

Use a fresh test character and world.

Try to craft/use the item.

Expected result:

- You can obtain or craft the Debug Apple.
- Using it prints a message: `Debug apple used. The loop works.`

If crafting is annoying, temporarily adjust the recipe or use a testing helper. The goal is to verify the loop, not suffer.

## Step 10 — Write the journal entry

Record:

- files changed
- build result
- error messages, if any
- whether the item appeared
- whether the message displayed
- what you will try next

Use [`templates/mod-journal-template.md`](../templates/mod-journal-template.md).

## Step 11 — Commit the working slice

```bash
git status
git add .
git commit -m "Add DebugApple item"
```

Do not commit `bin/`, `obj/`, or `.tmod` build outputs unless you intentionally changed repo rules.

## Common failures

### `The type or namespace name ... could not be found`

Usually missing `using`, wrong namespace, or typo.

### `No suitable method found to override`

The method signature is wrong for your tModLoader version. Check ExampleMod/API docs.

### Item has no name or weird text

Localization key/file is missing or wrong.

### Missing texture

The class path and texture path do not line up, or the PNG is missing/wrongly named.

### Mod does not appear

You may be editing the wrong folder, or tModLoader is looking at a different ModSources path.

## Done when

- [ ] `DebugApple` mod source exists.
- [ ] You can build/reload it.
- [ ] One custom item class exists.
- [ ] You tested in-game.
- [ ] You wrote a journal entry.
- [ ] You committed the working slice.

## Next

Then continue to [`03 — Items, Recipes, and Tooltips`](03-items-recipes-tooltips.md), where `DebugApple` grows into `training-arsenal`.
