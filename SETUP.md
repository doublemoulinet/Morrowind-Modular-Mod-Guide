[<< Home](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide) | [Next section >>](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/CORE.md)

# Setup

## Index
1. [Installation](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#installation)
	- [GOG Installation Cleanup](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#gog-installation-cleanup)
1. [Morrowind Code Patch](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#morrowind-code-patch)
1. [Wrye Mash](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#wrye-mash)
1. [Mod Organizer 2](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#mod-organizer-2)
	- [Configuration](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#configuration)
	- [Mod Installation](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#mod-installation)
	- [Creating Separators](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#creating-separators)
1. [MGE XE](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#MGE-XE)
	- [Configuring MGE XE](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#configuring-mge-xe)
	- [Distant Land](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#distant-land)
	- [Shaders](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#shaders)
1. [Tools](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#tools)
	- [Optional Tools](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#optional-tools)
	- [Tools Setup](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md#tools-setup)
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
*Note: this step applies only to users of the GOG edition of Morrowind GOTY. If you're using the Steam version, skip to the next step.*

The GOG edition of Morrowind GOTY bundles several unnecessary files. In addition to uncompressing the BSA archives (which contain all the game's meshes and textures), the GOG edition includes all of Bethesda's Official Plugins. These suck and you don't want to play with them. This guide assumes you will *not* be using the official plugins; play with them at your own peril!

Delete the following files from your ```Morrowind\Data Files``` folder:
- The **BookArt, Icons, Meshes, Textures** folders
- All **.esp** files 
- All **.txt** files

After this step, you should have only:
- Folders: Fonts, Music, Sound, Splash, Video
- BSAs: Bloodmoon.bsa, Morrowind.bsa, Tribunal.bsa
- ESMs: Bloodmoon.esm, Morrowind.esm, Tribunal.esm



# Morrowind Code Patch
#### [Morrowind Code Patch](https://www.nexusmods.com/morrowind/mods/19510?)
The Morrowind Code Patch (MCP) is an engine-level fix for the Morrowind.exe. It is an essential utility. The MCP must be installed manually.
1. Download the Morrowind Code Patch main file 
1. Extract to your Morrowind root directory (```C:\...\Morrowind```). Do not extract it to ```Morrowind\Data Files```

#### [MCP Skunk Works](https://www.nexusmods.com/morrowind/mods/26348/?tab=files)
1. Download the MCP Beta Main File 
1. Extract the contents of the MCP Beta to your Morrowind root directory (```C:\...\Morrowind```), and overwrite when prompted

## Setup
1. In your Root Folder, run **Morrowind Code Patch.exe** as an Administrator
1. Enable the following options:
	- **Beta**: every option EXCEPT *"Doppler audio fix"*
	- **Game Mechanics**: every option EXCEPT *"Allow Gloves with Bracers"*, *"Attribute Uncap"*, and *"Skill Uncap"*
	- **Visuals**: every option EXCEPT *"Over-the-shoulder third person camera,"* and *"Vanity camera lock"*
	- **Mod specific**: ensure EVERY option is enabled
	- **Interface changes**: enable every option EXCEPT *"Map Expansion (for TR),"* *"Disable map smoothing,"* *"Spell select by name,"* and *"see all standard potion effects"*
	- **International**: none
	- **Bug Fixes**: EVERY option is enabled by default--keep it this way!
1. Click the big "Apply chosen patches" button and exit

# Wrye Mash
### [Wrye Mash](https://www.nexusmods.com/morrowind/mods/45439?)
This powerful tool will be used primarily to clean and repair plugins, clean and repair game saves, enable mod-added BSA archives, and update plugin masters.
1. Download the latest x64 manual installation archive, under Main Files, **and** any x64 manual installation Update file (if applicable)
1. Extract the contents to your Morrowind root folder (```C:\...\Morrowind```). Overwrite/merge if prompted

## Setup
1. Run mash64.exe
	- The application will prompt you to select the Morrowind root directory. It will also prompt you to select an Installers path: select the ```C:\...\Morrowind\Mods``` directory you created earlier
	- **Morrowind directory**: select your Morrowind root folder (```C:\...\Morrowind```)
	- **Mods Installers directory**: you can direct the filepath to (```C:\...\Morrowind\Mopy\Mods```) or anywhere else; this guide will not use Wrye Mash's Mods Installers functionality
	- **Mlox directory**: You can ignore the mlox optional path for now
1. When prompted to enable support for 1024 plugins, choose "Yes"
1. Continue through the prompts and conclude the initialization process when prompted

Important: you *must* enable support for 1024 plugins. Currently, with this option disabled the save-cleaning tools are not working

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
```
DLC: Tribunal
DLC: Bloodmoon
```
Plugins are listed on the right pane; this is your **load order**. Morrowind loads plugins in descending order, meaning plugins closer to the bottom of the list will overwrite those at the top in the event of a conflict. On the right pane, ensure the list is as follows:
```
Morrowind.esm
Tribunal.esm
Bloodmoon.esm
```
## Profiles
Now that MO2 has been successfully installed, follow these steps to configure your MO2 profile:

- Click on the ID card icon along the top menubar to open the **Profiles** menu
- Tick **Use profile-specific Save Game files** and **Use profile-specific INI files**. Ensure that Automatic Archive Invalidation is **NOT** enabled
- Select the **Default** profile, and select **Rename**. In the text box, rename this profile to **Vanilla** and click OK
- With the **Vanilla** profile highlighted, select **Copy** and when prompted, title this new profile **Modular** or whichever profile name you like. Click **OK** and close the profile window.

On the **Profile** drop-down menu below the top menubar, be sure to select **Modular** or whatever you've named your modded installation profile. This is the profile you will be modding, and ensures you can easily revert to the Vanilla profile to deactivate all your mods.

## Mod Installation
MO2 will not only organize our installation and plugin order but will also handle downloading and installing mods as well.

In the initial setup for MO2 you should have clicked "yes" when prompted to associate MO2 with NXM (nexusmods) download links. If not, or for whatever reason this setting is reverted, navigate to **Settings** (the wrench and screwdriver icon) and click the **Nexus** tab. Click the **Associate with "download with mangager" links**.

Mods can be downloaded and installed one of two ways:
- **Mod Manager Download**: the preferred option when downloading mods from [Nexus Mods](https://www.nexusmods.com/morrowind); click the button of the same name when downloading from the website.
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

For readability, I recommend that you create separators for each module of the guide (for example: **CORE**, **VISUALS**, **CONTENT** and so on) as well as for each subsection within a module (for example: **Patches**, **Fixes**, **User Interface** and so on). Right-clicking on a separator and choosing "Select Color" from the dropdown menu allows you to choose a colour for your headings.

# MGE XE
The Morrowind Graphics Extender (MGE XE) is another essential fix. Among its other changes, it also supports and comes packaged with the MWSE 2.1 beta, the lua-based script extender. It works out of the box. Like the Morrowind Code Patch, MGE XE must be installed manually.

### [MGE XE](https://www.nexusmods.com/morrowind/mods/41102?)
1. Download the **MGE XE Manual Install** Main File
1. Extract all the contents **except "Data Files"** to your Morrowind root directory

There is one additional step to complete:
1. In the mod archive, delete the **XE Sky Variations.esp**
1. Make a .zip/.rar of the remaining files/folders in **Data Files** and name this archive **MGE XE Data Files**
1. Install manually with MO2

Congratulations: you've just installed your first mod.

## Updating MWSE
You need to run the MWSE updater at least once after installing MGEXE. You should also update MWSE regularly, whenever you install or update MWSE mods.
1. Within your root directory, right-click the **MWSE-Update.exe** and select **Run as Administrator**
1. The command-line window will automatically close when this process is done

## Launching MGE XE
Once the shaders have been installed, launch MGE XE through Mod Organizer:
1. Launch Mod Organizer 2
1. From the dropdown menu on the right pane (to the left of the big "Run" button) select **MGE XE**
1. Click **Run** to run the executable


# Configuring MGE XE
MGE XE consists of five tabs with configurable options: Graphics, Distant Land, In-Game, Config, and Instructions. There are a number of MGE XE options to enable now.

## Graphics Tab

![Screenshot](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/assets/MGEXE_graphics.jpg)

- Under **Display**: 
	- Select your display resolution
	- Set **Anti-Aliasing (AA)** and **Anistropic Filtering (AF)** (check the Config tab to report the max AA/AF your hardware supports) 
	- Enable **windowed mode** and **borderless fullscreen**
	- Enable **Vsync**
- Under **Renderer**: 
	- Tick **Enable shaders** (we will set these up later)
	- (Optional) Tick **Display FPS** to show your framerate in-game
	- Optional) Set the **FPS limiter** to your preferred framerate cap (**60 FPS** is realistically the upper limit on modded setups)

## In-game Tab

![Screenshot](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/assets/MGEXE_ingame.jpg)

Under **Options** tick the following:
- Skip opening movie
- Crosshair autohide
- Responsive menu caching

Under **Morrowind engine settings**, tick the following:
- Allow yes to all load errors
- Show subtitles
- Allow screenshots
- Thread loading
- Hit fader

## Distant Land
The Distant Land tab does what it says: it generates the distant land that, in-game, allows you to see past the currently rendered cell.

Most options are disabled when you first open this tab. You need to generate distant land for these options to become accessible. The **Distant land generator wizard** lets you select which plugins MGE XE will use when generating distant land, and will guide us through the process:
- Click the **Distant land generator wizard** button
- On the **Distant Land Setup Wizard**, click **Select all**. These ticked plugins will be used in distant land generation
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
	- Set **Mesh detail level** to **Full**
	- Set **Distant texture reduction** to **1/2**
	- Tick all the right-hand options **except** for **include reflective water in interiors**
	- Click **Create Statics**
- Once the process completes, click **Finish**

>Generally, you should regenerate your distant land any time you install or uninstall mods with plugins. Fortunately, this process will be much simpler as you will only need to click on **Run above steps using saved / default settings** the next time you use the **Distant land generator wizard**.

![Screenshot](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/assets/MGEXE_distantland.jpg)

After MGE XE has generated distant land, you will be returned to the **Distant Land** tab from earlier. Now, all the previously unavailable options can be set up. Follow the settings as suggested in the screenshot above. You may wish to tinker with them later. These recommended settings cleave to the game's original foggy aesthetic and keep performance costs to a minimum.

>You will need to run MGE XE at the end of your mod installation to regenerate distant land and enable mod-specific shaders.

### **Optional step: creating a distantland mod folder**
You may optionally move your newly-generated Distant Land files from their default location in the Mod Organizer 2 "Overwrite" folder:
1. Exit MGE XE and return to the MO2 interface
1. Located to the right of the Profile drop-down menu, click the small hammer-and-wrench icon and select "Create Empty Mod"
1. Name this mod "Distant Land - Vanilla" and make sure it is at the bottom of your load order
1. At the bottom of your load order, double click on the "Overwrite" folder
1. Drag and drop the "distantland" folder into the empty mod

>The advantage of this step is that you will always have vanilla distant land that you can easily revert to. This is useful both for testing purposes, or if you want to keep multiple install profiles and preserve a ready-to-go "vanilla" setup. With this complete, you may now relaunch MGE XE and continue the setup.

# Shaders
The default MGE XE shaders are excellent, and this guide sticks with them. That said, there are a few tweaks we can enable to improve them. Note that shaders are, along with distant land, the most performance-intensive parts of the game. The shaders and settings I recommend look great 

## Installing Shaders in MO2
Download the following MGE XE shaders. Install these manually with MO2:
#### [MGE XE Land Bias Fix](https://mega.nz/file/ft5hUJ5L#-5Y533Rtwy2uX5moycm4pQjEDXClyFGl78XMDvfVzME) 
- A small tweak to the distant land height bias to reduce clipping/seams
#### [MGE XE Shader - deband_fogaware](https://mega.nz/file/W8x3RTCK#w94LPJSeym5h82KUOg8SbkIoS8M7E-9Xm2Lar0gjqXw) 
- An improved fog shader
#### [MGE XE Shader - EdgeAA](https://mega.nz/file/HwxVXbQY#eSxnVWTbC165OC1EyC-P9IahvH05We88pyba-fy2ePI) 
- Improved anti-aliasing, to be used with MGE XE's AA settings

Place these 3 new mods under the **MGE XE** separator in your install order, directly beneath the **MGE XE Data Files** mod you created earlier.

## Configuring Shaders in MGE XE
Now that the shaders have been installed in Mod Organizer 2, they can be enabled in MGE XE.

### Graphics Tab
- Under **Renderer**, ensure that **Enable shaders** is ticked
- Click the **Shader setup...** button
- On the popup menu **Set active shaders**, click **Modding >>>**
	- Double-clicking on the shaders under **Available shaders** transfers them to the **Active shaders** list, meaning the game will use them
- Set up your **Active shaders** chain as follows:
```
SSAO Fast
Underwater Interior Effects
Underwater Effects
Sunshafts
Bloom Fine
EdgeAA
Eye Adaptation (HDR)
deband_fogaware
```
- Click **Save** after setting up your shader chain and exit MGE XE

>Note that you will have to repeat this step at the end of the mod guide if you install any mod-added shaders!

# Tools
These modding tools will be used for several key steps in this guide: mod cleaning, merged patch creation, and plugin editing/fixing. These are required.

### [tes3cmd](https://github.com/john-moonsugar/tes3cmd/releases)
This powerful command-line tool cleans mods and will be used to build a multipatch at the end of the mod guide.
1. Download the latest [tes3cmd](https://github.com/john-moonsugar/tes3cmd/releases) release (v0.40 pre-release 2)and extract the tes3cmd.exe to your ```Morrowind\Data Files``` folder. Do not install tes3cmd to the root directory
1. Download the [tes3cmd multipatch](https://mega.nz/file/D1pmHQBJ#9YMB2pyRLAFHqBczqQhqXvzNtaDW7yqwIH4Mt9MuEpA) and extract the tes3cmd_multipatch.bat to your ```Morrowind\Data Files``` folder. Do not install  to the root directory

### [TES3Merge](https://www.nexusmods.com/morrowind/mods/46870?tab=files)
This tool will automatically patch mod conflicts by generating a merged patch. This patch will be used in conjunction with tes3cmd's multipatch. 
1. Extract the contents to ```...\Morrowind Mods\Tools\TES3Merge```

###  [TES3View](http://www.mediafire.com/file/g10ay0bqynval8s/TES3View_%2528xEdit_4.1.3a_EXTREMELY_EXPERIMENTAL%2529.zip/file)
This experimental tool is an advanced GUI conflict viewer similar to xEdit for later TES/Bethesda games. It has more limited functionality than the latter but still provides excellent GUI for plugin conflicts. 

Download the xEdit 4.1.3a experimental build on MediaFire (courtesy of Sigourn). This download has already renamed the folder and .exe to TES3View in order to enable the tool to work in Morrowind
1. Extract the folder to ```...\Morrowind Mods\Tools\TES3View```

### [TESAME](http://mw.modhistory.com/download-95-5289)
TESAME is a useful mod editing program that can delete bad and unwanted references within a plugin.
1. Extract the folder to ```...\Morrowind Mods\Tools\TESAME```

### [TESTool](https://www.nexusmods.com/morrowind/mods/47473)
TESTool is a mod repair and management tool. You will use it to clean your plugins.
1. Download manually and extract the contents to ```...\Morrowind Mods\Tools\TESTool```

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

And in the inimitable words of Sean Connery, "here endeth the lesson." Go forth and mod...

**NEXT SECTION**:
[**Core**](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/CORE.md)

[<< Home](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide) | [Next section >>](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/CORE.md)
