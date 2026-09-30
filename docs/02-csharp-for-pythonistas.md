# 02 — C# for Pythonistas

## Goal

Learn only enough C# to read and write tModLoader code without flailing.

## Translation table

| Python instinct | C# / tModLoader reality |
| --- | --- |
| Duck typing | Static types and compile-time errors |
| Free functions | Classes and methods everywhere |
| Runtime surprises | Compiler yells earlier, which is good |
| Dictionaries/lists | `Dictionary<TKey,TValue>`, `List<T>` |
| Inheritance optional | Inheritance is central: `class Foo : ModItem` |
| Magic strings everywhere | Enums, constants, IDs, typed APIs |

## C# ideas you need first

- `class`
- `namespace`
- `public`, `private`, `protected`
- inheritance: `class SparkWand : ModItem`
- method override: `public override void SetDefaults()`
- properties and fields
- `int`, `float`, `bool`, `string`
- `List<T>` and `Dictionary<TKey, TValue>`
- `null` and nullable references

## tModLoader pattern

Most early code is “override a method, set fields, test in-game.”

The exact APIs can change. Verify against the current tModLoader docs and ExampleMod.

## Exercise

Create notes for three patterns:

1. `ModItem.SetDefaults`
2. `ModProjectile.AI`
3. `ModPlayer.SaveData` / `LoadData`

Do not memorize everything. Learn to read compiler errors.
