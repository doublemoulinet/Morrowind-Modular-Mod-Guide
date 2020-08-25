# Finish Line

Congraulations! You're nearly there. This last section details a few quick steps to ensure a bug-free playthrough.

## Cleaning
If you followed the cleaning advice as you installed each mod then you have already completed this section. Otherwise, run TESTool according to the instructions in [**Setup**](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md), and then the tes3cmd_clean.bat for individual plugins.

## Multipatch and Merged Patch
You need to create two merged patches to resolve plugin conflicts.

### Multipatch
First, you need to create the **tes3cmd multipatch**:
1. Click the tes3cmd_multipatch.bat in your Data Files (you created this in [**Setup**](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md))
1. Follow the instructions/prompts in the command-line window
1. Once complete, tes3cmd will create multipatch.esp in your Data Files

The multipatch erroneously edits four levelled lists affected by the Daedric rarity mod "Some of a Kind." Open TESAME and open the multipatch.esp. Filter by type and select the following four "Lev Item" entries and delete them (right click the entries and hit the delete key on your keyboard):
1. l_m_enchantitem_temple_rank8_2
1. random excellent melee weapon
1. random_Golden_saint_weapon
1. random_Golden_saint_shield

Save the edited plugin by choosing "save as" and overwriting the original plugin. In Wrye Mash's Mods Tab, ensure the multipatch.esp plugin is at the bottom of your load order. **NOTE:** You will have to do this each time you regenerate your multipatch.

###Merged Objects
Next, create the **Merged Objects patch** with **TES3Merge**:
1. Launch TES3Merge.exe and follow the prompts
1. Once complete, TES3Merge wil create Merged Objects.esp in your Data Files. 

Note that you will need to regenerate these two plugins nearly each time you adjust your load order (update, remove or add a plugin) so that the changes are carried on. For your convenience, Wrye Mash will indicate if the plugins are missing masters and require regenerating (the plugin will turn yellow or red in the Mods Tab).

## Merging
If you have installed new weapon/item mods and would like to reduce the plugin count, you can use MWedit to open all these plugins simultaneously and merge them into a new plugin (I usually call mine "Unique Items Merged.esp"). Remember to clean any created plugins with TESTool and tes3cmd.

As a rule, don't merge ESPs with scripts.

## Load order and Late Loaders
Generally, ESPs should remain in the order that they were installed in this guide. 

Additional re-ordering may be required. Ensure the following load *first* in your load order:
1. (Whatever ESMs you have enabled, ending with "Patch for Purists.esm")
1. (If you've installed HOTV Solstheim, make sure the ESM loads AFTER Patch for Purists.esm)
1. Patch for Purists - Book Typos.esp
1. Patch for Purists - Semi-Purist Fixes.esp
1. Morrowind Anti-Cheese.esp
1. Ownership Overhaul.esp

If you installed the **Content** section, you will need to move "Quorn Resource Integration.esp" higher in your load order, so that YAGD and Mamaea Awakened overwrite its changes. Move "Quorn Resource Integration.esp" and "Hunter's Mark.esp" below the unique item ESPs from the **Visuals** section:
1. Complete Armor Joints.esp
1. chuzei_helm_no_neck.esp
1. [Unique Item ESPS or the Unique Item Merged ESP]
1. Quorn Resource Integration.esp
1. Hunter's Mark.esp
[...]
1. Yet Another Guard Diversity Overhaul.esp
1. Mamaea Awakened.esp

Ensure that the following mods always load *last* in your load order:
1. Some of a Kind.esp
1. What is something that is too long for an ESP name.esp
1. XE Sky Variations.esp
1. multipatch.esp
1. Merged Objects.esp

## Distant Land Generation
Remember to re-run distant land generation according to the steps in [**Setup**](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md).

## Shaders
Remember to set up the mod-added shaders and enable them in the MGE XE shader tool. (If the following shaders don't appear in your shader list, that just means you didn't install the relevant mod, so you're fine!):
- invisibility (from Enhanced Invisibility)
- r0_qk_shader (from Shattered Stones - an Earthquake Mod)
- warp (from Expedition to Mzelthuand)

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
	- Blacklist: select the "Books" filter and click "filter all" in the right pane (this will allow you to read owned books without toggling sneak first). You may also want to blacklist "Doors" if you haven't installed Ownership Overhaul
- Book Pickup
	- On by default? = No (use shift + e to pickup books without reading them)
- Clock Block
	- Clock position=Bottom
	- Clock type = Game time
- Continue
	- Hide Credits Button = Yes
	- Hide New Game Button (In Game) = Yes
- Illegal Summoning
	- NPC Crime Trigger Distance = 2000
- Let There Be Darkness
	- In the General and Cell Settings tab, set Cell Lighting Value Overrides to TLAD
	- Leave the remaining settings at their defaults
- Magicka Based Skill Progression
	- Leave the Skill Experience per Magicka at default, or adjust as desired if magic skills are advancing too quickly.
- Miscast Enhanced
	- Ensure "Debug Mode" is disabled
- Multi Mark & Harder Recall
	- Customize Limited Recall values
		- Recalls per day: 4
	- *optional* Enable Miscast Enhanced integration!
- No Translation Tooltips
	- Disable road sign tooltips: yes
	- Disable banner tooltips: no
- Ownership Indicator
	- Hide Crosshair = Yes (you may need to toggle the crosshair on/off in the game options menu to get this to work)
- Quick Loot
	- Hide lock status? = Yes
	- Show quickloot menu on plant/organic containers? = No
- Realistic Movement Speeds
	- Strafing Movement Percentage Multiplier = 100
- Security Enhanced
	- Change the equip/cycle lockpick hotkey to "O" ("L" is used by Let There Be Darkness)
- Smart Merchants
	- Enable **Harder Barter like merchants buying prices reduction**: 2. Medium
- Sophisticated Save System
	- set up autosaves as you prefer, but recommend disabling “Create autosaves after changing cells”
- UI Expansion
	- Use verbose buttons instead of icons for inventory filtering? = No
- Weapon Sheathing
	- Show unreadied shields on back = Yes!