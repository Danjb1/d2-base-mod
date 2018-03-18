# Diablo II Base Mod

Diablo II modding, in its most basic form, consists of editing text files that make up the game's data. These files can be extracted from the game's MPQ files. However, the original files contain a number of bugs, which this project aims to fix, thereby providing a solid base of files for modders to build on.

Currently this only addresses bugs in the game's data files, not the code itself. There are still [many](https://us.battle.net/forums/en/bnet/topic/20752488250) [bugs](https://us.battle.net/forums/en/bnet/topic/20745264496) [out there](https://us.battle.net/forums/en/d3/topic/6037267083).

## Features

### New Features

 - Enable all Ladder-only runewords.
 - Enable Pattern and Plague runewords.
 - Re-enable Azurewrath Crystal Sword.

### Bug Fixes

 - Fixed Hratli's items all having a magic level of 1.
 - Fixed a bunch of magic prefixes never spawning on staffs.
 - Fixed Plague Javelin's poison trail not dealing damage.
 - Fixed various poison clouds playing incorrect sounds on collision.
 - Fixed Frozen Horror's arctic blast triggering on-collision events.
 - Fixed missing Frozen Orb explosion.
 - Fixed broken SandRaider AI where they get stuck in "flee" mode.
 - Fixed mismatched Hell Clan / Death Clan AI.
 - Fixed BatDemons spawning at ground level.
 - Fixed Spirit of Barbs displaying the wrong Thorns damage per level.
 - Fixed the Smith and Griswold's dropping the wrong loot on nightmare.
 - Fixed Siege Beast's stomp dealing no damage.
 - Fixed lots of other issues in the text files that have no impact on gameplay.
 - Incorporate [Fixed Font Mod](http://www.snakebytestudios.com/projects/mods/diablo-2-mods/#fixedfont) by SnakeByte Studios.
 - Incorporate [No Intro Mod](http://www.snakebytestudios.com/projects/mods/diablo-2-mods/#nointro) by SnakeByte Studios.

### Backported Features / Fixes

The following changes from the official patches are included in the Base Mod, and can be backported to older versions:

 - Rune and rare item names displayed in orange (requires modified *patchstring.tbl*).
 - Oblivion Knights no longer cast Iron Maiden (take care to refer to the new "Iron Maiden2" skill when making new items, etc.).
 - All non-code fixes from patches up to v1.13d.

## Getting Started

For information on creating a mod from these files, and which versions of the game are supported, see the [FAQ](docs/FAQ.md).

## Recompilation

After running the game, the text files will be converted to BIN files. These must be deleted before the game will recognise any further changes to the text files. The script `force_recompile.sh` will delete these files automatically (must be run through bash).
