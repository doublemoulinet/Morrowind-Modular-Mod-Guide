# Landmass Expansions

The landmass mods--**Tamriel Rebuilt** and its sister projects like **Skyrim: Home of the Nords**--are highly recommended on subsequent playthroughs. These are arguably the most impressive modding projects on the web. Tamriel Rebuilt is a decades-long project to recreate the Morrowind mainland in TES3. The "Old Ebonheart" release is one of the best quest mods available and I recommend a TR-centric playthrough to play the different questlines.

**Solstheim Tomb of the Snow Prince** overhauls the Bloodmoon expansion to bring the world design in line with current Tamriel Rebuilt / Project Tamriel design standards. It is highly recommended. You will see why after you play Bloodmoon in vanilla: the vanilla world design is flat, empty, and boring. STOTSP is a performance-friendly overhaul that makes playing Bloodmoon significantly more fun. I recommend it for all subsequent playthroughs!

	
## Landmass
1. [Tamriel Data](https://www.nexusmods.com/morrowind/mods/44537?)
	- Download “Tamriel_Data (vanilla)” or "Tamriel_Data (HD)" based on prefence. The latter fits well with Intelligent Textures
1. [Tamriel Rebuilt](https://www.nexusmods.com/morrowind/mods/42145?)
	- Download the Main File and Hotfix file. Enable "00 Core" and the hotfix ESP
	- Cleaning: TR_Preview.esp requires cleaning
1. [Skyrim Home of the Nords](https://www.nexusmods.com/morrowind/mods/44921?)
	- **Grass Plugins**: add the grass ESP to your "Grass Plugins" folder if you created one when installing Remiros' Grass
1. [Solstheim - Tomb of the Snow Prince](https://www.nexusmods.com/morrowind/mods/46810)
	- Download both Main Files
	- For "Solstheim Tomb of the Snow Prince" enable the following BAIN options:
		- 00 Core
		- 010 Solstheim - Tomb of the Snow Prince
		- 011 TOTSP Patches (we only want the Patch for Purists patch)
		- 012 Armor of the Snow Prince
	- For "Solstheim Graphical Replacer" enable only the following option:
		- 012 Remiros Groundcover for TOTSP
	- Ensure only the following four plugins are enabled: 
		- *Solstheim Tomb of the Snow Prince.esm*, 
		- *TOTSP TD Content Integration.esp* (only if you are also playing with Tamriel Rebuilt!)
		- *TOTSP_Patch_for-Purists_4.0.2.esp*, 
		- *VSW-Rem-Anthology Solstheim.esp*
	- **Grass Plugins**: create a "Grass Plugins" folder within the mod archive and place the *VSW-Rem-Anthology Solstheim.esp* grass plugin inside
	- **Cleaning**: Snow Prince Armor Redux.esp, and TOTSP TD Content Integration.esp require cleaning
1. [Rather Nice Factor's Estate](https://www.nexusmods.com/morrowind/mods/47933?)
	- Enable both the "00 Core" and "01 Patch - Patch for Purists 4.0.X" options

# Landmass Mod Compatibility
The following steps will ensure compatibility between the new landmass mods and your load order:

## Required Changes
1. Run the **Morrowind Code Patch (MCP)** again. Under the **Interface Changes** section, enable the "Map Expansion (for Tamriel Rebuilt)" option. 
	- This will expand the map boundaries so that Solstheim and the Morrowind mainland will not be cut off on your in-game map.
1. **Morrowind Optimization Project** (installed in the [**Core**](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/CORE.md) section)
	- Disable the "02 Lake Fjalding Anti-Suck" option and ensure the *Lake Fjalding Anti-Suck.esp* plugin is not loaded. This fix is already included in *Solstheim Tomb of the Snow Prince*
1. Lastly, you will need to **register the BSA archives** provided by these landmass mods (TR_Data.bsa and PT_Data.bsa). You can do this via Wrye Mash. Navigate to the right pane of the Mods Tab and select the "BSA Archives" tab. Make sure each BSA has a checkmark next to its name.

## Tamriel Rebuilt Compatibility
Optionally, you may update the following mods to enable compatibility/integration with Tamriel Rebuilt:
1. [Glow in the Dahrk](https://www.nexusmods.com/morrowind/mods/45886?) (installed in the [**Expanded Core**](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/EXPANDEDCORE.md) section)
	- Additionally enable BAIN option "06 - TR Interior Sunrays" if you have not already done so.
1. [Remiros' Groundcover](https://www.nexusmods.com/morrowind/mods/46733?) (installed in the [**Visuals**](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/VISUALS.md) section)
	- **Grass Plugins**: Additionally enable the "01 TR Plugins" and "02 TR Preview Plugins"
	- Note: grass in the landmass mods will decrease performance
1. [Facelift](https://www.nexusmods.com/morrowind/mods/47617?)
	- Download the "kart_fut_TR_PT" Main File and install. Installation order doesn't matter; you may merge, or place the mod underneath, *Facelift* in the **VISUALS** section. Adds high quality textures for TR faces to better fit in with HD texture replacers like IT.
1. [Near Vanilla Road Sign Replacer](https://www.nexusmods.com/morrowind/mods/44957?) (installed in the [**Visuals**](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/VISUALS.md) section)
	- enable the "00 Core" and "02 Vvardenfell, Morrowind, and Cyrodiil" BAIN options. This replaces the generic TR road signs with vanilla-friendly readable signs.

**NEXT SECTION**:
[**Finish Line**](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md)