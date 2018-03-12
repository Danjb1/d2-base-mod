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
 - Fixed lots of other issues in the text files that have no impact on gameplay.

### Backported Features / Fixes

The following changes from the official patches are included in the Base Mod, and can be backported to older versions:

 - Rune and rare item names displayed in orange (requires modified *patchstring.tbl*).
 - All non-code fixes from patches up to v1.13d.

## Getting Started

For information on creating a mod from these files, and which versions of the game are supported, see the [FAQ](docs/FAQ.md).

## Links

### Tools Used

 - [WinMPQ](http://sfsrealm.hopto.org/downloads/WinMPQ.html) - to extract files from the game's MPQ files.
 - [d2txtanalyser](http://d2mods.ulf-johan.info/forum/viewtopic.php?f=7&t=22624) - to analyse the text files and find errors.
 - [Peer TBL Editor](http://d2mods.info/filecenter/dload.php?action=file&file_id=144) and [d2edit](http://d2mods.info/filecenter/dload.php?action=file&file_id=1477) - to edit the game's string (TBL) files.
 - [WinMerge](http://winmerge.org/?lang=en) - to determine differences between 2 folders.
 - [TortoiseGitMerge](https://tortoisegit.org/docs/tortoisegitmerge/) - to determine differences between 2 files.

### Modding Guides

 - [File Guides](http://d2mods.info/forum/viewtopic.php?t=34455) - tutorials for editing the various text files.
 - [AI Compendium](http://d2mods.info/forum/viewtopic.php?f=4&t=36230) - tutorials for editing tweaking monster AI.

### Other Mods / Tools

 - [PlugY](http://plugy.free.fr/en/index.html) - huge single-player enhancement mod.
 - [D2MultiRes](http://www.moddb.com/games/diablo-2/news/d2multires) ([for v1.13c?](https://www.reddit.com/r/slashdiablo/comments/1a0cy7/good_news_multires_working_with_113c_bad_news_see/)) - enables higher resolutions.
 - [Hero Editor](http://www.moddb.com/games/diablo-2-lod/downloads/hero-editor-v-104) - save-game editor.
 
 > If anyone wants to have a go at making MultiRes work with later versions, here is some [related](https://github.com/lolet/D2Ex2/blob/master/ExMultiRes.cpp) [source](https://github.com/raler/Cham) [code](http://www.blizzhackers.cc/viewtopic.php?t=450772).

## Acknowledgements

 - Nefarius - for his fantastic work on the [fixed 1.11b text files](http://d2mods.info/filecenter/dload.php?action=file&file_id=1365).
 - Count.Dracula - for his [fixed 1.13c text files](http://d2mods.info/forum/viewtopic.php?f=5&t=56033).
 - FearedBliss - for finding the bug with the Smith and Griswold's loot tables (see [Vanilla Frosting](https://github.com/fearedbliss/Diablo-II--Vanilla-Frosting)).
 - [The Phrozen Keep](http://d2mods.info/) - for hosting so many excellent resources.

## Disclaimer

The unmodified game data within this project is the intellectual property of *Blizzard Entertainment*.
