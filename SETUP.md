# Setup

## Index
1.[Modding Basics](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#modding-basics)
1. [Wrye Mash](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#wrye-mash)
	1. [Mods Tab](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#mods-tab)
	1. [Installers Tab](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#installers-tab)
	1. [Additional Functions](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#additional-functions)
1. [Morrowind Code Patch](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#morrowind-code-patch)
1. [MGE XE](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#MGE-XE)
	1. [Graphics Tab](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#graphics-tab)
	1. [Distant Land Tab](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#distant-land-tab)
	1. [In-game Tab](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#in-game-tab)
1. [Additional Tools](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#additional-tools)
1. [Optional Tools](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#optional-tools)
1. [Plugin Cleaning](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#plugin-cleaning)

## Modding Basics
Install Morrowind to a root directory (ex. C:\Steam\steamapps\common\Morrowind) or (C:\Games\Morrowind). Do not install the game in Program Files.

Some general tips:
- Do not uninstall mods mid-playthrough. The only mods that can be safely uninstalled mid-game are esp-less texture/mesh replacers and *some* MWSE mods. Any mod with an ESP/ESM should not be removed from your mod order mid-playthrough (unless you know what you're doing)
- Always read the mod description on the mod page
- Remember to update MWSE! It's under active development and you should run the MWSE-Updater.exe frequently
- Likewise, check the Nexus for mod updates. MWSE mods are frequently updated and most can be safely installed and updated mid-playthrough

After you have installed the game, run the Morrowind Launcher and boot to the main menu. This ensures the proper files are generated.

## Wrye Mash
1. Download and install the [latest x64 manual installation archive, under Main Files](https://www.nexusmods.com/morrowind/mods/45439?tab=files)
1. Extract the contents to your Morrowind root foler (C:\...\Morrowind). Overwrite/merge if prompted
1. In the Morrowind root folder (C:\...\Morrowind) create a new folder called "Mods" (this is where you will extract and keep all your mod packages)
1. Run mash64.exe
1. The application will prompt you to select the Morrowind root directory. It will also prompt you to select an Installers path: select the C:\...\Morrowind\Mods directory you created earlier
1. You can ignore the mlox optional path for now

Wrye Mash has now been successfully initialized. 

### Mods Tab
Plugins in the Morrowind\Data Files are listed in the "Mods" tab. The plugins need to be arranged in this order:
- Morrowind.esm
- Tribunal.esm
- Bloodmoon.esm

### Installers Tab
To install a mod in Wrye Mash, place the mod package in the "Mods" folder you created in your Morrowind directory. Wrye Mash will detect it and upate its "Installers Tab." You can rearrange the order of your mod packages in the Installers Tab left pane. Finally, right click the package and select "install." Mash will display a plus icon to indicate that a mod has been successfully installed. 

Familiarize yourself with the colour coding scheme! If you are unfamiliar with Mash, you can access the readme by clicking the question mark at the bottom of the Mash interface. Read sections 5 (Installers Tab), 6 (Mods Tabs), and 7 (Saves Tab) at a minimum.

Pro tip: use markers to create helpful visual separators in your installers tab. In the menu bar: Actions->Add marker. Enter a name (Ex., "CORE" or "Patches" as per the headings and subheadings of this guide) and click OK. Drag and drop in the install order.

### Additional Functions
Wrye Mash has a few additional functions you should be aware of: cleaning saves and updating a plugin masters list:
1. **Cleaning saves**: any time you change your load order (removing or updating a plugin) go to the "Saves" tab in WM. Select your save and click the right pane (which lists the plugins associated with the save). Mash will prompt you to edit/update the masters list. Click yes. Then click save at the bottom of the right pane.
1. **Updating masters lists**: go to the "Mods" tab for your list of plugins. If a plugin's checkbox colour is yellow the associated master file size does not match the plugin's. Select the plugin and click the right pane (which lists the masters associated with the plugin). Mash will prompt you to edit/update the masters list. Click yes. Then click save at the bottom of the right pane.

## Morrowind Code Patch
The Morrowind Code Patch (MCP) is an engine-level fix for the Morrowind.exe. It is an essential utility. The MCP must be installed manually. Do not place this in your Wrye Mash "Mods" directory. 
1. Download the Morrowind Code Patch main file from [Morrowind Code Patch](https://www.nexusmods.com/morrowind/mods/19510?tab=files)
1. Extract to your Morrowind root directory (C:\...\Morrowind). Do not extract it to Morrowind\Data Files.
1. Download the MCP Beta from [MCP Skunk Works](https://www.nexusmods.com/morrowind/mods/26348/?tab=files)
1. Extract the contents to your Morrowind root diectory, and overwrite when prompted
1. Run Morrowind Code Patch.exe and enable the following options:
	- **Beta**: every option EXCEPT *"Doppler audio fix"*
	- **Game Mechanics**: every option EXCEPT *"Healthy Appetite"* and *"Allow Gloves with Bracers"*
	- **Visuals**: every option EXCEPT *"Over-the-shoulder third person camera,"* and *"Vanity camera lock"*
	- **Interface changes**: enable every option EXCEPT *"Map Expansion (for TR),"* *"Disable map smoothing,"* *"Spell select by name,"* and *"see all standard potion effects"*
	- **International**: none (if using the English language Morrowind)
	- **Bug Fixes**: ensure EVERY option is enabled
1. Click the big "Apply chosen patches" button

## MGE XE
The Morrowind Graphics Extender (MGE XE) is another essential fix. Among its other changes, it also supports and comes packaged with the MWSE 2.1 beta, the lua-based script extender. It works out of the box. Like the Morrowind Code Patch, MGE XE must be installed manually.
1. Download the latest version of [MGE XE](https://www.nexusmods.com/morrowind/mods/41102?tab=files)
1. Extract the contents to your Morrowind root directory (not "Data Files"). If you have unpacked correctly, the MGEXEGui.exe should be in the same folder as the Morrowind.exe
1. Right-click the MWSE-Update.exe and select **Run as Administrator**. (You may want to add this executable to your anti-virus whitelilst.) Allow the update process to take place. The command-line window will automatically close when this process is done. 

Next, download the following MGE XE shaders. You can install these manually or using Wrye Mash's Installers Tab. If installing manually, extract them to your Morrowind *Data Files* folder:
1. [MGE XE Land Bias Fix](https://mega.nz/file/ft5hUJ5L#-5Y533Rtwy2uX5moycm4pQjEDXClyFGl78XMDvfVzME) small tweak to the distant land height bias to reduce clipping/seams
1. [MGE XE Shader - deband_fogaware](https://mega.nz/file/W8x3RTCK#w94LPJSeym5h82KUOg8SbkIoS8M7E-9Xm2Lar0gjqXw) an improved fog shader
1. [MGE XE Shader - EdgeAA](https://mega.nz/file/HwxVXbQY#eSxnVWTbC165OC1EyC-P9IahvH05We88pyba-fy2ePI) improved anti-aliasing, to be used with MGE XE's AA settings

MGE XE consists of five tabs with configurable options: Graphics, Distant Land, In-Game, Config, and Instructions. There are a number of MGE XE options to enable now:

### Graphics Tab
The features in this section are mostly self-explanatory. Select your display resoultion, set AA and AF (check the Config tab to report the max AA/AF your hardware supports). Enable borderless fullscreen windowed mode. Enable Vsync only if not already enabled through your GPU hardware options (if using an Nvidia card, this is enabled through the Nvidia Control Panel). 

Shaders requires some setup:
1. Click the checkbox to enable shaders and enter "Shader setup..."
1. Select the High quality preset. Ensure the following shaders are enabled:
	- EdgeAA
	- SSAO Fast
	- Underwater Interior Effects
	- Underwater Effects
	- Sunshafts
	- Bloom Soft
	- Eye Adaptation (HDR)
	- deband_fogaware
	
You will need to run MGE XE at the end of your mod installation to regenerate distant land and enable mod-specific shaders.

### Distant Land Tab
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
- **Water**:
	- Reflections: ALL except "Blur Reflections"
	- Dynamic ripples: 12 height of waves
	- Caustics: 50%
- **XE**: enable Dynamic solar shadows
- **Auto set other distances**: By draw distance
- **Fog**:
	- Use high quality (exponential) fog: enable
	- High quality atomosphere and distance colouring: enable

You will need to run MGE XE at the end of your mod installation to regenerate distant land and enable mod-specific shaders.

### In-game Tab
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
These modding tools will be used for several key steps in this guide: mod cleaning, merged patch creation, and plugin editing/fixing. These are required.

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
This experimental tool is an advanced GUI conflict viewer similar to xEdit for later TES/Bethesda games. It has more limited functionality than the latter but still provides excellent GUI for plugin conflicts.
1. Download the [xEdit 4.1.3a experimental build](http://www.mediafire.com/file/g10ay0bqynval8s/TES3View_%2528xEdit_4.1.3a_EXTREMELY_EXPERIMENTAL%2529.zip/file) on MediaFire (courtesy of Sigourn). This download has already renamed the folder and .exe to TES3View in order to enable the tool to work in Morrowind
1. Extract the folder to the Morrowind root directory (...Morrowind\TES3View\TES3View.exe)

Familiarize yourself with TES3View. Like other xEdit iterations, it is a powerful tool to track conflicts in your plugin order. 

### TESTool
TESTool is a mod repair and management tool. You will use it to clean your plugins.
1. [Download TESTool](https://en.uesp.net/wiki/Tes3Mod:TESTool) and extract the executable and files to your root directory (Morrowind\TESTool.exe).

### TESAME
TESAME is a useful mod editing program that we will use exclusively to delete bad references within a plugin.
1. [Download TESAME](http://mw.modhistory.com/download-95-5289) and extract the contents to your Morrowind root folder in a new folder called "TESAME"

## Optional Tools
Tools that are not used in this guide, or are part of optional steps. While not strictly needed, if you plan to experiment with your installation and try mods not included in the guide, you will probably need these tools.

### Mlox
Optional. A plugin load order sorter. Mlox will not be used in this guide (plugin order will be adjusted manually in the [Finish Line](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md) section of the guide. If you add your own mods, you may want to check your load order with Mlox.
1. Download the latest version of [mlox from github](https://github.com/mlox/mlox/releases/). Review the [github page](https://github.com/mlox/mlox) for more information on its use
1. Extract the mlox.exe to your Morrowind root directory (Morrowind\mlox.exe).
You can add mlox to your list of executables in Wrye Mash by clicking the gear icon at the bottom bar. In the "Wrye Mash Settings" popup navigate to the "Paths" tab and add the Mlox.exe filepath.

### Official Construction Set
The official Bethesda The Elder Scrolls Construction Set, patched and fixed to work with the Steam, GOG, or Bethesda.net version of Morrowind. While not technically needed for this guide, a useful resource if you want to directly edit a plugin and necessary to create your own mods.
1. Download the [TES Construction Set](https://www.nexusmods.com/morrowind/mods/42196?tab=files)
1. Unpack the files to the Morrowind root directory (Morrowind\Tes Constructoin Set.exe)

### MWedit
An experimental alternative to the Construction Set. You can easily use MWedit to create merged plugins of certain mods (item/weapon replacers, for example) in order to reduce plugin count. This is optional.
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

### tes3cmd cleaning
Tes3cmd catches errors that TESTool misses, and vice versa. 

**Easy method**: Tes3cmd can be accessed through Wrye Mash's **Mods Tabs** by right-clicking the plugin and selecting: *clean with tes3cmd*. It's as easy as that. Move on to the next step: **Installing cleaned plugins**

**Manual method**: If for some reason Wrye Mash's integrated tes3cmd isn't working, or you are a masochist, you can use the tes3cmd_clean.bat you created earlier. To use the tes3cmd_clean.bat you need to drag and drop the .esp file onto the .bat and allow tes3cmd processes to run. To expedite this process, I recommend creating a desktop shortcut of the tes3cmd_clean.bat and drag/drop ESP/ESM files this way.

Each time you drop a plugin on the .bat file, a -cleaned.log file will generate. These can safely be deleted after you are done cleaning all your plugins.
	
### Installing cleaned plugins
Once you have cleaned your plugin, create a new folder "[Mod name] - Cleaned ESP" and drop the cleaned plugin into this folder. Repeat for all cleaned plugins. This is so that you don't overwrite the cleaned plugin with the dirty one if you accidentally reinstall the mod.

Drop the new "[Mod name] - Cleaned ESP" folders into your Mods directory. In Wrye Mash drag these new projects below the original mod packages in your Installers tab. You can then disable the plugin file in the original mod package by deselecting it in the "Esp/m filter" right pane, and then **refreshing** or **annealling** your Installers Tab to ensure these changes are registered.

**NEXT SECTION**:
[**Core**](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/CORE.md)