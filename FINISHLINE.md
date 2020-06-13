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
1. Once complete, TES3Merge wil create Merged Objects.esp in your Data Files. 

Note that you will need to regenerate these two plugins each time you adjust your load order (update, remove or add a plugin) so that the changes are carried on. For your convenience, Wrye Mash will indicate if the plugins are missing masters and require regenerating (the plugin will turn red in the Mods Tab).

## Merging
If you have installed new weapon/item mods and would like to reduce the plugin count, you can use MWedit to open all these plugins simultaneously and merge them into a new plugin (I usually call mine "Unique Items Merged.esp"). Remember to clean any created plugins with TESTool and tes3cmd.

As a rule, don't merge ESPs with scripts.

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

## Shaders
Remember to set up the modd-added shaders and enable them in the MGE XE shader tool:
- invisibility
- r0_qk_shader
- warp

Add them to the bottom of the list of active shaders in MGE XE.

## In-game Settings

### Menu Options
In the in-game menu Options set the following:

**Prefs**
- Set difficulty to 0 (Dynamic Difficulty will handle scaling to keep things interesting--unless you want to punish yourself and play at 100 difficulty)
- Set **AI Distance** to the furthest right on the slider (decreasing the value improves performance but may break AI commands. I play with the AI slider set to the furthest left--this saves about 5-7 FPS in areas with lots of NPCs) 
- Autosave when rest=OFF
- Always Use Best Attack=OFF (controversial opinion, but the direction-based attack types can be a pain--experiment and make up your own mind)
- Subtitles=ON

**Controls**
- Use = mouse1
- activate=e
- Ready weapon=r
- Ready magic=f
- Jump=spacebar

### MCM Settings
The final step. Launch the game and enter the **Mod Configuration Menu** in the main menu. Some settings may require you to re-launch the game to take effect.

Note: unlike the Skyrim MCM, Morrowind MCM options will persist across every new game because settings are stored in .json config files in the MWSE folder in the root directory. You only need to make these settings changes once.

- Abot's Loading Door
	- Lock door with shift + activate = yes
- Abot’s Smart Journal
	- Add a prefix in order to group quest name? = 0
	- Sort quest list by name? = No
	- Add quest id to quest hint? = No
	- Add source mod name to quest hint = No
	- Add source mod author… = No
	- Open first URL… = No
- Accidental Theft Protection
	- Blacklist: select the "Books" filter and click "filter all" in the right pane (this will allow you to read owned books without toggling sneak first).
- Book Pickup
	- On by default? = No (use shift + e to pickup books without reading them)
- Clock Block
	- Clock position=Bottom
	- Clock type = Game time
- Continue
	- Hide Credits Button = Yes
	- Hide New Game Button (In Game) = Yes
- Graphic Herbalism
	- In order for **Immersive Mining** to work with GH, set up a blacklist to block all ore activators:
		- In the Blacklist tab, navigate to the Objects list and search “mine”
		- Click Toggle Filtered to add these objects to the blacklist
		- Repeat these steps for the keyword "rock"
	- You can toggle off Immersive Mining's gameplay changes by undoing these blacklist changes
- Illegal Summoning
	- NPC Crime Trigger Distance = 2000
- Miscast Enhanced
	- Ensure "Debug Mode" is disabled
- Multi Mark & Harder Recall
	- Customize Limited Recall values
		- Recalls per day: 4
	- *optional* Enable Miscast Enhanced integration!
- Ownership Indicator
	- Hide Crosshair = Yes (you may need to toggle the crosshair on/off in the game options menu to get this to work)
- Quick Loot
	- Hide lock status? = Yes
	- Show quickloot menu on plant/organic containers? = No
- Realistic Movement Speeds
	- Strafing Movement Percentage Multiplier = 100
- Sophisticated Save System
	- set up autosaves as you prefer, but recommend disabling “Create autosaves after changing cells”
- UI Expansion
	- Use verbose buttons instead of icons for inventory filtering? = No
- Weapon Sheathing
	- Show unreadied shields on back = Yes!