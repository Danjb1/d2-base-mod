# Diablo II Base Mod

Diablo II modding, in its most basic form, consists of editing text files that make up the game's data. These files can be extracted from the game's MPQ files. However, the original files contain a number of bugs, which this project aims to fix, thereby providing a solid base of files to work with.

## FAQ

### Which version of the game do these files come from?

These files are taken from Diablo II - Lord of Destruction v1.13c, which is the latest version of the game to include any data modifications (as opposed to just code changes).

### Can I use these files with other versions of the game?

Yes, with a few caveats:

 - **v1.14a - v1.14d**
   - The Base Mod will work perfectly, since these versions use the same text files as v1.13c.
 - **v1.10 - v1.12a**
   - The Base Mod will work, with the added advantage that these files will actually backport some of the fixes and new items added by v1.13. However, the new items will not display correctly, because their graphics are missing from older patches. This can be fixed by using the *Patch_D2.mpq* file from v1.13+.
 - **v1.09 and older**
   - These versions are incompatible with the Base Mod since they use older text files with different columns.

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

No; mods are not supported in Battle.net, only single-player games and TCP/IP.

### How is this project different from the other text file fixes out there?

It's not vastly different - this project simply combines several other fixes that are already available, and brings them up to date with the latest patches, so that mods can be made to target any version of the game without degrading functionality.

Care has been taken to include only changes that are balanced and true to the original game. For example, Nefarius' fixed 1.11b text files included an undocumented change that enabled an extremely overpowered item called the Constricting Ring; this change has not been included in the Base Mod.

Having the project on Github also makes it very easy to see precisely what's been changed in each file (the first commit contains just the clean text files, with no changes).

## Credits

 - Nefarius - for his fantastic work on the fixed 1.11b text files.
 - Count.Dracula - for his fixed 1.13c text files.
 - FearedBliss - for finding the bug with the Smith and Griswold's loot tables.

## Disclaimer

The unmodified game data is the intellectual property of *Blizzard Entertainment*.
