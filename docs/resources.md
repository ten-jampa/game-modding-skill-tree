# Resources

This repo should not be a sealed box of homemade notes. Use these external resources as the source material while climbing the skill tree.

## How to use resources

- **Docs** answer: “What does this API actually do?”
- **ExampleMod** answers: “What does the pattern look like in real tModLoader code?”
- **Wiki.gg** answers: “How does vanilla Terraria behave?”
- **Microsoft Learn** answers: “What does this C# syntax mean?”
- **Logs** answer: “What actually broke?”

## tModLoader / Terraria

| Resource | Use it for |
| --- | --- |
| [tModLoader API docs](https://docs.tmodloader.net/) | Official class/method reference for `ModItem`, `ModProjectile`, `ModNPC`, `ModPlayer`, hooks, recipes, etc. |
| [tModLoader Wiki](https://github.com/tModLoader/tModLoader/wiki) | Setup, development workflow, publishing, and conceptual guides. |
| [tModLoader ExampleMod](https://github.com/tModLoader/tModLoader/tree/stable/ExampleMod) | The most important reference. Copy patterns from here before trusting random snippets. |
| [ExampleMod generated docs](https://docs.tmodloader.net/docs/stable/class_example_mod.html) | Browse ExampleMod classes through docs. |
| [tModLoader GitHub](https://github.com/tModLoader/tModLoader) | Source, issues, releases, advanced reference. |
| [tModLoader Steam Workshop](https://steamcommunity.com/app/1281930/workshop/) | Published mods, dependencies, distribution norms. |
| [Terraria Wiki.gg](https://terraria.wiki.gg/wiki/Terraria_Wiki) | Vanilla items, NPCs, mechanics, balancing references. |

## C# / .NET

| Resource | Use it for |
| --- | --- |
| [Microsoft C# docs](https://learn.microsoft.com/en-us/dotnet/csharp/) | Official C# language documentation. |
| [Take your first steps with C#](https://learn.microsoft.com/en-us/training/paths/get-started-c-sharp-part-1/) | Beginner interactive Microsoft Learn path. |
| [C# type system](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/types/) | Static typing, value/reference types, classes. |
| [Object-oriented C#](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/object-oriented/) | Classes, inheritance, and why `class Foo : ModItem` matters. |
| [Inheritance](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/object-oriented/inheritance) | `override`, base classes, and tModLoader hook methods. |
| [Install .NET on macOS](https://learn.microsoft.com/en-us/dotnet/core/install/macos) | Official macOS .NET SDK setup. |
| [Download .NET](https://dotnet.microsoft.com/en-us/download) | Official SDK downloads. |
| [C# Yellow Book](https://www.robmiles.com/c-yellow-book/) | Friendly beginner C# book. Optional but good. |

## Editors on Mac

| Resource | Use it for |
| --- | --- |
| [VS Code C# docs](https://code.visualstudio.com/docs/languages/csharp) | C# setup in VS Code / Cursor-like workflows. |
| [C# Dev Kit](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csdevkit) | Microsoft C# extension. |
| [Rider](https://www.jetbrains.com/rider/) | Full-featured C# IDE option. |
| [Visual Studio for Mac retirement notice](https://learn.microsoft.com/en-us/visualstudio/mac/what-happened-to-vs-for-mac) | Avoid old tutorials that tell you to use Visual Studio for Mac. |

## Git / GitHub

| Resource | Use it for |
| --- | --- |
| [GitHub Hello World](https://docs.github.com/en/get-started/start-your-journey/hello-world) | First GitHub concepts: repo, branch, commit, PR. |
| [Set up Git](https://docs.github.com/en/get-started/git-basics/set-up-git) | Initial Git configuration. |
| [Git basics](https://docs.github.com/en/get-started/git-basics) | Common GitHub/Git operations. |
| [Pro Git book](https://git-scm.com/book/en/v2) | Deeper Git reference. |
| [Learn Git Branching](https://learngitbranching.js.org/) | Visual branch/merge practice. |

## Safety / recovery

| Resource | Use it for |
| --- | --- |
| [Steam: backup game files](https://help.steampowered.com/en/faqs/view/4593-5CB7-DC3C-64F0) | General backup/restore concepts. |
| [Steam: verify integrity of game files](https://help.steampowered.com/en/faqs/view/0C48-FCBD-DA71-93EB) | Recovering from broken installs. |
| [PCGamingWiki: Terraria](https://www.pcgamingwiki.com/wiki/Terraria) | File locations across OSes. |
| [Choose a License](https://choosealicense.com/) | Choosing a license for mod code repos. |
| [Keep a Changelog](https://keepachangelog.com/en/1.1.0/) | Writing readable release notes. |
| [SemVer](https://semver.org/) | Versioning mods. |

## Later branches

| Branch | Resources |
| --- | --- |
| Minecraft Fabric | [Fabric Wiki](https://wiki.fabricmc.net/), [Fabric setup](https://wiki.fabricmc.net/tutorial:setup), [Fabric example mod](https://github.com/FabricMC/fabric-example-mod) |
| RimWorld | [RimWorld modding](https://rimworldwiki.com/wiki/Modding), [Modding tutorials](https://rimworldwiki.com/wiki/Modding_Tutorials), [Harmony docs](https://harmony.pardeike.net/) |
| universal-modder | [universal-modder repo](https://github.com/rehan-remade/universal-modder) after the beginner path, not before. |

## Lesson mapping

| Lesson | Primary external references |
| --- | --- |
| `00` orientation | tModLoader Wiki, Terraria Wiki.gg |
| `01` Mac setup | Install .NET on macOS, VS Code C# docs, tModLoader Wiki |
| `02` C# bridge | Microsoft C# docs, first steps with C#, inheritance docs |
| `02` DebugApple | tModLoader API docs, tModLoader ExampleMod |
| `03` items/recipes | `ModItem` docs, ExampleMod items, Terraria Wiki.gg |
| `04` projectiles | `ModProjectile` docs, ExampleMod projectiles |
| `05` progression | `ModPlayer` docs, ExampleMod player examples |
| `06` NPCs | `ModNPC` docs, ExampleMod NPCs |
| `09-10` skill tree UI | tModLoader UI examples, ExampleMod UI patterns |
| `13` release | Steam Workshop, SemVer, Keep a Changelog |
