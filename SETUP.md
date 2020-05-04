# Setup

## Modding Basics
Install Morrowind to a root directory (ex. C:\Steam\steamapps\common\Morrowind) or (C:\Games\Morrowind). Do not install the game in Program Files.

Some general tips:
	- Do not uninstall mods mid-playthrough. The only mods that can be safely uninstalled mid-game are esp-less replacers and MWSE mods. Any mod with an ESP/ESM should not be removed from your mod order mid-playthrough
	- Always read the mod description on the mod page

After you have installed the game, run the Morrowind Launcher and boot to the main menu. This ensures the proper files are generated.

## Wrye Mash - Polemos Fork
[Wrye Mash - Polemos Fork - 2020](https://www.nexusmods.com/morrowind/mods/45439?tab=files)
1. Download and install the latest x64 manual installation archive or the latest x64 beta manual installation archive
1. Extract the contents to your Morrowind root foler (C:\...\Morrowind). Overwrite/merge if prompted
1. In the Morrowind root folder (C:\...\Morrowind) create a new folder called "Mods" (this is where you will extract and keep all your mod packages)
1. Run mash64.exe
1. The application will prompt you to select the Morrowind root directory. It will also prompt you to select an Installers path: select the C:\...\Morrowind\Mods directory you created earlier
1. You can ignore the mlox optional path for now

Wrye Mash has now been successfully initialized. 

The plugins are listed in the "Mods" tab. They should be listed as follows:
	- Morrowind.esm
	- Tribunal.esm
	- Bloodmoon.esm

To install a mod in Wrye Mash, place the mod package in the "Mods" folder you created in your Morrowind directory. Wrye Mash will detect it and upate its "Installers Tab." 

## Morrowind Code Patch
The Morrowind Code Patch (MCP) is an engine-level fix for the Morrowind.exe. It is an essential utility. The MCP must be installed manually. Do not place this in your Wrye Mash "Mods" directory. 
1. Download the Morrowind Code Patch main file from [Morrowind Code Patch](https://www.nexusmods.com/morrowind/mods/19510?tab=files)
1. Extract to your Morrowind root directory (C:\...\Morrowind). Do not extract it to Morrowind\Data Files.
1. Download the MCP Beta from [MCP Skunk Works](https://www.nexusmods.com/morrowind/mods/26348/?tab=files)
1. Extract the contents to your Morrowind root diectory, and overwrite when prompted
1. Run Morrowind Code Patch.exe and enable the following options:
	- Beta: every option EXCEPT "Doppler audio fix"
	- Game Mechanics: every option EXCEPT "Healthy Appetite" and "Allow Gloves with Bracers"
	- Visuals: every option EXCEPT "Over-the-shoulder third person camera" and "Vanity camera lock"
	- Mod specific: enable EVERY option
	- Interface changes: enable every option EXCEPT "Disable map smoothing" and "Spell select by name" and "see all standard potion effects"
	- International: none
	- Bug Fixes: ensure EVERY option is enabled
1. Click the big "Apply chosen patches" button

## MGE XE
The Morrowind Graphics Extender (MGE XE) is another essential fix. Among its other changes, it also supports and comes packaged with the MWSE 2.1 beta, the lua-based script extender. It works out of the box. Like the Morrowind Code Patch, MGE XE must be installed manually.
1. Download the latest version of [MGE XE](https://www.nexusmods.com/morrowind/mods/41102?tab=files)
1. Extract the contents to your Morrowind root directory (not "Data Files"). If you have unpacked correctly, the MGEXEGui.exe should be adjacent to the Morrowind.exe
1. Right-click the MWSE-Update.exe and select **Run as Administrator**. (You may want to add this executable to your anti-virus whitelilst.) Allow the update process to take place. The command-line window will automatically close when this process is done. 
1. Run MGEXEGui.exe

MGE XE consists of five tabs with configurable options: Graphics, Distant Land, In-Game, Config, and Instructions. There are a number of MGE XE options to enable now:

### Graphics
The features in this section are self-explanatory. Select your display resoultion, set AA and AF (check the Config tab to report the max AA/AF your hardware supports). I recommend borderless windowed mode. Enable Vsync only if not already enabled through your GPU options. 

Shaders requires some setup:
1. Click the checkbox to enable shaders and enter "Shader setup..."
1. Select the High quality preset. Ensure the following shaders are enabled:
	- SSAO Fast
	- Underwater Interior Effects
	- Underwater Effects
	- Sunshafts
	- Bloom Soft
	- Eye Adaptation (HDR)
	
You will need to run MGE XE at the end of your mod installation to regenerate distant land and enable mod-specific shaders.

### Distant Land
Distant Land does what it says. My personal settings ensure a low performance impact and cleave to the original foggy aesthetic. 

The **Distant land generator wizard** lets you select which plugins MGE XE will use when generating distant land. I recommend selecting **Use current load order**. When you click **Continue** a prompt will offer you three options to generate distant land:
- **Automatic setup will** generate distant land for you according to pre-defined settings
- **Customize setup** will let you modify the distant land generation options. I recommend this setting when generating distant land for the first time
- **Update existing distant land** will regenerate distant land according to the last used settings. If you've generated distant land previously, this is the option to use.

For **Customize setup** I recommend the following settings:
- Land Textures: **world texture resolution**: 2048, **world normalmap resolution**: 1024
- Land Meshes: set **world mesh detail** to high
- Statics: set **minimum static size** to 150, **Mesh detail level** to Full, **Distant texture reduction** to 1/2, and tick all the right-hand options EXCEPT "include reflective water in interiors"

After MGE XE has generated distant land, in the "Distant Land" tab in MGE XE, set the **Draw Distance** to 3.0 cells. I recommend between 2-4 cell draw distance to maintain the vanilla atmosphere and keep performance cost to a minimum.

Other Distant Land settings:
- Water:
	- Reflections: ALL except "Blur Reflections"
	- Dynamic ripples: 20 height of waves
	- Caustics: 50%
- XE: enable Dynamic solar shadows
- Auto set other distances: By draw distance
- Fog:
	- Use high quality (exponential) fog: enable
	- High quality atomosphere and distance colouring: enable

You will need to run MGE XE at the end of your mod installation to regenerate distant land and enable mod-specific shaders.

### In-game

Enable the following options:
	- Skip opening movie
	- Crosshair autohide
	- Responsive menu caching
Under Morrowind engine settings, enable the following:
	- Allow yes to all load errors
	- Show subtitles
	- Allow screenshots
	- Thread loading
	- Hit fader

## Additional Tools

### tes3cmd
This powerful command-line tool cleans mods and will be used to build a multipatch at the end of the mod guide.
1. Download [tes3cmd](http://wiki.theassimilationlab.com/mmw/TES3cmd) and extract the tes3cmd.exe your **Morrowind\Data Files** folder. Do not install tes3cmd to the root directory
1. Inside **Morrowind\Data Files** create a .txt file and [copy the batch file cleaning text](http://wiki.theassimilationlab.com/mmw/TES3cmd#Using_a_batch_file_to_clean_plugins)
1. Rename the .txt file to tes3cmd_clean.bat. Make sure to change the filetype extension from .txt to .bat
1. Inside **Morrowind\Data Files** create another .txt file and [copy the batch file multipatch text](http://wiki.theassimilationlab.com/mmw/TES3cmd#Using_a_batch_file_to_create_a_multipatch_plugin)
1. Rename the .txt file to tes3cmd_multipatch.bat. Make sure to change the filetype extension from .txt to .bat

### TES3Merge
This tool will automatically patch mod conflicts by generating a merged patch. This patch will be used in conjunction with tes3cmd's multipatch. 
1. Download [TES3Merge](https://www.nexusmods.com/morrowind/mods/46870?tab=files)
1. Extract the contents to your Morrowind root directory in a new folder called "TES3Merge"

###  TES3View
This experimental tool is an advanced GUI conflict viewer similar to xEdit for later TES/Bethesda games. It has more limited functionality than the latter but still provides excellent functionality
1. Download the [xEdit 4.1.3a experimental build](http://www.mediafire.com/file/g10ay0bqynval8s/TES3View_%2528xEdit_4.1.3a_EXTREMELY_EXPERIMENTAL%2529.zip/file) on MediaFire (courtesy of Sigourn). This download has already renamed the folder and .exe to TES3View in order to enable the tool to work in Morrowind
1. Extract the folder to the Morrowind root directory (...Morrowind\TES3View\TES3View.exe)

Familiarize yourself with TES3View. Like other xEdit iterations, it is a powerful tool to track conflicts in your plugin order. 

### TESTool
TESTool is a mod repair and management tool. You will use it to clean your plugins.
1. [Download TESTool](https://en.uesp.net/wiki/Tes3Mod:TESTool) and extract the executable and files to your root directory (Morrowind\TESTool.exe).

### Mlox
A plugin load order sorter. Highly recommended.
1. Download the latest version of [mlox from github](https://github.com/mlox/mlox/releases/). Review the [github page](https://github.com/mlox/mlox) for more information on its use
1. Extract the mlox.exe to your Morrowind root directory (Morrowind\mlox.exe).
You can add mlox to your list of executables in Wrye Mash by clicking the gear icon at the bottom bar. In the "Wrye Mash Settings" popup navigate to the "Paths" tab and add the Mlox.exe filepath.

### Official Construction Set
The official Bethesda The Elder Scrolls Construction Set, patched and fixed to work with the Steam, GOG, or Bethesda.net version of Morrowind. While not technically needed for this guide, a useful resource if you want to directly edit a plugin or create your own mods.
1. Download the [TES Construction Set](https://www.nexusmods.com/morrowind/mods/42196?tab=files)
1. Unpack the files to the Morrowind root directory (Morrowind\Tes Constructoin Set.exe)

## MWedit
An experimental alternative to the Construction Set. Unlike the CS, you can use MWedit to create merged plugins of certain mods (item/weapon replacers, for example) in order to reduce plugin count. This is optional.
1. Download [MWedit](http://wiki.theassimilationlab.com/mmw/MWEdit)
1. Extract the folder to the Morrowind root directory (Morrowind\MWedit\Mwedit.exe)

## Plugin Cleaning
As you follow the modlist, you will see that I note certain mods "require cleaning." ESPs sometimes contain dirty references and your job is to squash these bugs. You will use two tools for this: TESTool and tes3cmd's batch cleaning file.

### TESTool
The first step is to use TESTool to clean your plugins.
1. Launch Testool
1. A window will prompt you if you want to use your Morrowind root foler instead of registry settings. Click **Yes**
1. Select **Options** and enable: 
	- Don't change plugin filenames
	- Retain file time, when cleaning
	- Restricted dialog cleaning
1. Select **Clean ESP/ESM Files** and click **Execute**
1. Select the relevant plugin that requires cleaning (or, alternately select ALL .esm/.esp files and check the log after for a list of cleaned plugins)

### tes3cmd_clean.bat
Tes3cmd catches errors that TESTool misses, and vice versa.

To use the tes3cmd_clean.bat you need to drag and drop the .esp file onto to .bat and allow tes3cmd processes to run. To expedite this process, I recommend creating a desktop shortcut of the tes3cmd_clean.bat and drag/drop ESP/ESM files this way.

Each time you drop a plugin on the .bat file, a -cleaned.log file will generate. These can safely be deleted after you are done cleaning all your plugins.
	
### Installing cleaned plugins
Once you have cleaned your plugins, create a new folder "[Mod name] - Cleaned ESP" and drop the cleaned plugin into this folder. Repeat for all cleaned plugins.

Drop the new "[Mod name] - Cleaned ESP" folders into your Mods directory. In Wrye Mash drag these new projects below the original mod packages in your Installers tab. You can disable the plugin file in the original mod package by deselecting it in the "Esp/m filter" right pane.

**NEXT SECTION**:
[**Core**](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/CORE.md)