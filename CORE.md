# Core
The following are all you need to play the game on modern systems. This section and [Setup](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md) are the only required sections of the guide. The patches section fixes most of the game's bugs, and MOP and Project Atlas dramatically increase performance.

## Patches
1. [Patch for Purists](https://www.nexusmods.com/morrowind/mods/45096?tab=files)
1. [Anthology Solstheim](https://www.nexusmods.com/morrowind/mods/43436?tab=files)
	- Download main file and enable the following options:
		- 00 Core
		- 01 Core - ESM version
		- 02 Patch - Patch for Purists 4.0
		- 11 Addon - Fort Frostmoth Repaired
	- NB: Don't install Anthology Solstheim if using HoTV Solstheim Tomb of the Snow Prince, included in the Optional Content section at the end of this guide (STOTSP already includes the Anthology fix)
1. [Expansion Delay](https://www.nexusmods.com/morrowind/mods/47588?tab=files)
1. [No More Stage Diving](https://www.nexusmods.com/morrowind/mods/47738?tab=files)
1. [Projectile Enchant Capacity](https://www.nexusmods.com/morrowind/mods/46685?tab=files)
	- Download both main files and repackage as BAIN and install as a single mod
	- Enable only one of the ESPs (Vanilla, or, Vanilla + Tamriel Rebuilt)
1. [Skill Increase GMST Fix](https://www.nexusmods.com/morrowind/mods/48029?tab=files)
1. [Quest Skill Reward Fix](https://www.nexusmods.com/morrowind/mods/48269?tab=files)

## MWSE Fixes
1. [Easy Escort](https://github.com/NullCascade/morrowind-mods)
	- Click “Clone or download” the zip of all NullCascade’s Morrowind mods
	- Unzip, select Easy Escort and install
1. [Expeditious Exit](https://github.com/NullCascade/morrowind-mods)
	- Click “Clone or download” the zip of all NullCascade’s Morrowind mods
	- Unzip, select Expeditious Exit and install
1. [Memory Monitor](https://github.com/NullCascade/morrowind-mods)
	- Click “Clone or download” the zip of all NullCascade’s Morrowind mods
	- Unzip, select Memory Monitor and install
1. [Sophisticated Save System](https://github.com/NullCascade/morrowind-mods)
	- Click “Clone or download” the zip of all NullCascade’s Morrowind mods
	- Unzip, select Sophisticated Save System and install

## Mesh Fixes
1. [Mesh Fix](https://www.nexusmods.com/morrowind/mods/42134?tab=files)
1. [UV Fix for Velothi Trap Doors](https://www.nexusmods.com/morrowind/mods/43528?tab=files)
	- Download only the “UV Fix for Velothi Trap Door” file
1. [Correct Meshes](https://www.nexusmods.com/morrowind/mods/39348?tab=files)
1. [Correct UV Rocks](https://www.nexusmods.com/morrowind/mods/46104?tab=files)
1. [Morrowind Optimization Patch](https://www.nexusmods.com/morrowind/mods/45384?tab=files)
	- Activate the following:
		- 00 Core
		- 01 Fixed Vanilla Textures
		- 02 Lake Fjalding Anti-Suck
		- 03 MGE XE Addon
	- NB: “Lake Fjalding Anti Suck” is already included in HOTV Solstheim Tomb of the Snow Prince. Do not enable if using STOTSP
	- NB: You will install the “04 Weapon Sheathing Patch” as a separate mod further down in the installation order
1. [Project Atlas](https://www.nexusmods.com/morrowind/mods/45399?tab=files)
	- Enable only the following:
		- 00 Core
	- NB: you will enable the “10 Glow in the Darhk Patch” options later in the installation as a separate mod

## User Interface – Core
1. [Better Daedric Font](https://www.nexusmods.com/morrowind/mods/44540?tab=files)
	- NB before you download and install this mod: if you uninstall this mod after enabling it you will crash to desktop because the default .fnt files will have been overwritten and then uninstalled by Mash, leaving no .fnt files at all. This mod does not by default provide a backup of the vanilla .fnt files, so you _should_ make a backup of the following:
		- daedric_font.fnt
		- daedric_font_obw.tex
	- Create a "backup" folder in the Fonts folder and  copy-paste these two files there before you install Better Daedric Fonts
	- Download and install normally. This will enable the default "Standard style" Daedric font--identical to the vanilla game but in a higher resolution. Read the readme for instructions on installing the other variants if you prefer those.
1. [Better Dialogue Font](https://www.nexusmods.com/morrowind/mods/36873?tab=files)
	- NB: if you uninstall this mod after enabling it you will CTD because the default .fnt files will have been overwritten and uninstalled by Mash. Remember to restore the backup default .fnt files provided in the mod package (They're in Morrowind\Data Files\Fonts\backup)!
1. [Continue](https://www.nexusmods.com/morrowind/mods/45952?tab=files)
1. [Fixed Journal Next Button](https://www.nexusmods.com/morrowind/mods/48097?tab=files)
1. [New Game Confirmation](https://www.nexusmods.com/morrowind/mods/45952?tab=files)


**NEXT SECTION**:
[**Expanded Vanilla**](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/EXPANDEDVANILLA.md)