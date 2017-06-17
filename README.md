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

## FAQ

### How do I create a mod from these files?

1. Create a directory for your mod within your Diablo II directory, e.g. "My Mod".
2. Create a shortcut to Diablo II, and place it in your mod folder.
3. Edit the shortcut properties, and append *-direct -txt* to the target parameter.
For example:
    > Target:
"C:\Diablo II\Game.exe" -direct -txt
4. Place the Base Mod files into your mod folder such that you have the following directory structure:
    ```
    .
    +-- Diablo II
    |   +-- My Mod
    |   |   +-- data
    |   |   |   +-- global
    |   |   |   |   +-- ...
    |   |   |   +-- local
    |   |   |   |   +-- ...
    |   |   +-- Mod shortcut
    ```

5. Running your shortcut will launch the game with your mod applied; any changes made to the text files will take effect. Note that the game compiles the text files into BIN files. The game will always use the BIN files if they are present, so be sure to delete them the next time you want to make a change!

> Note: If you want to run your mod with PlugY, you have to follow slightly different steps. See the PlugY documentation.

### Can I play my mod online?

No; mods are not supported in Battle.net, only single-player games and TCP/IP. Worse - connecting to Battle.net will automatically patch your game to the latest version, which may not be desirable.

### Which version of the game do these files come from?

These files are taken from Diablo II: Lord of Destruction v1.13c, which is the latest version of the game to include any data modifications (as opposed to just code changes).

### Can I use these files with other versions of the game?

Yes, with a few caveats. The list below describes exactly what you can expect from all of the significant versions. For the full list of changes made by each patch, see *[patch.txt](https://raw.githubusercontent.com/Danjb1/d2-versions/master/patch.txt)*:

#### v1.14d
 - The Base Mod will work perfectly, since this version uses the same text files as v1.13c.
 - You will have all of the latest features of the game.

#### v1.13d
 - The Base Mod will work perfectly.
 - You will have all of the latest features of the game.
 - You will be missing the minor fixes / improvements added by the v1.14 patches.
 - **This is the last version of the game to support [PlugY](#links).**

#### v1.12a
 - This version is the same as v1.11b, with the addition of a no-CD patch (see *patch.txt* for instructions).
 - **This is the only version of the game compatible with the [D2MultiRes](#links) mod.**

#### v1.11b
 - The Base Mod will work, with the added advantage that these files will actually backport some of the fixes and new items added by v1.13. However, the new items will not display correctly, because their graphics are missing from older patches. This can be fixed by using the *Patch_D2.mpq* file from v1.13+.
 - You will be missing the minor fixes / improvements added by the v1.14 patches.
 - You will be missing some features / fixes introduced by the v1.13 patches, notably:
     - Uber Tristram.
     - The ability to respec. The essences will still drop, but they will not be functional. Respecialisation can be done manually through the [Hero Editor](#links) instead.
     - Some code fixes, mostly related to online play.

#### v1.09 and older
 - These versions are incompatible with the Base Mod since they use older text files with different columns.

> To find out how to switch between different game versions, check out [this project](https://github.com/Danjb1/d2-versions).

### Do I need all of the text files?

No, some are included only for reference and cannot be changed. See [this thread](http://d2mods.info/forum/viewtopic.php?t=34455) for the full list.

However, this is no harm in including all of the files in your mod.

### How is this project different from the other text file fixes out there?

It's not vastly different - this project simply combines several other fixes that are already available, and brings them up to date with the latest patches, so that mods can be made to target any version of the game without degrading functionality.

Care has been taken to include only changes that are balanced and true to the original game. For example, Nefarius' fixed 1.11b text files included an undocumented change that enabled an extremely overpowered item called the Constricting Ring; this change has not been included in the Base Mod.

Having the project on Github also makes it very easy to see precisely what's been changed in each file (the first commit contains just the clean text files, with no changes).

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
