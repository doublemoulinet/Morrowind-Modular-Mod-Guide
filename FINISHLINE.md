# Finish Line

Congraulations! You're nearly there. This last section details a few quick steps to ensure a bug-free playthrough.

# Index
1. [Cleaning and Updating Plugins](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#cleaning)
1. [Load Order](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#load-order)
1. [Conflict Resolution](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#conflict-resolution)
	1. [Conflict Resolution Patch](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#conflict-resolution-patch)
	1. [Multipatch](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#multipatch)
	1. [Merged Objects](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#merged-objects)
1. [Distant Land](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#distant-land)
1. [Shaders](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#shaders)
1. [In-game Settings](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#in-game-settings)
	1. [MCM Settings](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#mcm-settings)
	1. [Menu Options](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#menu-options)
	1. [Mod Keybinds](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#mod-keybinds)


# Cleaning and Updating

## Plugin Cleaning
If you followed the cleaning advice as you installed each mod then you have already completed this section. Otherwise, run TESTool according to the instructions in [**Setup**](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md), and then the "clean with tes3cmd" utility in Wrye Mash for individual plugins. 

Please note that this may take some time. However, cleaning your plugins is absolutely necessary.

## Updating Masters Lists
Launch Wrye Mash. Go to the **Mods** tab for your list of plugins. If a plugin's checkbox colour is yellow the associated master file size does not match the plugin's. Follow these steps:
- Select the plugin and click the right pane (which lists the masters associated with the plugin). 
- Mash will prompt you to edit/update the masters list. Click **yes**. 
- Then click **save** at the bottom of the right pane.

# Load Order
Generally, ESPs should remain in the order that they were installed in this guide. However, in some cases  re-ordering is required.

Ensure the following plugins load *first* (i.e. at the very top) in your load order (the right pane of MO2), in this order:
1. Morrowind.esm
1. Tribunal.esm
1. Bloodmoon.esm
1. Patch for Purists.esm
1. Ownership Overhaul.esm
1. (Whatever ESMs installed in the CONTENT or LANDMASS EXPANSIONS section, ex OOAB_Data.esm or Tamriel_Data.esm)
1. Patch for Purists - Book Typos.esp
1. Patch for Purists - Semi-Purist Fixes.esp
1. Expansion Delay.esp
1. No More Stage Diving.esp
1. chuzei_helm_no_neck.esp
1. Descriptive Shrines.esp
1. Morrowind Anti-Cheese.esp
1. MDMD - More Deadly Morrowind Denizens.esp
1. MDMD - Creatures Add-on.esp

If you installed the **Content** section, you will need to move "Quorn Resource Integration.esp" higher in your load order, so that Yet Another Guard Diversity Overhaul and Mamaea Awakened overwrite its changes. Move "Quorn Resource Integration.esp" the other "New Items" plugins below the equipment ESPs from the **Visuals** section:
1. Hopesfire Torch (+ brighter trueflame).esp
1. Hircine's Artifacts.esp
1. Hunter's Mark.esp
1. Quorn Resource Integration.esp

Ensure that the following mods always load *last* (i.e. at the very bottom) in your load order:
1. Some of a Kind.esp
1. Conflict Resolution - Finish Line.esp
1. XE Sky Variations.esp
1. multipatch.esp
1. Merged Objects.esp

# Conflict Resolution
Several of the mods in this guide make edits to the same creatures and NPCs, and in some cases these changes will not be carried over and merged by the multipatch and merged patch. The following patch will resolve those conflicts and ensure the correct changes are carried forward into your merged patches in the next step of this guide.

You need to create two merged patches to resolve remaining plugin conflicts. Make sure all your plugins are enabled in the Mods Tab and follow these instructions to generate the patch

## Conflict Resolution Patch
1. [Conflict Resolution - Finish Line](https://mega.nz/file/70B23IKA#SRwTb-CnFroOY-q3bUFG-ze9AJmV3_7M_kpbHWafmKM)
	- Conflict resolution patch for MDMD - More Deadly Morrowind Denizens, Quorn Resource Integration, Some of a Kind, and Morag Tong Polished
	- Select one of the options based on your installation order and install. Make sure the plugin is enabled and at the bottom of your load order

## Multipatch
First, you need to create the **tes3cmd multipatch**:
1. Launch **tes3cmd** from your list of executables in MO2
1. In the command promt, type: "tes3cmd_multipatch.bat" without the quotation marks
1. Follow the prompts in the command-line window and wait for it to generate the patch
1. Once complete, tes3cmd will create multipatch.esp in your Overwrite folder in MO2

## Merged Objects
Next, create the **Merged Objects patch** with **TES3Merge**:
1. Launch TES3Merge.exe from your list of plugins in MO2 and wait for it to generate the plugin
1. Once complete, TES3Merge wil create Merged Objects.esp in your overwrite folder
1. Move the newly-created **Merged Objects.esp plugin** to the bottom of your load order (i.e. last)

Now we will move the two plugins to a new mod folder in the left pane. Select the mini-wrench-and-screwdriver icon next to the **Profiles** dropdown menu:
- Select **Create empty mod** and title it "**Merged Patches**"
- Double click the **Overwrite** folder at the bottom of your installation order
- Drag and drop the newly-created **multipatch.esp** and **Merged Objects.esp** to the empty mod and enable it

Note that you will need to regenerate these two plugins nearly each time you adjust your load order (update, remove or add a plugin) so that the changes are carried on. For your convenience, Wrye Mash will indicate if the plugins are missing masters and require regenerating (the plugin will turn yellow or red in the Mods Tab).

# Distant Land
Remember to re-run distant land generation according to the steps in [**Setup**](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md).

If you have installed **Remiros' Groundcover**, there are additional settings to check in MGE XE's distant land generation tab:
1. Depending on the method you followed during installation, ensure that the ESPs are enabled and appear in your load order. They should be at the very bottom (i.e. last)
1. If you installed the plugins to a separate folder (ex, \Data Files\Grass Plugins), you will need to specify this directory in the distant land generator wizard. Again, ensure the plugins are enabled and have a tick box in the wizard
1. On the "Create Distant Statics" tab, set **Grass Density** to 100% and click generate statics
	- Note: you can tweak this setting and re-generate distant land if the grass density affects performance. On my setup, 100% had no impact on framerate
1. After distant land generation completes, remember to disable the Remiros' Groundcover grass ESPs in your load order (if you did not create a "Grass Plugins" folder)

# Shaders
Remember to set up the mod-added shaders and enable them in the MGE XE shader tool. (If the following shaders don't appear in your shader list, that just means you didn't install the respective mods, and these instructions can be ignored):
- invisibility (from **Enhanced Invisibility** in **GAMEPLAY**)
- r0_qk_shader (from **Shattered Stones - an Earthquake Mod** in **GAMEPLAY**)
- warp (from **Expedition to Mzelthuand** in **CONTENT**)
- heathaze (from **Heat Haze** in **VISUALS**)

Add them to the bottom of the list of active shaders in MGE XE.

# In-game Settings
The final step. Nearly there...

## MCM Settings
Launch the game and enter the **Mod Configuration Menu** in the main menu. Some settings may require you to re-launch the game to take effect.

Note: unlike the Skyrim MCM, Morrowind MCM options will persist across every new game because settings are stored in .json config files in the MWSE folder in the root directory. You only need to make these settings changes once per installation.

### **Abot's Loading Door**
- Lock door with shift + activate = yes
### **Abot’s Smart Journal**
- Add a prefix in order to group quest name? = 0
- Sort quest list by name? = No
- Add quest id to quest hint? = No
- Add source mod name to quest hint = No
- Add source mod author… = No
- Open first URL… = No
### **Abot's Smart Merchants**
- Enable **Harder Barter like merchants buying prices reduction**: 2. Medium
### **Accidental Theft Protection**
- Blacklist: select the "Books" filter and click "filter all" in the right pane (this will allow you to read owned books without toggling sneak first).
	- You may also want to blacklist "Doors" if you haven't installed Ownership Overhaul
### **AURA**
- General Tab
	- No: Enable UI Module
	- No: Enable Containers Module
	- No: Enable PC Module
- Service Voices Tab
	- No: Enable voice comments on spells vendor service
### **Book Pickup**
- On by default? = No (use shift + e to pickup books without reading them)
### **Clock Block**
- Clock position=Bottom
- Clock type = Game time
### **Continue**
- Hide Credits Button = Yes
- Hide New Game Button (In Game) = Yes
- **Graphic Herbalism**
- Whitelist: 
	- ab_r_kwamaeggblighted
	- abtv_o_kweggblightedmm
- Blacklist:
	- _in_lib_scrolls*
	- ab_r_kwamstorager
### **Illegal Summoning**
- NPC Crime Trigger Distance = 2000
### **Let There Be Darkness**
- In the General and Cell Settings tab, set Cell Lighting Value Overrides to TLAD
- Leave the remaining settings at their defaults
### **Less Aggressive Creatures**
- Peaceful Chance: I recommend a value between 50-80% 
- Peaceful Creatures Whitelist: 
	```
	alit, 
	alit_diseased, 
	bm_horker, guar, 
	guar_feral, 
	h11_kwama_forager_dis, 
	h11_kwama_warrior_dis, 
	h11_netch_betty_dis, 
	h11_netch_bull_dis, 
	h11_rat_rust, 
	h11_slaughterfish_dis, 
	kagouti, 
	kagouti_diseased, 
	kwama forager, 
	kwama worker, 
	kwama worker diseased, 
	mudcrab, 
	mudcrab-diseased, 
	netch_betty, 
	netch_bull, 
	nix-hound, 
	rat, 
	rat_diseased, 
	scrib, 
	scrib_diseased, 
	shalk, 
	shalk_diseased, 
	slaughterfish, 
	slaughterfish_small
	```
### **Locks and Traps Detection**
- Set Visually Trapped Objects integration to "Yes"
### **Magicka Based Skill Progression**
- Skill Experience per Magicka: **0.05** (the default value is too high)
### **Magicka Regen**
- Set the player value to 50%
- Enable Magicka Decay: On
### **Miscast Enhanced**
- Ensure "Debug Mode" is disabled
### **Multi Mark & Harder Recall**
- Customize Limited Recall values
	- Recalls per day: 4
- *optional* Enable Miscast Enhanced integration!
### **No Translation Tooltips**
- Disable road sign tooltips: yes
- Disable banner tooltips: no
### **Ownership Indicator**
- Hide Crosshair = Yes (you may need to toggle the crosshair on/off in the game options menu to get this to work)
### **Poison Redux-ion**
- NO: Enable poison creation/application messages (toggle this on/off to use the poison crafting function)
- NO: Allow enemies to resist your poisons
- YES: Use Poison Crafting's additional icons and models
- NO: Use base stats for alchemy instead of fortified ones
### **Quick Loot**
- Hide lock status? = Yes
- Show quickloot menu on plant/organic containers? = No
### **Realistic Movement Speeds**
- Strafing Movement Percentage Multiplier = 100
### **Security Enhanced**
- Change the equip/cycle lockpick hotkey to "O" ("L" is used by Let There Be Darkness)
### **Simple Combat Mechancis**
- Disarmament: Disable (prevents NPCs from stealing bound weapons)
### **Sophisticated Save System**
- set up autosaves as you prefer, but recommend disabling “Create autosaves after changing cells”
### **The Midnight Oil**
- Toggle Static Lights only = No (this enables imperial lanterns to toggle in towns)
### **UI Expansion**
- Use verbose buttons instead of icons for inventory filtering? = No
### **Weapon Sheathing**
- Show unreadied shields on back = Yes!

## Menu Options
In the in-game menu Options set the following:

### **Prefs**
- Set difficulty to 0 (Dynamic Difficulty will handle scaling to keep things interesting--unless you want to punish yourself and play at 100 difficulty)
- Set **AI Distance** to the furthest left on the slider (decreasing the value improves performance but may break AI commands. I play with the AI slider set to the furthest left--this saves about 5-10 FPS in areas with lots of NPCs)
- Autosave when rest=OFF
- Always Use Best Attack=OFF (controversial opinion, but the direction-based attack types can be a pain--experiment and make up your own mind)
- Subtitles=ON

### **Controls**
- Use = mouse1
- activate=e
- Ready weapon=r
- Ready magic=f
- Jump=spacebar

### **Video**
- Set **Real-time shadows** to the middle of the slider (this is less for performance reasons than to reduce the incidence of buggy shadows through walls, etc.)

## Mod Keybinds
The following lists the keybinds set by the mods used in this guide:
- **C** - toggle equippable light source (from Torch Hotkey)
- **G** - precision object placement (from Perfect Placement)
- **K** - order companions to attack the target (from Kill Command)
- **L** - modders' tool, you won't need this (from Let There Be Darkness)
- **O** and **P** - toggle equip lockpicks, probes (from Security Enhanced)
- **Spacebar** and **left-ctrl** - z-axis movement when levitating or swimming (from Better Buoyancy)

Within the journal quest menu:
- **Shift** - hold and click quest names to highlight, hide, or unhide from the journal (from Better Questlist)

# The End
Hey, congratulations. You've made it to the end of the guide. Email Virgil if you have any questions or complaints. Enjoy the game!