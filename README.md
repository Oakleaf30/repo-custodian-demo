# Lumina-Caverns

Dive into the caves to mine ores and discover gems!

Lumina-Caverns is a roguelite mining game across three biomes: **Normal**,
**Frozen**, and **Lava**. Each biome has 30 floors to descend through, its own
main ore, magic ore, and pair of gems, and its own set of enemies to survive.

## Biomes

| Biome  | Main Ore | Magic Ore  | Gems                  |
|--------|----------|------------|------------------------|
| Normal | Copper   | Cobalt     | Amethyst, Topaz        |
| Frozen | Iron     | Mithril    | Aquamarine, Sapphire   |
| Lava   | Gold     | Adamantite | Ruby, Emerald          |

An elevator unlocks once a new biome is reached, letting players skip ahead on
future runs. Unlocking it costs bars and magic ore from that biome.

## Core gameplay loop

- Break rocks to reveal the ladder down to the next floor.
- There's a flat chance per rock broken to instead reveal a hole, unrelated
  to the ladder, leading to a **coal floor** or an **infested floor**.
- Coal is required to smelt mined ore into bars. Bars repair and upgrade gear.
- Dying costs the player their mining inventory for that run — unless they've
  crafted an amulet (see Extras below).
- Health potions can be crafted at base from monster drops. Carrying capacity
  is capped, and potions heal slowly over time, to discourage spamming.

## Extras

- Coal drops from ore/coal nodes, barrels, and enemies.
- Geodes drop (uncommonly, not guaranteed) from mining, barrels, and enemies.
  They open for free and mostly contain magic ore, with occasional coal, ore,
  or rare gems. A pity system protects against extreme bad-luck streaks.
- Magic ore + a diamond crafts an amulet that prevents inventory loss on
  death. Diamonds are otherwise found in chests, or extremely rarely from
  mining/barrels/enemies, and can substitute for enchanting materials.
- Coal floors always spawn with a ladder. Infested floor ladders appear once
  all enemies are cleared and the floor's chest is looted.
- Bombs (crafted from coal + monster parts, capped per run) instantly break
  nodes and kill enemies — except dungeon enemies.

## Enchantments

Enchantments unlock after clearing the first biome and require a gem plus
magic ore from that biome. Each enchantment lasts a fixed number of runs
before it needs reapplying. See `docs/game-design.md` for the full list of
pickaxe, armour, and sword enchantments.

See `docs/game-design.md` for full mechanical detail: enemy behaviours,
pickaxe tiers, enchantment lists, and the trader system.
