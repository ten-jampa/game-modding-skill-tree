# 01 — MacBook Setup

## Goal

Get a MacBook ready for Terraria/tModLoader modding without Windows-tutorial path hell.

## Install order

### 1. Xcode command-line tools

```bash
xcode-select --install
```

Verify:

```bash
xcode-select -p
git --version
clang --version
```

### 2. Homebrew

Install from <https://brew.sh/>.

Apple Silicon setup usually looks like:

```bash
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```

Verify:

```bash
brew --version
brew doctor
```

### 3. Core tools

```bash
brew install git git-lfs jq wget curl unzip
brew install --cask dotnet-sdk
brew install --cask steam
```

Optional editors:

```bash
brew install --cask cursor
brew install --cask visual-studio-code
brew install --cask rider
```

Verify:

```bash
git --version
git lfs version
dotnet --info
dotnet --list-sdks
```

### 4. Steam, Terraria, tModLoader

Install through Steam:

1. Terraria
2. tModLoader

Launch tModLoader once from Steam before trying to mod it.

## Common macOS paths

Steam apps usually live here:

```text
~/Library/Application Support/Steam/steamapps/common/
```

Terraria/tModLoader user data usually lives here:

```text
~/Library/Application Support/Terraria/tModLoader
```

Mod sources often live here:

```text
~/Library/Application Support/Terraria/tModLoader/ModSources
```

Open the folder:

```bash
open "$HOME/Library/Application Support/Terraria/tModLoader"
```

## Recommended source layout

For serious hacking, keep repos outside iCloud-synced folders:

```text
~/src/GameModdingSkillTree
~/src/NoviceRealms
```

Then symlink into tModLoader when needed:

```bash
mkdir -p "$HOME/Library/Application Support/Terraria/tModLoader/ModSources"
ln -s "$PWD" "$HOME/Library/Application Support/Terraria/tModLoader/ModSources/YourModName"
```

## Mac-specific gotchas

- Finder hides `~/Library`; use Terminal or Finder → Go → hold Option → Library.
- Always quote paths with spaces.
- macOS may be case-insensitive; keep asset paths and class names consistently cased.
- If an old tool needs Rosetta: `softwareupdate --install-rosetta --agree-to-license`.

## First verification loop

1. Launch Steam.
2. Launch tModLoader.
3. Create a fresh test character.
4. Create a fresh test world.
5. Create or open a starter mod.
6. Build/reload the mod.
7. Check logs if anything breaks.

Logs are usually under:

```text
~/Library/Application Support/Terraria/tModLoader/Logs
```
