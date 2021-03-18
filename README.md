# Morrowind Modular Mod Guide
A modular, vanilla-friendly installation guide for Morrowind in 2021.

See the [Changelog](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/CHANGELOG.md) for a full list of changes.

# Module Index
1. [Introduction](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/README.md)
1. [Setup](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md)
1. [Core](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/CORE.md)
1. [Core - Expanded](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/EXPANDEDCORE.md)
1. [Visuals](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/VISUALS.md)
1. [Gameplay - Balance](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/BALANCE.md)
1. [Gameplay - Consistency](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/CONSISTENCY.md)
1. [Gameplay - Expanded](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/GAMEPLAY.md)
1. [Content](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/CONTENT.md)
1. [Content - Landmass Expansions](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/OPTIONAL.md)
1. [Finish Line](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/FINISHLINE.md)

# Introduction
This is my personal mod list for Morrowind, with an emphasis on performance and preserving the original character of the game. This is the result of years of messing around, learning the tools, and curating mods that don't suck but actually rule, man.

For a similar-looking guide, see Sigourn's [Morrowind Improved](https://github.com/Sigourn/morrowind-improved). Beginners might also see Danae's [Morrowind First Time](http://danaeplays.thenet.sk/morrowind-first-time/) guide. Some of the structure of this guide (particularly the setup section) has been adapted from Sigourn's.

This guide's selling features:
- Step-by-step instructions in a **fully modular format**--including essential, visual, balance, and quality-of-life mods.
- A curated selection of **vanilla-friendly content mods**, including settlement and dungeon expansions, new items, and quests.
- On moderate desktop hardware (ex., an i7-3770 and GTX 680), you will get a solid **50-60FPS in-game**. Dips below 60FPS should be rare.

## Note on performance:
Morrowind is a single-core application, meaning CPU load is the major performance bottleneck. A CPU with fast single-core processing speed is the key to good performance. This guide tries to keep the CPU load low, so that a range of moderate systems will get stable framerates. Mods that add lots of references to exteriors, or add lots of NPCs, should be installed sparingly.

## Using this Guide and Installing Mods
The guide is modular, meaning you can install most sections incrementally. Many of the mods in this guide can be skipped without causing mod compatibility/dependency problems. A first-time player need only follow the instructions in the first sections to have a stable, playable game. However, all sections are designed with a vanilla-friendly experience in mind. I recommend first-time players skip the "**CONTENT**"  section.

This list does not typically describe what each mod does. Read the description on the mod page, and always read the readme.

# Mod Management
My preferred mod manager is Mod Organizer 2. This is a powerful tool that allows users considerable freedom to adjust their mod installation on the fly.

If you are more familiar with Mod Organizer 2, it now has native Morrowind support. MO2's advantage is its Virtual File System (VFS), meaning you can create multiple game profiles with different mod orders on a whim. Previously, boot time was very slow as paging the VFS is not very optimized for Morrowind. However, with recent MWSE updates, MO2's slow boot times have been circumvented and I now recommend MO2 over the alternative, Wrye Mash. The initial set up for Morrowind's mod tools with MO2 is more complicated, but the rewards are worth the extra setup time.

The alternative to MO2 is Wrye Mash. While it does not have the advantage of VFS profiles, Mash has the advantage of being an older and more established tool. WM also presents more information to the user in the main interface, and is a necessary tool whether you use it to manage your installation or not--you need Wrye Mash to clean your saves, fix master dependencies, and more.

A note on terms: know the difference!
- "Installation order" refers to the order of the mod archives themselves (the packages, usually .zip or .rar but sometimes unpacked folders) in the "Installers Tab" in Wrye Mash or the left pane of MO2
- "Load order" refers to the plugin order (.esp or .esm files) in The "Mods Tab" of Wrye Mash or the right pane of MO2

**NEXT SECTION**:
[**SETUP**](https://github.com/doublemoulinet/Morrowind-Modular-Mod-Guide/blob/master/SETUP.md)