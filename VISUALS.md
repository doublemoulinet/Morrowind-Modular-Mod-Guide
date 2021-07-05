[<< Previous section](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/EXPANDEDCORE.md)
 | [Home](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide) | [Next section >>](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/BALANCE.md)

# Visuals
Improves the visual quality of the game while preserving the original  design.

## Visuals Base
Fixed ground meshes and character heads, and AI-upscaled and hand-polished vanilla textures.
1. [Adjustable Landscape Texture Scale](https://www.nexusmods.com/morrowind/mods/49689)
1. [Facelift](https://www.nexusmods.com/morrowind/mods/47617?)
	- Download the "kart_facelift_meshes" Main File, and "olaf_facelift_argonian" Optional File, selecting Merge when prompted
1. [Intelligent Textures](https://www.nexusmods.com/morrowind/mods/47469?)
	- Enable both "00 Core" and "01 Atlas Textures"

## Grass
Performance-friendly groundcover that dramatically improves the look of the environments.
1. [Remiros' Groundcover](https://www.nexusmods.com/morrowind/mods/46733?)
	- Installation: enable the "00 Core" option
	- *Post-installation*: within the "Remiros' Groundcover" mod archive, create a folder named "Grass Plugins"
		- Place all plugins from *Remiros' Groundcover* in this new folder

>*Note*: Grass plugins will only be enabled during MGE XE's distant land generation, which you will run at the end of the guide in the [**Finish Line**](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md) section.

## Lighting and Weather
Better ambient lighting values, darker nights, dynamic lights and weathers.
1. [Glow in the Dahrk](https://www.nexusmods.com/morrowind/mods/45886?)
	- Follow the install prompts and select these options:
		- Interior Sunrays: Yes
		- Nord Glass Windows: (leave unticked)
		- Raven Rock Glass Windows: Yes
		- Dark Molag Mar: (leave unticked)
		- Optional files: tick only "include Tel Uvirith"
1. [Project Atlas - Glow in the Dahrk Patch](https://www.nexusmods.com/morrowind/mods/45399?)
	- Download the main file install *only* the following BAIN option:
		- 10 Glow in the Dahrk Patch - Interior Sunrays
	- Rename the mod to "Project Atlas - Glow in the Dahrk Patch". Click OK.
1. [Let There Be Darkness](https://www.nexusmods.com/morrowind/mods/47912?)
1. [The Midnight Oil](https://www.nexusmods.com/morrowind/mods/48293?)
1. [Weather Adjuster](https://www.nexusmods.com/morrowind/mods/46816?)
1. [MGG Weather Darker Nights](https://www.nexusmods.com/morrowind/mods/47141?)
1. [Watch the Skies](https://www.nexusmods.com/morrowind/mods/48636)
	- Enable: "00 Lua core" and "02 Weather Adjuster Replacer"

## Environmental VFX
New or enhanced visual effects, including improved flame and particle effects, shaders, and other subtle improvements.
1. [Better Waterfalls](https://www.nexusmods.com/morrowind/mods/45424?)
	- Enable the "00 Core" option
1. [The Dream is the Door](https://www.nexusmods.com/morrowind/mods/47423?)
1. [Enlightened Flames](https://www.nexusmods.com/morrowind/mods/48816?)
	- Enable both the "00 Core" and "01 enlightened flames" options
1. [Heat Haze](https://www.nexusmods.com/morrowind/mods/48973)
1. [Keg Drip](https://www.nexusmods.com/morrowind/mods/47903?)
	- Enable the "00 Core" and "01 MWSE" options
1. [Mistify](https://www.nexusmods.com/morrowind/mods/48112?)
	- Enable both the "00 Core" and "01 Vanilla Mist Replacer" options
	- *Note*: may cause FPS drop at night in the Bitter Coast region depending on your CPU. Disable the ESP if the performance decrease annoys you (but keep the mod active for the fixed mist meshes)
1. [Perfectly Proficient Parasol Particles Performance Patch](https://www.nexusmods.com/morrowind/mods/48923)
	- Enable  "00 Project Atlas" only
1. [Shattered Stones - An Earthquake Mod](https://www.nexusmods.com/morrowind/mods/45105?)
1. [Subtle Smoke](https://www.nexusmods.com/morrowind/mods/47341?)
1. [Unto Dust](https://www.nexusmods.com/morrowind/mods/48435?)
	- Enable both "00 Core" and "01 Default Dust"
1. [Visually Filled Soul Gems](https://github.com/NullCascade/morrowind-mods)
	- In the MO2 installation interface, set "Visually Filled Soul Gems" as the data directory
	- Name the mod "Visually Filled Soul Gems" and install
1. [Visually Trapped Objects](https://www.nexusmods.com/morrowind/mods/48936)
1. [Waterfall Tweaks](https://www.nexusmods.com/morrowind/mods/46271?)

## Character Visuals
Better blood, new damage effects, visible equipment on character models, and more.
1. [Assetless No Glow](https://github.com/NullCascade/morrowind-mods)
	- In the MO2 installation interface, set "No Glow" as the data directory
	- Name the mod "Assetless No Glow" and install
1. [Elemental Effects](https://www.nexusmods.com/morrowind/mods/49799)
1. [Hopesfire Glow](https://www.nexusmods.com/morrowind/mods/45855?)
	- Enable only the "Hopesfire Torch (+brighter trueflame).esp
1. [MWSE Blood Diversity](https://www.nexusmods.com/morrowind/mods/47913)
	- Install both the "00 Core" option and the texture version of your choice ("01 vanilla-friendly textures" for vanilla textures; "02 R-zero's textures" for better-looking, bloodier blood)
	- *Post-installation*: Open your MO2 profile's .ini in ```Mod Organizer 2\Profiles\[profile name]\Morrowind.ini```
		- Replace the "[Blood]" section with the following:
			<details>
			<summary>Morrowind.ini [Blood]</summary>
			
					[Blood]
					;Model 0=BloodSplat.nif
					;Model 1=BloodSplat2.nif
					;Model 2=BloodSplat3.nif

					;Texture 0=Tx_Blood.tga
					;Texture 1=Tx_Blood_White.tga
					;Texture 2=Tx_Blood_Gold.tga

					;Texture Name 0=Default (Red)
					;Texture Name 1=Skeleton (White)
					;Texture Name 2=Metal Sparks (Gold)
					
					Model 0=BloodSplat.nif
					Model 1=BloodSplat2.nif
					Model 2=BloodSplat3.nif

					Texture 0=Anu\Blood\Tx_Blood.dds
					Texture 1=Anu\Blood\Tx_Blood_Dust.dds
					Texture 2=Anu\Blood\Tx_Blood_Sparks.dds
					Texture 3=Anu\Blood\Tx_Blood_Ichor.dds
					Texture 4=Anu\Blood\Tx_Blood_Ecto.dds
					Texture 5=Anu\Blood\Tx_Blood_Blue.dds
					Texture 6=Anu\Blood\Tx_Blood_Insect.dds
					Texture 7=Anu\Blood\Tx_Blood_Energy.dds

					Texture Name 0=Red Blood
					Texture Name 1=Dust
					Texture Name 2=Metal Sparks
					Texture Name 3=Ichor
					Texture Name 4=Ectoplasm
					Texture Name 5=Blue Blood
					Texture Name 6=Orange Blood
					Texture Name 7=Energy
			</details>
1. [Pincushion](https://www.nexusmods.com/morrowind/mods/46862?)
1. [Vanity](https://www.nexusmods.com/morrowind/mods/48529?)
1. [Weapon Sheathing](https://www.nexusmods.com/morrowind/mods/46069?)
	- Download and install the “MWSE” Main File
	- In the MO2 installer interface, right-click "Data Files" and click `set as data files directory`
1. [MOP - Weapon Sheathing Patch](https://www.nexusmods.com/morrowind/mods/45384?)
	- Install *only* the “04 Weapon Sheathing Patch” BAIN option
	- Rename the mod to "MOP - Weapon Sheathing Patch". Click OK.
	
## Meshes and Textures
Additional fixes to vanilla meshes and textures.
1. [Ashmire Replacer](https://www.nexusmods.com/morrowind/mods/48291?)
	- Download "Ashmire Replacer" and enable ONLY the "01 - Still Mire" BAIN option
1. [Bitter Coast Scum Replacer](https://www.nexusmods.com/morrowind/mods/48291?)
	- Download "Bitter Coast Scum Replacer" and enable the "00 Core" and "03 Standalone - Lougian's Meshes Fixed" options
1. [Dunmer Lanterns Replacer](https://www.nexusmods.com/morrowind/mods/43219?)
	- Enable both "00 Core" and "03 Glow Effect" options
1. [Enhanced Stone Walls](https://www.nexusmods.com/morrowind/mods/45939?)
	- Download the “Enhanced Stone Walls” file
1. [I Lava a Good Mesh Replacer](https://www.nexusmods.com/morrowind/mods/49605)
	- Enable the "00 Core" option
1. [Improved Nordic Iron Helm](https://www.nexusmods.com/morrowind/mods/43816?)
	- Download and install the Optional File "Improved Nordic Iron Helm 1.0-alternate"
1. [Improved Thrown Weapon Projectiles](https://www.nexusmods.com/morrowind/mods/44763?)
	- Download and install only the main file
1. [Lore Friendly Iron Warhammer](https://www.nexusmods.com/morrowind/mods/45939?)
	- Download only "Lore Friendly Iron Warhammer" and install
1. [Near Vanilla Road Sign Replacer](https://www.nexusmods.com/morrowind/mods/44957?)
	- Enable "00 Core" and "01 Vvardenfell only"
	- Optional: install [No Translation Tooltips](https://www.nexusmods.com/morrowind/mods/48540?) to remove now-redundant road sign tooltips
1. [Vivec Palace Water Replacer](https://www.nexusmods.com/morrowind/mods/48291?)
	- Download "Vivec Palace Water Replacer" and enable the "00 Core" and "01 Original Color" options

## Splash Screen / Video 
Vanilla splash screens reformatted for 16:9 screens.
1. [Widescreen Menu and Logo Replacer](https://www.nexusmods.com/morrowind/mods/47164?)
1. [Widescreen Splash Replacer](https://www.nexusmods.com/morrowind/mods/47163?)
1. [Additional Splash Screens](https://www.nexusmods.com/morrowind/mods/43319?)
1. [Widescreen Splash Additions](https://www.nexusmods.com/morrowind/mods/48001?)
	- Archive is incorrectly packed: in MO2's "manual" install interface, create a "splash" folder and place the .tga files inside


**NEXT SECTION**:
[**Gameplay - Balance**](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/BALANCE.md)

[<< Previous section](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/EXPANDEDCORE.md)
 | [Home](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide) | [Next section >>](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/BALANCE.md)
