# Finish Line

Congraulations! You're nearly there. This last section details a few quick steps to ensure a bug-free playthrough.

## Cleaning
If you followed the cleaning advice as you installed each mod then you have already completed this section. Otherwise, run TESTool according to the instructions in [**Setup**](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md), and then the tes3cmd_clean.bat for individual plugins.

## Multipatch and Merged Patch
You need to create two merged patches to resolve plugin conflicts.

First, you need to create the tes3cmd multipatch:
1. Click the tes3cmd_multipatch.bat in your Data Files (you created this in [**Setup**](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md))
1. Follow the instructions/prompts in the command-line window
1. Once complete, tes3cmd will create multipatch.esp in your Data Files
 
Next, create the Merged Objects patch with TES3Merge:
1. Launch TES3Merge.exe and follow the prompts
1. Once complete, TES3Merge wil create Merged Objects.esp in your Data Files
Note that you will need to regenerate these two plugins each time you adjust your load order (update, remove or add a plugin) so that the changes are carried on. For your convenience, Wrye Mash will indicate if the plugins are missing masters and require regenerating (the plugin will turn red in the Mods Tab).

## Merging
If you have installed new weapon/item mods and would like to reduce the plugin count, you can use MWedit to open all these plugins simultaneously and merge them into a new plugin (I usually call mine "Unique Items Merged.esp"). Remember to clean any created plugins with TESTool and tes3cmd.

## Load order and Late Loaders
Run mlox.exe and allow it to make changes.

Ensure that the following mods always load last in your load order:
1. Yet Another Guard Diversity - Regular.esp
1. Urnest Loot.esp
1. There Can Be Only One.esp
1. Morrowind Anti-Cheese.esp
1. XE Sky Variations.esp
1. multipatch.esp
1. Merged Objects.esp

## Distant Land Generation
Remember to re-run distant land generation according to the steps in [**Setup**](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md).

## In-game MCM Settings
The final step. Launch the game and enter the **Mod Configuration Menu** in the main menu. Some settings may require you to re-launch the game to take effect.

Note: unlike the Skyrim MCM, Morrowind MCM options will persist across every new game because settings are stored in .json config files in the MWSE folder in the root directory. You only need to make these settings changes once.

	- Graphic Herablism: blacklist ores for immersive mining compat
	- Realistic Movement Speeds strafing to 100