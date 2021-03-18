# Finish Line

Congraulations! You're nearly there. This last section details a few quick steps to ensure a bug-free playthrough.

# Index
1. [Cleaning Plugins](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#cleaning-plugins)
1. [Load Order](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#load-order)
1. [Conflict Resolution](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#conflict-resolution)
	1. [Conflict Resolution Patch](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#conflict-resolution-patch)
	1. [Multipatch](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#multipatch)
	1. [Merged Objects](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#merged-objects)
	1. [Updating Masters](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#updating-masters)
1. [Distant Land](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#distant-land)
1. [Shaders](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#shaders)
1. [In-game Settings](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#in-game-settings)
	1. [Menu Options](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#menu-options)
	1. [MCM Settings](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#mcm-settings)
	1. [Mod Keybinds](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#mod-keybinds)


# Cleaning Plugins

If you followed the cleaning advice as you installed each mod then you have already completed this section. Otherwise, run TESTool according to the instructions in [**Setup**](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md), and then the "clean with tes3cmd" utility in Wrye Mash for individual plugins. 

Please note that this may take some time. However, cleaning your plugins is absolutely necessary.

# Load Order
Generally, ESPs should remain in the order that they were installed in this guide. However, in some cases re-ordering is required.

Ensure the following plugins load *first* (i.e. at the very top) in your load order (the right pane of MO2), in this order:
1. Morrowind.esm
1. Tribunal.esm
1. Bloodmoon.esm
1. *Tamriel_Data.esm ```(installed in LANDMASS)```
1. *OAAB_Data.esm  ```(installed in CONTENT)```
1. Patch for Purists.esm
1. Ownership Overhaul.esm
1. *TR_Mainland.esm ```(installed in LANDMASS)```
1. *Sky_Main.esm ```(installed in LANDMASS)```
1. *Solstheim Tomb of the Snow Prince.esm ```(installed in LANDMASS)```
1. [**Any other ESMs** in your load order]
1. Patch for Purists - Book Typos.esp
1. Patch for Purists - Semi-Purist Fixes.esp
1. Expansion Delay.esp
1. No More Stage Diving.esp
1. chuzei_helm_no_neck.esp
1. Descriptive Shrines.esp
1. Morrowind Anti-Cheese.esp
1. MDMD - More Deadly Morrowind Denizens.esp
1. MDMD - Creatures Add-on.esp

Ensure that the following mods always load *last* (i.e. at the very bottom) in your load order:
1. There Can Be Only One (Alt Fyr).esp
1. Conflict Resolution.esp ```(installed in the next step)```
1. XE Sky Variations.esp
1. multipatch.esp ```(created in the next step)```
1. Merged Objects.esp ```(created in the next step)```

### Load Order Backup
Finally, make a backup of both your installation order and your load order (this is in the event that MO2 crashes and purges your load order):
1. In the right pane of MO2, click the harddisk icon. A text popup "Backup of load order created" should appear at the bottom of the MO2 interface
1. In the left pane of MO2, click the harddisk icon. A text popup "Backup of mod list created" should appear at the bottom of the MO2 interface.

# Conflict Resolution
Several of the mods in this guide make edits to the same creatures and NPCs, and in some cases these changes will not be carried over and merged by the multipatch and merged patch. The following patch will resolve those conflicts and ensure the correct changes are carried forward into your merged patches in the next step of this guide.

You need to create two merged patches to resolve remaining plugin conflicts. Make sure all your plugins are enabled in the Mods Tab and follow these instructions to generate the patch

## Conflict Resolution Patch
1. [Conflict Resolution - Finish Line](https://mega.nz/file/nxw2jCKb#4Bmon9XoNNM4xDHLRchumq6F6yuA_fwAqlMvjxnBAqQ)
	- Conflict resolution patch for MDMD - More Deadly Morrowind Denizens,  There Can Be Only One, OAAB Integrations, Quorn Resource Integration, Immersive Madness, and Morag Tong Polished
	- Select one of the options based on your installation order and install.
		- Users who skipped the CONTENT module: use "MDMD + There Can Be Only One"
		- Users who installed the full CONTENT module: use "OAAB + MDMD + There Can Be Only One + MT Polished + Immersive Madness"
	- Make sure the plugin is enabled and at the bottom of your load order

## Multipatch
First, you need to create the **tes3cmd multipatch**:
1. Launch **tes3cmd** from your list of executables in MO2
1. In the command promt, type: "tes3cmd_multipatch.bat" without the quotation marks
1. Follow the prompts in the command-line window and wait for it to generate the patch
1. Once complete, close tes3cmd. Tes3cmd will create multipatch.esp in your Overwrite folder in MO2

## Merged Objects
Next, create the **Merged Objects patch** with **TES3Merge**:
1. Launch TES3Merge.exe from your list of plugins in MO2 and wait for it to generate the plugin
1. Once complete, TES3Merge will auto-close and create Merged Objects.esp in your overwrite folder

Now we will move the two plugins to a new mod folder in the left pane. Select the mini-wrench-and-screwdriver icon next to the **Profiles** dropdown menu:
- Select **Create empty mod** and title it "**Merged Patches**"
- Double click the **Overwrite** folder at the bottom of your installation order
- Drag and drop the newly-created **multipatch.esp** and **Merged Objects.esp** to the empty mod and enable it
- Move the two plugins to the bottom of your load order, with **Merged Objects.esp** loading last

Note that you will need to regenerate these two plugins nearly each time you adjust your load order (update, remove or add a plugin) so that the changes are carried on. For your convenience, Wrye Mash will indicate if the plugins are missing masters and require regenerating (the plugin will turn yellow or red in the Mods Tab).

## Updating Masters
Wrye Mash can synchronize the master dependencies of your plugins, correcting for when masters are out of the expected order or file size. This prevents error messages on startup.

Launch Wrye Mash. Go to the **Mods** tab for your list of plugins. If a plugin's checkbox colour is yellow the associated master file size does not match the plugin's. Follow these steps:
- Select the plugin and click the right pane (which lists the masters associated with the plugin). 
- Mash will prompt you to edit/update the masters list. Click **yes**. 
- Then click **save** at the bottom of the right pane.

You should repeat this process anytime you update common master plugins like Patch for Purists, Tamriel Data, or OAAB Data.

# Distant Land
You will need to regenerate your distant land. If you followed the steps in [**Setup**](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md) this will be considerably easier:

1. **Untick** the "Distant Land - Vanilla" mod you created in the Setup section
1. Launch MGE XE in MO2
1. In the "Distant Land" tab launch the "Distant land generator"
1. On the "Plugins" tab, click "Select All"

If you have installed **Remiros' Groundcover**, there are additional settings to check in MGE XE's distant land generation tab:
1. Depending on the method you followed during installation, ensure that the ESPs are enabled and appear in your load order. They should be at the very bottom (i.e. last)
1. *If you installed the plugins to a separate folder (ex, \Data Files\Grass Plugins)*: 
	- select "plugin directories..." to add this folder to the plugin list
	- Click "Add" and select your "Grass Plugins" folder
	- Be sure to click "Save" and then confirm that the plugins are all ticked in the plugin list (you may have to click "Select All" again)
1. With all your plugins loaded, click *Run above steps using saved/default settings* and wait for the process to complete
	- Note: you can tweak the settings and re-generate distant land if the grass density affects performance. On my setup, the default 100% density had no impact on framerate
1. *If you did not create a "Grass Plugins" folder*: after distant land generation completes, remember to disable the Remiros' Groundcover grass ESPs in the right-pane (your load order)

### **Optional step: create a distant land mod folder**
Optionally, you may create a new mod for your modded game's distant land:
1. Exit MGE XE and return to the MO2 interface
1. Located to the right of the Profile drop-down menu, click the small hammer-and-wrench icon and select "Create Empty Mod"
1. Name this mod "Distant Land - Modular" or something distinct, and make sure it is at the bottom of your load order
1. At the bottom of your load order, double click on the "Overwrite" folder
1. Drag and drop the "distantland" folder into the empty mod
1. Tick the mod to enable it

If you also followed this optional step during the [**Setup**](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md) section, you can untick "Distant Land - Vanilla" (or whatever you named the mod) in MO2's left pane.

Note: any time you regenerate your distant land it will automatically update and replace the files in the "Distant Land - Modular" mod, assuming you leave it enabled in the left-pane. This means you will only have to perform the above steps *once*! 

# Shaders
Remember to set up the mod-added shaders and enable them in the MGE XE shader tool. (If the following shaders don't appear in your shader list, that just means you didn't install the respective mods, and these instructions can be ignored):
- invisibility (from **Enhanced Invisibility** in **GAMEPLAY**)
- r0_qk_shader (from **Shattered Stones - an Earthquake Mod** in **GAMEPLAY**)
- warp (from **Expedition to Mzelthuand** in **CONTENT**)
- heathaze (from **Heat Haze** in **VISUALS**)

Add them to the bottom of the list of active shaders in MGE XE.

# In-game Settings
The final step. Nearly there...

## Menu Options
Launch the game and enter the in-game Options menu. Adjust the following:

### **Prefs**
- Set difficulty to 0 (Dynamic Difficulty will handle scaling to keep things interesting--unless you want to punish yourself and play at 100 difficulty from the start)
- Set **AI Distance** to the furthest right on the slider (decreasing the value improves performance but may break AI commands. I play with the AI slider set to the furthest left--this saves about 5-10 FPS in areas with lots of NPCs, but will break some follower quests)
- Autosave when rest=OFF
- Always Use Best Attack=OFF
- Subtitles=ON

## Audio
- Turn the Music slider all the way down and let this AURA's ambient soundscapes transport you... Strongly recommended.

### **Controls**
- Use = mouse1
- activate=e
- Ready weapon=r
- Ready magic=f
- Jump=spacebar

### **Video**
- Set **Real-time shadows** to OFF, i.e. the slider all the way to the left (this is  for performance reasons as well as to reduce the incidence of buggy shadows through walls, etc.).

## MCM Settings
From the in-game menu, select the **Mod Configuration Menu**. Note: some settings may require you to re-launch the game to take effect.

Unlike the Skyrim MCM, Morrowind MCM options will persist across every new game because settings are stored in .json config files in the MWSE folder in the root directory. You only need to make these settings changes once per installation.

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
- Select the "Doors" filter and click "filter all" in the right pane (this is largely a preecaution, since Ownership Overhaul should fix all vanilla game door ownership)
### **AURA**
- Main Settings
	- No: Interior Ambient
	- No: Populated Ambient
	- No: Enable UI Module
	- No: Enable Containers Module
	- No: Enable PC Module
### **Book Pickup**
- On by default? = No (use shift + e to pickup books without reading them)
### **Clock Block**
- Clock position=Bottom
- Clock type = Game time
### **Continue**
- Hide Credits Button = Yes
- Hide New Game Button (In Game) = Yes
### **Illegal Summoning**
- NPC Crime Trigger Distance = 2000
### **Let There Be Darkness**
- In the General and Cell Settings tab, set Cell Lighting Value Overrides to TLAD
- Leave the remaining settings at their defaults
### **Less Aggressive Creatures**
- Peaceful Chance: I recommend a value between 50-70% 
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
- Skill Experience per Magicka: **0.2** (the default value is too high)
### **Magicka Regen**
- Set the player value to 50%
- Enable Magicka Decay: On
### **Miscast Enhanced**
- Ensure "Debug Mode" is disabled
### **Multi Mark & Harder Recall**
- Enable Limited Recall: No
- Enable Miscast Enhanced integration: Yes
### **No More Friendly Fire**
- Blacklist: add "Hlormar Wine-Sot" (corrects an interaction between this mod and a vanilla quest)
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
- Show quickloot menu on plant/organic containers? = No (Graphic Herbalism's tooltip is superior)
- Show vanilla container tooltip = yes 
	- (will cause redundant tooltips but resolves an edge-case issue when the quickloot menu is disabled for improperly flagged-as-organic containers)
### **Security Enhanced**
- Change the equip/cycle lockpick hotkey to "O" ("L" is used by Let There Be Darkness)
- Set auto-equip options to OFF
### **Sophisticated Save System**
- set up autosaves as you prefer, but recommend disabling “Create autosaves after changing cells”
### **Soulless Creatures**
- add the following to the blocked list:
	- bonewalker_greater_summ, 
	- fsheog_cr_haki3summon
	- oj_me_summalfiqcrea
### **The Midnight Oil**
- Toggle Static Lights only = No (this enables imperial lanterns to toggle in towns)
### **UI Expansion**
- Use verbose buttons instead of icons for inventory filtering? = No
### **Weapon Sheathing**
- Show unreadied shields on back = Yes!

## In-game Settings
The last step is to open the in-game console and adjust the formula for earthquake chances in "Shattered Stones." Open the console (~) and type: ```set fQuakeChance to 10```

## Mod Keybinds
The following lists the keybinds set by the mods used in this guide:
- **B** - toggle closed/open book covers and scrolls (from Switchable Scriptures)
- **C** - toggle equippable light source (from Torch Hotkey)
- **G** - precision object placement (from Perfect Placement)
- **K** - order companions to attack the target (from Kill Command)
- **L** - modders' tool, you won't need this (from Let There Be Darkness)
- **O** and **P** - toggle equip lockpicks, probes (from Security Enhanced)
- **X** and **Z** - Take-all, and open container/alternate activate key (from Quickloot)
- **Spacebar** and **left-ctrl** - z-axis movement when levitating or swimming (from Better Buoyancy)
- **Shift** plus **activate** - instant book pickup (from Book Pickup)
- **Ctrl** plus **activate** - alchemy apparatus worldspace activation (from Poison Redux-ion)

Within the journal quest menu:
- **Shift** - hold and click quest names to highlight, hide, or unhide from the journal (from Better Questlist)

# The End
Hey, congratulations. You've made it to the end of the guide. Email Virgil if you have any questions or complaints. Enjoy the game!