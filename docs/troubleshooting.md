# Troubleshooting Cookbook

When something breaks, do not flail. Match the symptom, inspect the nearest evidence, change one thing, test again.

## Where are logs?

Common macOS tModLoader logs folder:

```text
~/Library/Application Support/Terraria/tModLoader/Logs
```

Open it:

```bash
open "$HOME/Library/Application Support/Terraria/tModLoader/Logs"
```

## Symptom: `dotnet` command not found

Meaning: .NET SDK is not installed or not on PATH.

Try:

```bash
dotnet --info
```

If missing, revisit [`01 — MacBook Setup`](01-mac-setup.md) and [Install .NET on macOS](https://learn.microsoft.com/en-us/dotnet/core/install/macos).

## Symptom: Homebrew command not found

Meaning: Homebrew is not installed or your shell does not load it.

Apple Silicon usually needs:

```bash
eval "$(/opt/homebrew/bin/brew shellenv)"
```

## Symptom: tModLoader does not see my mod

Check:

- Are you editing the folder under `ModSources`?
- Did you create a source mod, not just download a Workshop mod?
- Did you restart/reload tModLoader?
- Is the folder name weird or nested twice?

## Symptom: Build failed

Do this:

1. Read the **first** compiler error, not the last.
2. Find the file and line number.
3. Check for typos, missing `using`, wrong method signature.
4. Compare with ExampleMod.

Useful prompt:

```text
Explain this tModLoader/C# compile error. Identify the likely file, smallest fix, and whether this is a C# syntax issue or tModLoader API issue.
<paste first error>
```

## Symptom: `No suitable method found to override`

Meaning: your method signature does not match the tModLoader version.

Fix: check the API docs and ExampleMod for the exact method name, return type, and parameters.

## Symptom: Item has no display name or tooltip

Likely localization issue.

Check:

- localization file exists
- key matches your mod/item namespace
- file format is valid
- tModLoader version uses the localization style you copied

## Symptom: Missing texture

Likely path/casing issue.

Check:

- PNG exists
- folder path matches class namespace/convention
- capitalization matches exactly
- file is included in source, not ignored

Mac warning: your filesystem may hide casing mistakes. Other systems may not.

## Symptom: Recipe does not work

Check:

- ingredient exists
- tile requirement is reachable
- recipe registered in `AddRecipes`
- you rebuilt/reloaded after changes

## Symptom: Game crashes or hangs on reload

Do not keep clicking randomly.

1. Disable the mod if possible.
2. Read logs.
3. Revert last change with Git if needed.
4. Test a smaller slice.

## Symptom: AI gave me code that does not compile

Normal. AI agents hallucinate APIs.

Ask:

```text
Which exact tModLoader ExampleMod file or API doc supports this code? If none, rewrite it using only verified APIs.
```

## What to paste when asking for help

- OS: macOS version / Apple Silicon or Intel
- tModLoader version
- Terraria version
- file changed
- exact first error
- what you expected
- what happened
- relevant log snippet
