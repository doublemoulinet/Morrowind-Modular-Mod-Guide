# Optional Early Loaders
These optional mods should not be used on your first playthrough. The **Official Plugins** are a real grab bag--some are mediocre, others are trivial, most are best forgotten. The cleaned and fixed versions presented here are the best way to incorporate them into your game, but are not necessary (or even recommended) for an enjoyable Morrowind experience. In fact, let me put this another way: I strongly discourage using any of the Offical Plugins. Just don't.

The landmass mods--**Tamriel Rebuilt** and its sister projects like **Skyrim: Home of the Nords**--are highly recommended on subsequent playthroughs. These are arguably the most impressive modding projects on the web. Tamriel Rebuilt is a decades-long project to recreate the Morrowind mainland in TES3. The "Old Ebonheart" release is one of the best quest mods available and I recommend a TR-centric playthrough to play the different questlines.

**Solstheim Tomb of the Snow Prince** overhauls the Bloodmoon expansion to bring the world design in line with current Tamriel Rebuilt / Project Tamriel design standards. It is highly recommended. You will see why after you play Bloodmoon in vanilla: the vanilla world design is flat, empty, and boring. STOTSP is a performance-friendly overhaul that makes playing Bloodmoon significantly more fun.

**Important**: if you install the Unofficial Plugins and/or Landmass mods move them to the *top of your install order* in the Wrye Mash Installers Tab. This is to ensure neither TR nor the official plugins overwrite your mesh/texture fixes in the [Core](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/CORE.md) section
	
## Official Plugins
All due respect to the mod author, who has done taken on an enormous task in fixing and polishing the official plugins--but you are better off without them. If you *must* play with the official plugins, this is the best way to experience them:
1. [Unofficial Morrowind Official Plugins Patched](https://www.nexusmods.com/morrowind/mods/43931?)
	- Download both main files “UMOPP” and “Merged and Compatibility Versions”
	- Install UMOPP first and do not activate any of the ESPs
	- Install Merged and Compatibility Versions as a separate mod and activate the “UMOPP Compatibility Merged” BAIN option
	
## Landmass
1. [Tamriel Data](https://www.nexusmods.com/morrowind/mods/44537?)
	- Download “Tamriel_Data (vanilla)” or "Tamriel_Data (HD)" based on prefence. The latter fits well with Intelligent Textures
1. [Tamriel Rebuilt](https://www.nexusmods.com/morrowind/mods/42145?)
	- Download both “Tamriel Rebuilt” and the optional “TR Music” files; install as separate mods
	- Cleaning: TR_Preview.esp requires cleaning
1. [Skyrim Home of the Nords](https://www.nexusmods.com/morrowind/mods/44921?)
1. [HOTV Solstheim Tomb of the Snow Prince](https://www.nexusmods.com/morrowind/mods/46810)
	- STOTSP incorporates Anthology Solstheim's worldspace edits. Be sure to disable "Anthology Solstheim" in the CORE section
	- Enable the following BAIN options:
		- 00 Core
		- 010 Solstheim - Tomb of the Snow Prince
		- 012 Armor of the Snow Prince
	- Cleaning: Snow Prince Armor Redux.esp, and VSW_Solstheim_TD_Item_Expansion.esp require cleaning
	- NB: STOTSP requires Tamriel_Data.esm, which you installed just above
1. [Rather Nice Factor Estate](https://www.nexusmods.com/morrowind/mods/47933?)

### Landmass Mod Compatibility
Solstheim Tomb of the Snow Prince overhauls the entire landmass of Bloodmoon, so any mods that edit the same landmass create incompatibilities. You will need to make some edits:

1. Run the **Morrowind Code Patch (MCP)** again. Under the **Interface Changes** section, enable the "Map Expansion (for Tamriel Rebuilt)" option. 
	- This will expand the map boundaries so that Solstheim and the Morrowind mainland will not be cut off on your in-game map.
1. **Ownership Overhaul** (installed in the [**Balance**](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/BALANCE.md) section)
	- NOTE: This mod overwrites some changes to Anthology Solstheim / Solstheim Tomb of the Snow Prince (which moves the island of Solstheim farther north). If you are using STOTSP, you will need to delete the exterior Solstheim cell references with TESAME (or get used to floating objects in the middle of the sea)
	- Run TESAME and open the *"Ownership Overhaul.esp"* plugin. TESAME will generate a list of the edits created by the plugin
	- The Cell edits you need to delete in TESAME are:
		1. **Felsaad Coast Region** (This Cell is unnamed; it will be the penultimate unnamed entry if listed alphabetically--you can check by clicking the entry and looking at the information in the bottom tab of the GUI)
		1. **Isinfer Plains Region** (This Cell is unnamed; it will be the last unnamed entry if listed alphabetically--you can check by clicking the entry and looking at the information in the bottom tab of the GUI)
		1. **Fort Frostmoth**
		1. **Fort Frostmoth**
		1. **Raven Rock**
		1. **Skaal Village**
		1. **Skaal Village**
		1. **Thirsk**
	- Delete these *and only* these cells in TESAME. Remember to save the plugin before exiting TESAME
	- I recommend zipping the edited ESP and installing as a new mod to avoid accidentally overwriting it

Remember to drag this Optional Early Loaders section to the top of your Install order.


**NEXT SECTION**:
[**Finish Line**](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md)