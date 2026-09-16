# Game Design Details

Full mechanical reference for Lumina-Caverns. For a high-level overview, see
the top-level `README.md`.

## Pickaxe

The pickaxe has three upgrade tiers, each requiring materials from
progressively deeper biomes:

1. **Crude** — a new pickaxe with increased base damage. Costs bars.
2. **Refined** — better mining efficiency and reduced repair cost. Costs bars
   and magic ore.
3. **Flawless** — grants a special ability tied to the biome's main ore.
   Costs bars, magic ore, and a gem.

If a player has no resources available, a free 5% repair is always offered.

### Special abilities by ore

- **Copper** — magnetises drops to the player.
- **Iron** — 1-tile radius knockback on swing.
- **Gold** — damages nearby nodes when mining.

## Enemies

Enemies are grouped by the biome/zone they appear in: **N**ormal, **F**rozen,
**L**ava, or **D**ungeon.

| Enemy         | Zone | Behaviour                                                        |
|---------------|------|-------------------------------------------------------------------|
| Slime         | N    | Moves directly towards the player.                                |
| Bug           | N    | Flies in straight lines.                                          |
| Bat           | F    | Flies towards the player; can cross rocks, liquids, and holes.     |
| Spinner       | F    | Moves in straight lines, bouncing off walls.                       |
| Icy slime     | F    | Slows player movement and swing speed on hit.                      |
| Elemental     | L    | Stationary; shoots projectiles at the player.                      |
| Lava worm     | L    | Burrows underground, periodically surfacing beneath the player.    |
| Lava slime    | L    | Leaves a lava trail as it moves.                                   |
| Fire spinner  | L    | Explodes after a delay when killed.                                |
| Skeleton      | D    | Walks quickly towards the player.                                  |
| Ghost         | D    | Floats through obstacles; teleports after damaging the player.     |
| Necromancer   | D    | Summons damaging ground spots around the player.                   |

## Enchantments

Enchantments unlock after clearing the first biome and require a gem plus
magic ore from that biome. Each enchantment lasts a fixed number of runs.

### Pickaxe enchantments

- Increased swing speed.
- Increased chance to find ladders and shafts.
- Chance to smelt a node directly into a bar when mined.
- Chance to drop magic ore when breaking nodes.
- Chance to reveal nearby nodes after mining one.
- Chance to instantly break the current rock.

### Armour enchantments

- Increases light radius around the player.
- Increases movement speed.
- Grants immunity to status effects (frozen, on fire, etc).
- Chance to block the next hit after taking damage.
- Periodically releases a damaging, enemy-repelling wave after being hit.
- Grants the ability to blink (short-range dash/teleport) in a direction.

### Sword enchantments

- Hitting enemies grants a temporary speed boost.
- Hitting enemies has a chance to stun them.
- Chance to heal on enemy kill.
- Causes an explosion on enemy kill.
- Chance to double drops from enemies.
- Swings have a chance to critically hit.

## Trader

*Note: The trader system is currently being finalised and details may change.*

The trader lets players see and choose from available reward tiers. Lower
tiers require more gems to purchase. Which gem set a player has correlates
with which biome's rewards they can access. A special gem — separate from
the standard biome gems — is required to unlock the trader's fourth and
final perk slot, and can only be used once all other perks are unlocked.

## Miscellaneous systems

- **Minimap** — shows floor layout as it's explored.
- Shaft and dungeon room icons on the minimap indicate whether a coal floor
  or infested floor is accessible from that point.
- **Emergency brewing stand** — usable once per run, for emergency potion
  crafting away from base.
- **Bar transfusion** — lower-tier bars can be transfused into higher-tier
  bars (at some conversion cost, exact rate TBD).