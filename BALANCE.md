# Gameplay - Balance

## Balance - Core
1. [Beware the Sixth House](https://www.nexusmods.com/morrowind/mods/46036?)
1. [Bloodmoon Rebalance](https://www.nexusmods.com/morrowind/mods/45714?)
1. [Ownership Overhaul](https://www.nexusmods.com/morrowind/mods/48051?)
	- Enable only the ESM plugin. In the right pane (your load order), move the *Ownership Overhaul.esm* below *Patch For Purists.esm*, near the top of your load order
1. [There Can Be Only One](https://www.nexusmods.com/morrowind/mods/47766)
	- Enable only the "There Can Be Only One (Alt Fyr).esp" plugin
1. [Tribunal Rebalance](https://www.nexusmods.com/morrowind/mods/45713?)

## Balance - Extended
1. [Better Balanced Booze](https://www.nexusmods.com/morrowind/mods/45844?)
	- Download and install "Better Balanced Booze" main file
1. [Controlled Consumption](https://github.com/NullCascade/morrowind-mods)
	- Click “Clone or download” the zip of all NullCascade’s Morrowind mods
	- In MO2, set Controlled Consumption as your data directory and install
1. [Dynamic Difficulty](https://github.com/NullCascade/morrowind-mods)
	- Click “Clone or download” the zip of all NullCascade’s Morrowind mods
	- In MO2, set Dynamic Difficulty as your data directory and install
1. [Enchant Capacity Rebalance](https://www.nexusmods.com/morrowind/mods/48742?)
	- Enable the MWSE version (not the plugin version)
1. [Less Aggressive Creatures](https://www.nexusmods.com/morrowind/mods/48292?)
1. [Limited Leaping](https://github.com/NullCascade/morrowind-mods)
	- Click “Clone or download” the zip of all NullCascade’s Morrowind mods
	- In MO2, set Limited Leaping as your data directory and install
1. [Marksman Rebalanced](https://www.nexusmods.com/morrowind/mods/46715?)
1. [Putting Power in Willpower](https://www.nexusmods.com/morrowind/mods/45742?)
1. [Realistic Movement Speeds](https://www.nexusmods.com/morrowind/mods/46248?)
1. [Smart Merchants](https://www.nexusmods.com/morrowind/mods/47787?)
1. [Soulless Creatures](https://www.nexusmods.com/morrowind/mods/49215)
1. [Wading in Water MW](https://www.nexusmods.com/morrowind/mods/48783?)
1. [Wings of Will](https://www.nexusmods.com/morrowind/mods/46626?)

## Balance - Hardcore
1. [Illegal Summoning](https://www.nexusmods.com/morrowind/mods/47105?)
1. [MDMD - More Deadly Morrowind Denizens](https://www.nexusmods.com/morrowind/mods/48745)
	- Enable the *MDMD - More Deadly Morrowind Denizens.esp* and *MDMD - Creatures Add-On.esp*
1. [Morrowind Anti-Cheese](https://www.nexusmods.com/morrowind/mods/49232)
	- Download the "Ownership Overhaul Patches" Main File
	- Enable "04 Morrowind Anti-Cheese" and rename the mod "Morrowind Anti-Cheese"
	- Be sure to [endorse the original mod](https://www.nexusmods.com/morrowind/mods/47305?)
1. [No Disease Labels](https://www.nexusmods.com/morrowind/mods/48295?)
1. [OperatorJack's Deleveler](https://www.nexusmods.com/morrowind/mods/47897?)
1. [Sepulchral Curses](https://www.nexusmods.com/morrowind/mods/48332)
	- Post-installation: this mod adds some messagebox flavour text that sticks out, so we will comment out the lines in the lua script to remove them
	- Open the "main.lua" in a text editor (like Notepad++)
	- Add "--" (without the quotation marks) to the beginning of lines 81, 82, 93, and 96:
		```
		[line 81] 	--tes3.messageBox(revenantTauntList[math.random(1, #revenantTauntList)])
		```
		```
		[line 82]	--tes3.messageBox(environmentalEffectList[math.random(1, #environmentalEffectList)])
		```
		```
		[line 93]	--tes3.messageBox(revenantTauntList[math.random(1, #revenantTauntList)])
		```
		```
		[line 96]	--tes3.messageBox(environmentalEffectList[math.random(1, #environmentalEffectList)])
		```
	- In Notepad++, the line will turn green to indicate it is a comment and not part of the script language. Confirm that these four lines are green
	- Save the file when finished

**NEXT SECTION**:
[**Gameplay - Consistency**](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/CONSISTENCY.md)