[<< Previous section](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/OPTIONAL.md)
 | [Home](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide)

# Finish Line

Congraulations! You're nearly there. This last section details a few quick steps to ensure a bug-free playthrough.

# Index
1. [Cleaning Plugins](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#cleaning-plugins)
1. [Load Order](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#load-order)
1. [Registering BSAs](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#registering-bsas)
1. [Conflict Resolution](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#conflict-resolution)
	1. [Multipatch](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#multipatch)
	1. [Merged Objects](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#merged-objects)
	1. [Updating Masters](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#updating-masters)
1. [Re-running MCP](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#re-running-mcp)
1. [Distant Land](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#distant-land)
1. [Shaders](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#shaders)
1. [In-game Settings](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#in-game-settings)
	1. [Menu Options](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#menu-options)
	1. [MCM Settings](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#mcm-settings)
	1. [Mod Keybinds](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md#mod-keybinds)


# Cleaning Plugins
It's a fact of life: sometimes mod authors forget to clean their plugins. ESPs sometimes contain dirty references and your job is to squash these bugs. You will use Wrye Mash's integrated tes3cmd cleaning file.

<details>
<summary>Plugins that require cleaning</summary>

```
Bigger Velothi Temples.esp
Bloated Caves.esp
Divayth Fyr Puzzle Fixed.esp
Religions Elaborated.esp
FMI_Nice_to_Meet_You.esp
FMI_ServiceRefusal_Contraband.esp
What Thieves Guild.esp
mwse_PoisonCrafting.esp
TheMidnightOil.esp
RFD_Heartthrum.esp
Shattered Stones - An Earthquake Mod.esp
Atmospheric Delights.esp
RR_Gnisis_Arch_Eng.esp
RR_Aldruhn_Under_Skar_Eng.esp
Brevur of Balmora - Finally Some Good Statue Mod.ESP
Meteorite Ministry Temple.esp
Foyada Mamaea Overhaul.esp
OAAB - The Ashen Divide.esp
RR_Telvanni_Lighthouse_Tel Vos_Eng.esp
QL_SevenGracesShrines.esp
AndranoTombRemastered
Dura Gra-Bol's House Reclaimed.esp
Mage Robes.esp
Morag Tong Polished.esp
STOTSP TD Content Integration.esp
```
</details>

## Tes3cmd cleaning
Tes3cmd makes it easy to batch clean your plugins:
- Run **Wrye Mash** through MO2
- Navigate to the **Mods** Tab
- Right-click on the relevant plugin in the list and choose **clean with tes3cmd**
	- Note: you can **shift-click to select multiple plugins** and batch clean them

Mod Organizer 2 automatically updates your installed mod archives with your cleaned plugins. That's all!

>Not all plugins should be cleaned: some mods intentionally add duplicate (identical to master) records, which tes3cmd will mistakenly flag as "dirty" and clean. So don't ever clean **all** your plugins or you will have to redownload **Patch for Purists.esm**. (Don't clean ESMs).

# Load Order
Generally, plugins should remain in the order that they were installed in this guide. However, MO2 does not automatically place ESMs at the top of your load order--you must drag and drop these manually. This will have no impact in-game (the vanilla engine always loads ESMs before ESPs regardless their order in your mod manager).

Make sure your load order looks something like this:

<details>
<summary>Plugin Load Order</summary>

```
Morrowind.esm
Tribunal.esm
Bloodmoon.esm
Tamriel_Data.esm
OAAB_Data.esm
Patch for Purists.esm
Ownership Overhaul.esm
Solstheim Tomb of The Snow Prince.esm
Patch for Purists - Book Typos.ESP
Patch for Purists - Semi-Purist Fixes.ESP
TOTSP_Patch_for_Purists_4.0.2.esp
Lake Fjalding Anti-Suck.esp
chuzei_helm_no_neck.esp
No Thank You.esp
GITD_WL_RR_Interiors.esp
GITD_Telvanni_Dormers.ESP
The Dream is the Door.ESP
Hopesfire Torch (+ brighter trueflame).ESP
Keg Drip.ESP
mistify.ESP
Waterfalls Tweaks.esp
NearVanillaRoadSigns.esp
Beware the Sixth House.ESP
Bloodmoon Rebalance.esp
tribunal rebalance.ESP
Morrowind Anti-Cheese.ESP
There Can Be Only One (Alt Fyr).esp
Early Transport to Mournhold.esp
Expansion Delay.ESP
Expansions Integrated (Sigourn Edit).esp
Bigger Velothi Temples.esp
Bloated Caves.esp
Divayth Fyr Puzzle Fixed.ESP
Dubdilla Location Fix.ESP
Religions Elaborated.ESP
Services Restored.ESP
Silt Strider Animation Restored.ESP
Supply Chests.ESP
Synthesis Series - Creatures and Diseases.ESP
Temples With Shrines.ESP
The Publicans.ESP
Yet Another Guard Diversity - Regular.ESP
Hospitality_Papers_Expanded_v2.7.esp
FMI_Nice_to_Meet_You.ESP
FMI_#NotAllDunmer.ESP
FMI_ServiceRefusal_Contraband.ESP
Great Service.ESP
Greetings for No Lore.esp
Idle Talk.ESP
Its a deal.ESP
LDM - Context Matters.ESP
Nasty Camonna Tong.esp
outfit greetings tweaked.ESP
What Thieves Guild.ESP
Haunted Barrows.ESP
Outdoor Banners With Sound.ESP
Realistic_Repair_Add-on.ESP
Realistic_Repair_Add-on - PFP Patch.ESP
mwse_PoisonCrafting.esp
Magicka Expanded - Resource Pack.ESP
Enhanced Light.ESP
Clear Your Name.esp
Personal Effects_MWSE.ESP
Blight Is Coming.ESP
RFD_Heartthrum.ESP
TheMidnightOil.ESP
Shattered Stones - An Earthquake Mod.esp
OAAB Creature Loot.ESP
OAAB_GoldenReeds.ESP
OAAB Leveled Creatures.ESP
OAAB Leveled Lists.ESP
OAAB - Bloodmoon Rebalance Patch.ESP
OAAB Creature Loot - PFP Patch.ESP
OAAB - There Can Be Only One Patch.ESP
Atmospheric Delights.ESP
RR_Gnisis_Arch_Eng.ESP
Brevur of Balmora - Finally Some Good Statue Mod.ESP
Glass Domes of Vivec_atmospheric arena.esp
Glass Domes of Vivec_atmospheric arena Ownership Overhaul Patch.ESP
Meteorite Ministry Temple.ESP
OAAB_Grazelands.ESP
OAAB_Tel Mora.ESP
OAAB - Ownership Overhaul Extension.ESP
SarandasHall.ESP
Stav_gnisis_minaret_eng.esp
VEHK Palace.esp
Foyada Mamaea Overhaul.ESP
The Grove of Ben'Abi.ESP
OAAB - The Ashen Divide.ESP
RR_Telvanni_Lighthouse_Tel Branora_Eng.ESP
RR_Telvanni_Lighthouse_Tel Vos_Eng.ESP
QL_SevenGracesShrines.esp
ShrineOfAzura.ESP
Balmora Guilds Expanded.esp
Caldera Mages Guild Expanded.ESP
Vivec_Mages_Guild_Expanded.esp
Wolverine Hall Interior Expanded.esp
AndranoTombRemastered.esp
OAAB - Tombs and Towers.ESP
Samarys Ancestral Tomb Expanded.esp
Area Effect Projectiles Integrated.esp
Hircine's Artifacts.ESP
ABCs for Outlanders.ESP
Dura Gra-Bol's House Reclaimed.ESP
CultSheog.ESP
Mage Robes.ESP
Mamaea Awakened.ESP
Morag Tong Polished.ESP
OAAB - Astral Pocket.ESP
Plunder the Dungeon.ESP
The Sanguine Rose.ESP
Scrolls of The Nine Barriers.ESP
Umbra, Blademaster.ESP
[any other province mod ESPs]
multipatch.esp
Merged Objects.esp
```
</details>

## Load Order Backup
Finally, make a backup of both your installation order and your load order (this is in the event that MO2 crashes and purges your load order):
1. In the right pane of MO2, click the harddisk icon. A text popup "Backup of load order created" should appear at the bottom of the MO2 interface
1. In the left pane of MO2, click the harddisk icon. A text popup "Backup of mod list created" should appear at the bottom of the MO2 interface.

# Registering BSAs 
Some mods include packaged archives called BSAs. **Tamriel Rebuilt** and **Skyrim: Home of the Nords** are dependent on the BSAs in **Tamriel Data**. You must register them in order for the assets to show up in-game.

- Launch **Wrye Mash** from within MO2
- Go to the **Mods Tab**
- The right-pane has two tabs for **Mod Details** and **BSA Archives**
- Select the **BSA Archives** tab and ensure each listed BSA has a check mark

This ensures the game will load the assets archives in these files. The three vanilla BSAs should already be registered; you may have to check **TR_Data** and **PT_Data** if you followed the optional [**Landmass Expansions**](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/OPTIONAL.md) section of this guide.

# Conflict Resolution
You need to create two merged patches to resolve remaining plugin conflicts. Make sure all your plugins are enabled in the Mods Tab and follow these instructions to generate the patch

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

- Launch **Wrye Mash** from within MO2 
- Go to the **Mods** tab for your list of plugins
- If a plugin's checkbox colour is yellow the associated master file size does not match the plugin's, follow these steps:
	- Select the plugin and click the right pane (which lists the masters associated with the plugin)
	- Mash will prompt you to edit/update the masters list. Click **yes**. 
	- Then click **save** at the bottom of the right pane

You should repeat this process anytime you update common master plugins like Patch for Purists, Tamriel Data, or OAAB Data.

# Re-running MCP
There are a few additional **Morrowind Code Patch** options you can enable, depending on which mods you installed during the course of this guide.

If you installed the [Gameplay - Expanded](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/GAMEPLAY.md) section, follow these instructions:
- In your Root Folder, run **Morrowind Code Patch.exe** as an Administrator
- Enable the following options:
	- **Game Mechanics**: enable *"Attribute Uncap"*, and *"Skill Uncap"*
- Click the big "Apply chosen patches" button and exit


# Distant Land
The Distant Land tab does what it says: it generates the distant land that, in-game, allows you to see past the currently rendered cell.

- Launch **MGE XE** from your list of executables.
- Navigate to the **Distant land** tab in **MGE XE**

Most options are disabled when you first open this tab. You need to generate distant land for these options to become accessible. The **Distant land generator wizard** lets you select which plugins MGE XE will use when generating distant land, and will guide us through the process:
- Click the **Distant land generator wizard** button
- On the **Distant Land Setup Wizard**, click **Select all**. These ticked plugins will be used in distant land generation
	- *Optional step*: If you installed **Remiros' Groundcover** to a separate folder (for example, ```Data Files\Grass Plugins```) you must specify this directory
		- Select **plugin directories...** and navigate to your grass plugins folder
		- Select the folder, click **Add** and then **Save**
- Click **Continue**. This will open the next window
- In the **Land Textures** tab:
	- Set **World texture resolution** to 2048
	- Set **World normalmap resolution** to 1024
	- Click **Create Land Textures**
- In the **Land Meshes** tab:
	- Set **World mesh detail** to **Ultra High** in the dropdown menu
	- Click **Create Land Meshes**
- In the **Statics** tab:
	- Set **Minimum static size** to **150**
	- Set **Grass density** to **100%**
		- *Note*: grass density is GPU-intensive. On weaker graphics cards, you may have to reduce this setting.
	- Set **Mesh detail level** to **Full**
	- Set **Distant texture reduction** to **1/2**
	- Tick **all** the right-hand options *except* **include reflective water in interiors**
	- Click **Create Statics**
- Once the process completes, click **Finish**

Generally, you should regenerate your distant land any time you install or uninstall mods with plugins. Fortunately, this process will be much simpler as you will only need to click on **Run above steps using saved / default settings** the next time you use the **Distant land generator wizard**.

![Screenshot](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/assets/MGEXE_distantland.jpg)

After MGE XE has generated distant land, you will be returned to the **Distant Land** tab from earlier. Now, all the previously unavailable options can be set up. Follow the settings as suggested in the screenshot above. You may wish to tinker with them later. These recommended settings cleave to the game's original foggy aesthetic and keep performance costs to a minimum.

### **Optional step: creating a distantland mod folder**
You may optionally move your newly-generated Distant Land files from their default location in the Mod Organizer 2 "Overwrite" folder:
1. Exit MGE XE and return to the MO2 interface
1. Located to the right of the Profile drop-down menu, click the small hammer-and-wrench icon and select "Create Empty Mod"
1. Name this mod "Distant Land - Vanilla" and make sure it is at the bottom of your load order
1. At the bottom of your load order, double click on the "Overwrite" folder
1. Drag and drop the "distantland" folder into the empty mod

The advantage of this step is that you can easily toggle between different mod profiles without regenerating distantland each time. Simply repeat distantland generation for your other profiles.

>Any time you regenerate your distant land it will automatically update and replace the files in the "Distant Land - Modular" mod, assuming you leave it enabled in the left-pane. This means you will only have to perform this step *once*! 

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
Launch the game and enter the in-game Options menu.
>Remember: just like all your modding executables, you must also run **Morrowind.exe** via Mod Organizer 2!

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

# MCM Settings
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
### **Adjustable Landscape Texture Scale**
- If using vanilla textures: leave at **160%**
- If using **HD textures**: set to **140%**
### **AURA**
- Main Settings
	- No: Interior Ambient
	- No: Populated Ambient
	- No: Enable UI Module
	- No: Enable Containers Module
	- No: Enable PC Module
### **Book Pickup**
- On by default? = No (use shift + e to pickup books without reading them)
### **Character Sound Overhaul**
- Movement Settings Tab
	- Enable Alternative Armor Weight Mechanic: ON
- Misc Sound Settings Tab
	- Enable Vanilla Thumps: ON
### **Clock Block**
- Clock position=Bottom
- Clock type = Game time
### **Continue**
- Hide Credits Button = Yes
- Hide New Game Button (In Game) = Yes
### **GMST Menu**
- Search these strings and adjust the values:
	```
	i1stPersonSneakDelta = 30
	iGreetDistanceMultiplier = 5
	```
- Optionally, change the GMSTs governing projectiles:
	
	```
	Faster projectiles:
	fProjectileMaxSpeed = 7200
	fProjectileMinSpeed = 960
	fThrownWeaponMaxSpeed = 1200
	fThrownWeaponMinSpeed = 360

	Higher projectile recovery chance:
	fProjectileThrownStoreChance 80

	Faster magic missiles:
	fTargetSpellMaxSpeed 1200
	```

### **HUD Weapon Charge**
- Fillbar thickness: 7
### **Let There Be Darkness**
- General and Cell Settings:
	- Cell Lighting Value Overrides: True Lights and Darkness
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
### **Security Enhanced**
- Change the equip/cycle lockpick hotkey to "O" ("L" is used by Let There Be Darkness)
- Set auto-equip options to OFF
### **Sophisticated Save System**
- set up autosaves as you prefer, but recommend disabling “Create autosaves after changing cells”
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

[<< Previous section](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/OPTIONAL.md)
 | [Home](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide)