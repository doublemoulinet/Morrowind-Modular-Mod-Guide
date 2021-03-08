# Setup

## Index
1. [Installation](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#installation)
1. [Morrowind Code Patch](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#morrowind-code-patch)
1. [Tools](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#tools)
1. [Optional Tools](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#optional-tools)
1. [Mod Organizer 2](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#mod-organizer-2)
	- [Configuration](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#configuration)
	- [Tools Setup](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#tools-setup)
	- [Mod Installation](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#mod-installation)
	- [Creating Separators](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#creating-separators)
1. [MGE XE](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#MGE-XE)
	- [Graphics Tab](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#graphics-tab)
	- [Distant Land Tab](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#distant-land-tab)
	- [In-game Tab](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#in-game-tab)
1. [Plugin Cleaning](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#plugin-cleaning)
1. [Wrye Mash Tools](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#wrye-mash-tools)
	- [Cleaning Saves](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#cleaning-saves)
	- [Updating Masters Lists](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#updating-masters-lists)
	- [Registering BSAs](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#registering-bsas)

# Installation
This guide assumes you will be using an English-language edition of Morrowind GOTY (either the GOG or Steam editions). This includes the base game and two main expansions, Tribunal and Bloodmoon.

Install Morrowind and all modding tools to a root directory, outside the default Windows folders. For example: 
- **For your Morrowind installation**: ```C:\Steam\steamapps\common\Morrowind``` or ```C:\Games\Morrowind```
- **For your Morrowind tools**: ```C:\Steam\steamapps\common\Morrowind Mods``` or ```C:\Games\Morrowind Mods```

Do not install the game in Program Files, Program Files (x86), or any other default Windows folder (ex. Desktop, Documents).

## GOG Installation Cleanup
*Note: this step applies only to users of the GOG edition of Morrowind GOTY.*

The GOG edition of Morrowind GOTY bundles several unnecessary files. In addition to uncompressing the BSA archives (which contain all the game's meshes and textures), the GOG edition includes all of Bethesda's Official Plugins. These suck and you don't want to play with them. This guide assumes you will *not* be using the official plugins; play with them at your own peril!

Delete the following files from your ```Morrowind\Data Files``` folder:
- BookArt, Icons, Meshes, Textures folders
- All .esp files 
- All .txt files

After this step, you should have only:
- Folders: Fonts, Music, Sound, Splash, Video
- BSAs: Bloodmoon.bsa, Morrowind.bsa, Tribunal.bsa
- ESMs: Bloodmoon.esm, Morrowind.esm, Tribunal.esm

## General Tips
- Do not uninstall mods mid-playthrough. The only mods that can be safely uninstalled mid-game are esp-less texture/mesh replacers and *some* MWSE mods. Any mod with an ESP/ESM should not be removed from your mod order mid-playthrough (unless you know what you're doing)
- Always read the mod description on the mod page
- Remember to update MWSE! It's under active development and you should run the MWSE-Updater.exe frequently
- Likewise, check the Nexus for mod updates. MWSE mods are frequently updated and most can be safely installed and updated mid-playthrough

After you have installed the game, run the Morrowind Launcher and boot to the main menu. This ensures the proper files are generated.

# Morrowind Code Patch
The Morrowind Code Patch (MCP) is an engine-level fix for the Morrowind.exe. It is an essential utility. The MCP must be installed manually.
1. Download the Morrowind Code Patch main file from [Morrowind Code Patch](https://www.nexusmods.com/morrowind/mods/19510?)
1. Extract to your Morrowind root directory (```C:\...\Morrowind```). Do not extract it to ```Morrowind\Data Files```.
1. Download the MCP Beta from [MCP Skunk Works](https://www.nexusmods.com/morrowind/mods/26348/?tab=files)
1. Extract the contents of the MCP Beta to your Morrowind root directory (```C:\...\Morrowind```), and overwrite when prompted
1. Run Morrowind Code Patch.exe and enable the following options:
	- **Beta**: every option EXCEPT *"Doppler audio fix"*
	- **Game Mechanics**: every option EXCEPT *"Allow Gloves with Bracers"*
	- **Visuals**: every option EXCEPT *"Over-the-shoulder third person camera,"* and *"Vanity camera lock"*
	- **Mod specific**: ensure EVERY option is enabled
	- **Interface changes**: enable every option EXCEPT *"Map Expansion (for TR),"* *"Disable map smoothing,"* *"Spell select by name,"* and *"see all standard potion effects"*
	- **International**: none (if using the English language Morrowind)
	- **Bug Fixes**: ensure EVERY option is enabled
1. Click the big "Apply chosen patches" button

# Tools
These modding tools will be used for several key steps in this guide: mod cleaning, merged patch creation, and plugin editing/fixing. These are required.

### [tes3cmd](https://github.com/john-moonsugar/tes3cmd/releases)
This powerful command-line tool cleans mods and will be used to build a multipatch at the end of the mod guide.
1. Download the latest [tes3cmd](https://github.com/john-moonsugar/tes3cmd/releases) release and extract the tes3cmd.exe to your ```Morrowind\Data Files``` folder. Do not install tes3cmd to the root directory
1. Download the [tes3cmd multipatch](https://mega.nz/file/D1pmHQBJ#9YMB2pyRLAFHqBczqQhqXvzNtaDW7yqwIH4Mt9MuEpA) and extract the tes3cmd_multipatch.bat to your ```Morrowind\Data Files``` folder. Do not install  to the root directory

### [TES3Merge](https://www.nexusmods.com/morrowind/mods/46870?tab=files)
This tool will automatically patch mod conflicts by generating a merged patch. This patch will be used in conjunction with tes3cmd's multipatch. 
1. Extract the contents to ```...\Morrowind Mods\Tools\TES3Merge```

###  [TES3View](http://www.mediafire.com/file/g10ay0bqynval8s/TES3View_%2528xEdit_4.1.3a_EXTREMELY_EXPERIMENTAL%2529.zip/file)
This experimental tool is an advanced GUI conflict viewer similar to xEdit for later TES/Bethesda games. It has more limited functionality than the latter but still provides excellent GUI for plugin conflicts. 

Download the xEdit 4.1.3a experimental build on MediaFire (courtesy of Sigourn). This download has already renamed the folder and .exe to TES3View in order to enable the tool to work in Morrowind
1. Extract the folder to ```...\Morrowind Mods\Tools\TES3View```

### [TESTool](https://www.nexusmods.com/morrowind/mods/47473)
TESTool is a mod repair and management tool. You will use it to clean your plugins.
1. Download manually and extract the contents to ```...\Morrowind Mods\Tools\TESTool```

### [Wrye Mash](https://www.nexusmods.com/morrowind/mods/45439?)
This powerful tool will be used primarily to clean and repair plugins, clean and repair game saves, enable mod-added BSA archives, and update plugin masters.
1. Download the latest x64 manual installation archive, under Main Files, and any x64 manual installation Update file (if applicable)
1. Extract the contents to your Morrowind root folder (```C:\...\Morrowind```). Overwrite/merge if prompted
1. Run mash64.exe
	- The application will prompt you to select the Morrowind root directory. It will also prompt you to select an Installers path: select the ```C:\...\Morrowind\Mods``` directory you created earlier
	- **Morrowind directory**: select your Morrowind root folder (```C:\...\Morrowind```)
	- **Mods Installers directory**: you can direct the filepath to (```C:\...\Morrowind\Mopy\Mods```) or anywhere else; this guide will not use Wrye Mash's Mods Installers functionality
	- **Mlox directory**: You can ignore the mlox optional path for now
1. When prompted to enable support for 1024 plugins, choose Yes
1. Continue through the prompts and conclude the initialization process when prompted

Important: you *must* enable support for 1024 plugins. Currently, with this option disabled the save-cleaning tools are not working

# Optional Tools
Tools that are not used in this guide. While not strictly needed, if you plan to experiment with your installation and try mods not included in the guide, you may find need of these tools. Otherwise, you may skip this section!

### [TESAME](http://mw.modhistory.com/download-95-5289)
TESAME is a useful mod editing program that can delete bad and unwanted references within a plugin.
1. Extract the folder to ```...\Morrowind Mods\Tools\TESAME```

### [Mlox](https://github.com/mlox/mlox/releases/)
Optional. A plugin load order sorter. Mlox will not be used in this guide (plugin order will be adjusted manually in the [Finish Line](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md) section of the guide. If you add your own mods, you may want to check your load order with Mlox.
1. Extract the mlox.exe to your Morrowind root directory (```...\Morrowind\mlox.exe```).

### [Official Construction Set](https://www.nexusmods.com/morrowind/mods/42196?tab=files)
The official Bethesda The Elder Scrolls Construction Set, patched and fixed to work with the Steam and GOG version of Morrowind. While not technically needed for this guide, a useful resource if you want to directly edit a plugin and necessary to create your own mods and merges.
1. Unpack the files to the Morrowind root directory (```...\Morrowind\Tes Construction Set.exe```)

# Mod Organizer 2
As described earlier, this powerful tool will manage your mod installation, mod downloads, and modding tools. Here, you will download and configure the mod organizer as a portable instance to manage your Morrowind installation.

### [Mod Organizer 2](https://www.nexusmods.com/skyrimspecialedition/mods/6194)
1. Download the Main File: **Mod Organizer 2 (Archive)**
1. Extract to ```...\Morrowind Mods\Tools\MO2```
1. Run ModOrganizer.exe
	- You will be prompted to **Choose Instance**. Select **Portable**
	- You will be prompted to **select the game to manage**. Select **Morrowind**.
1. Mod Organizer 2 will launch, and prompt you to follow a brief tutorial. You can skip this if you are familiar with the interface
1. You will be prompted to associate MO2 with nxm links. Select **Yes**

## Configuration
Installed mods are listed on the left pane; this is your **installation order**. Morrowind loads assets in descending order, meaning mods closer to the bottom of the list will overwrite those at the top in the event of a conflict. On the left pane, ensure the list is as follows:
1. DLC: Tribunal
1. DLC: Bloodmoon

Plugins are listed on the right pane; this is your **load order**. Morrowind loads plugins in descending order, meaning plugins closer to the bottom of the list will overwrite those at the top in the event of a conflict. On the right pane, ensure the list is as follows:
1. Morrowind.esm
1. Tribunal.esm
1. Bloodmoon.esm

Now that MO2 has been successfully installed, follow these steps to configure your MO2 profile:

- Click on the ID card icon along the top menubar to open the **Profiles** menu
- Tick **Use profile-specific Save Game files** and **Use profile-specific INI files**. Ensure that Automatic Archive Invalidation is **NOT** enabled
- Select the **Default** profile, and select **Rename**. In the text box, rename this profile to **Vanilla** and click OK
- With the **Vanilla** profile highlighted, select **Copy** and when prompted, title this new profile **Modular** or whichever profile name you like. Click **OK** and close the profile window.

On the **Profile** drop-down menu below the top menubar, be sure to select **Modular** or whatever you've named your modded installation profile. This is the profile you will be modding, and ensures you can easily revert to the Vanilla profile to deactivate all your mods.

## Tools Setup
Tools require additional setup to work with Mod Organizer's virtual file system. After this initial setup, the executables must be run from within Mod Organizer 2 in order to hook into MO2's VFS.

Follow and repeat these steps for **TES3Merge**, **TES3View**, **TESTool**, and **TESAME**:
1. Open the **Executables** menu (the gear icon)
1. In the **Modify Executables** menu, click **Add an executable** (blue plus icon) and choose **Add from file...**
1. Navigate to the location of the relevant tool (see the [Tools](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#tools) section just above) and select its executable file (.exe)
1. In the **Start In** field, search for and choose the location of your Morrowind root folder (ex., ```C:\Games\Morrowind```)
1. Click **Apply** and then **OK**

Follow these steps for **Tes3cmd**:
1. Open the **Executables** menu (the gear icon)
1. In the **Modify Executables** menu, click **Add an executable** (the blue plus iccon) and choose **Add from file...**
1. Navigate to the location of your command line executable (ex., C:\Windows\System32\cmd.exe) and choose it
1. In **Start In**, search for and choose the location of your Morrowind **Data Files** folder (ex., ```C:\Morrowind\Data Files```)

Follow these steps for **Wrye Mash**:
1. Open the **Executables** menu (the gear icon)
1. In the **Modify Executables** menu, click **Add an executable** (the blue plus iccon) and choose **Add from file...**
1. Navigate to the location of your mash64.exe (ex., ```C:\Games\Morrowind\Mopy\mash64.exe```) and choose it
1. Click **Apply** and then **OK**

## Mod Installation
MO2 will not only organize our installation and plugin order but will also handle downloading and installing mods as well.

In the initial setup for MO2 you should have clicked "yes" when prompted to associate MO2 with NXM (nexusmods) download links. If not, or for whatever reason this setting is reverted, navigate to **Settings** (the wrench and screwdriver icon) and click the **Nexus** tab. Click the **Associate with "download with mangager" links**.

Mods can be downloaded and installed one of two ways:
- **Mod Manager Download**: the preferred option when downloading mods from Nexusmods; click the button of the same name when downloading from the website.
	- On the right pane of MO2, select the **downloads** pane
	- Double click on your downloaded archive
	- The "quick install" popup will prompt you to enter the mod name (you can use your scrollwheel to choose from the autogenerated file names)
	- Click **OK**
- **Manual Download**: for mods not from the nexus, or which do not offer a manager download link. 
	- Click on the **Install Mod** menubar icon (to the left of the **Visit Nexus** globe icon)
	- Select the downloaded mod archive you want to install
	- MO2 will prompt you to enter a name for the mod (you can use your scrollwheel to choose from the autogenerated file names)
	- Click **OK**

Sometimes, mods are incorrectly packaged, and "quick install" will not work. Where indicated in the guide, you will be required to manually set the data files directory within MO2's installation popup.

## Creating Separators
Separators are a convenient visual tool to organize your installation order in the left pane. It is strongly recommended that you create separators for each module of the guide, as well as for the subsections in each.

We will create our first separator for the upcoming **MGE XE** section:
- Click the mini-wrench-and-screwdriver icon to the right of the **Profile** dropdown menu
- In the dropdown menu, click **Create separator**
- Name it **MGE XE** and click OK

MO2 will automatically place your new separator at the very bottom of your load order. You can then drag and drop this separator in the left pane as you see fit. In this case, ensure that the separator comes after the two expansions, like so:
1. DLC: Tribunal
1. DLC: Boodmoon
1. **MGE XE**

It is recommended that you create separators for each module of the guide (for example, **CORE**, **VISUALS**, **CONTENT** and so on) as well as for each subsection within a module (for example, **Patches**, **Fixes**, **User Interface** and so on). Right-clicking on a separator and choosing "Select Color" from the dropdown menu allows you to choose a colour for your headings. I recommend coloured module separators and default separators for the subsections.

# MGE XE
The Morrowind Graphics Extender (MGE XE) is another essential fix. Among its other changes, it also supports and comes packaged with the MWSE 2.1 beta, the lua-based script extender. It works out of the box. Like the Morrowind Code Patch, MGE XE must be installed manually.

## [MGE XE](https://www.nexusmods.com/morrowind/mods/41102?)
1. Download the **MGE XE Manual Install** Main File
1. Extract all the contents **except "Data Files"** to your Morrowind root directory
	- If you have unpacked correctly, the MGEXEGui.exe should be in the same folder as the Morrowind.exe
1. Within your root directory, right-click the **MWSE-Update.exe** and select **Run as Administrator**
	- (You may need to add this executable to your anti-virus whitelist) 
	- Allow the update process to take place. The command-line window will automatically close when this process is done

There is one additional installation step to complete:
1. In the MGE XE mod archive, zip the remaining folders in **Data Files** (**meshes**, **shaders** and **textures**) and name this archive **MGE XE - Data Files**
1. Install this file in MO2

Congratulations: you've just installed your first mod.

## Shaders
Next, download the following MGE XE shaders. Install these with MO2:
1. [MGE XE Land Bias Fix](https://mega.nz/file/ft5hUJ5L#-5Y533Rtwy2uX5moycm4pQjEDXClyFGl78XMDvfVzME) a small tweak to the distant land height bias to reduce clipping/seams
1. [MGE XE Shader - deband_fogaware](https://mega.nz/file/W8x3RTCK#w94LPJSeym5h82KUOg8SbkIoS8M7E-9Xm2Lar0gjqXw) an improved fog shader
1. [MGE XE Shader - EdgeAA](https://mega.nz/file/HwxVXbQY#eSxnVWTbC165OC1EyC-P9IahvH05We88pyba-fy2ePI) improved anti-aliasing, to be used with MGE XE's AA settings

You should now have four mods installed and enabled (i.e ticked) in your MO2 left pane: the MGE XE Data Files, and the above three shaders.

## Launching MGE XE
Once the shaders have been installed, launch MGE XE through Mod Organizer:
1. Launch Mod Organizer 2
1. From the dropdown menu on the right pane (to the left of the big "Run" button) select **MGE XE**
1. Click **Run** to run the executable

MGE XE consists of five tabs with configurable options: Graphics, Distant Land, In-Game, Config, and Instructions. There are a number of MGE XE options to enable now:

## Graphics Tab
The features in this section are mostly self-explanatory. 

Under the "Display" section: Select your display resolution, set Anti-Aliasing (AA) and Anistropic Filtering (AF) (check the Config tab to report the max AA/AF your hardware supports). Enable borderless fullscreen windowed mode. Enable Vsync only if not already enabled through your GPU hardware options (if using an Nvidia card, this is enabled through the Nvidia Control Panel).

In the "Renderer" section: tick "Auto FOV" and set the FPS limiter to your preferred cap (although 60 FPS is realistically the upper limit). For "Fog Mode" ensure that "Range vertex (Best)" is selected. "Mipmap LOD Bias" should be 0.

"Shaders" requires some setup:
1. Tick the "Enable shaders" checkbox and then click "Shader setup..."
1. Select the High quality preset. 
1. Click the "Modding >>>" button and ensure the following shaders are listed under the "active shaders" tab in this order:
	- SSAO Fast
	- Underwater Interior Effects
	- Underwater Effects
	- Sunshafts
	- Bloom Soft
	- EdgeAA
	- Eye Adaptation (HDR)
	- deband_fogaware
	
You will need to run MGE XE at the end of your mod installation to regenerate distant land and enable mod-specific shaders.

## Distant Land Tab
Distant Land does what it says. My personal settings ensure a low performance impact and cleave to the original foggy aesthetic. 

The **Distant land generator wizard** lets you select which plugins MGE XE will use when generating distant land. I recommend selecting **Use current load order**. When you click **Continue** a prompt will offer you three options to generate distant land:
- **Automatic setup will** generate distant land for you according to pre-defined settings
- **Customize setup** will let you modify the distant land generation options. I recommend this setting when generating distant land for the first time
- **Update existing distant land** will regenerate distant land according to the last used settings. If you've generated distant land previously, this is the option to use.

Click **Customize setup**. I recommend the following settings:
- Land Textures: **world texture resolution**: 2048, **world normalmap resolution**: 1024
- Land Meshes: set **world mesh detail** to high
- Statics: set **minimum static size** to 150, **Mesh detail level** to Full, **Distant texture reduction** to 1/2, and tick all the right-hand options EXCEPT "include reflective water in interiors"

Follow the prompts and allow MGE XE to complete the distant land generation. Exit the wizard when prompted. 

After MGE XE has generated distant land, in the "Distant Land" tab in MGE XE, set the **Draw Distance** to 3.0 cells. You can adjust this to your preference, but I recommend between 3-5 cell draw distance to maintain the vanilla atmosphere and keep performance cost to a minimum.

Other Distant Land settings:
- **Water**:
	- Reflections: ALL except "Blur Reflections"
	- Dynamic ripples: 10 height of waves
	- Caustics: 50%
- **XE**: enable Dynamic solar shadows
- **Auto set other distances**: By draw distance
- **Fog**:
	- Use high quality (exponential) fog: enable
	- High quality atomosphere and distance colouring: enable

You will need to run MGE XE at the end of your mod installation to regenerate distant land and enable mod-specific shaders.

## In-game Tab
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

# Plugin Cleaning
As you follow the modlist, certain mods are flagged to "require cleaning." ESPs sometimes contain dirty references and your job is to squash these bugs. You will use two tools for this: TESTool and Wrye Mash's integrated tes3cmd cleaning file.

## TESTool
The first step is to use TESTool to clean your plugins.
1. Launch Testool through MO2 (select the executable from the dropdown list in the right pane)
1. A window will prompt you if you want to use your Morrowind root folder instead of registry settings. Click **Yes**
1. Select **Options** and enable: 
	- Don't change plugin filenames
	- Retain file time, when cleaning
	- Restricted dialog cleaning
1. Select **Clean ESP/ESM Files** and click **Execute**
1. Select the relevant plugin that requires cleaning (or, alternately select ALL .esm/.esp files and check the log after for a list of cleaned plugins)

## tes3cmd cleaning
Tes3cmd catches errors that TESTool misses, and vice versa. This is a necessary step--do not skip tes3cmd cleaning!
1. Run **Wrye Mash** through MO2 (select the mash executable from the dropdown menu in the right pane)
1. Within Wrye Mash, navigate to the **Mods** Tab
1. Right-click on the relevant plugin in the lsit and choose **clean with tes3cmd**
1. The popup window will display a progress bar and print whether the mod was cleaned, or unaltered
1. Click **OK**
	
Mod Organizer 2 automatically updates your installed mod archives with your cleaned plugins. That's all!

# Wrye Mash Tools
Wrye Mash has a few additional functions you should be aware of: cleaning saves and updating a plugin masters list.

## Cleaning Saves
Any time you change your load order (removing or updating a plugin) go to the **Saves** tab in Wrye Mash:
- Select your save and click the right pane (which lists the plugins associated with the save).
- Mash will prompt you to edit/update the masters list. Click **yes**. 
- Then click **save** at the bottom of the right pane.

## Updating Masters Lists 
Go to the **Mods** tab for your list of plugins. If a plugin's checkbox colour is yellow the associated master file size does not match the plugin's. Follow these steps:
- Select the plugin and click the right pane (which lists the masters associated with the plugin). 
- Mash will prompt you to edit/update the masters list. Click **yes**. 
- Then click **save** at the bottom of the right pane.

## Registering BSAs 
The right pane of the Mods Tab has two tabs for "Mod Details" and "BSA Archives. Select the "BSA Archives" tabs and ensure each BSA archive has a check mark. This ensures the game will load the assets archived in these files. The three vanilla BSAs should already be registered. In this guide, two additional BSAs will need to be registered if you install the optional landmass mods in the **CONTENT** section.


**NEXT SECTION**:
[**Core**](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/CORE.md)