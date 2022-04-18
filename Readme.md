# Legend of SkyrimVR Install Guide

- **[1] [Introduction](#introduction)**

- **[2] [Recommended Specs for LoSVR](#recommended-specs-for-losvr)**

- **[3] [Gameplay Prep](#gameplay-prep)**

    - [3a] [SkyrimVR Install](#skyrimvr-install)

    - [3b] [Visual C Runtime Installs](#visual-c-runtime-installs)
    
    - [3c] [Windows Antivirus and Firewall Settings](#windows-antivirus-and-firewall-settings)

    - [3d] [Windows Paging File Size](#windows-paging-file-size)
    
    - [3e] [Wabbajack and LoSVR Install](#wabbajack-and-losvr-install)
    
    - [3f] [SkyrimVR ini Tweaker](#skyrimvr-ini-tweaker)
    
    - [3g] [CPU Threads](#cpu-threads)
    
- **[4] [MCM Recorder Auto-Load Settings](#mcm-recorder-auto-load-settings)**
    
    - [4a] [Fine-Tuned Challenge](#fine-tuned-challenge)
    
    - [4b] [LoSVR Monster Population](#losvr-monster-population)

    - [4c] [Nethers Follower Framework](#nethers-follower-framework)

- **[5] [The Sharper Eye](#the-sharper-eye)**

- **[6] [TAA On or Off](#taa-on-or-off)**

- **[7] [Nvidia Settings](#nvidia-settings)**

- **[8] [SkyrimVR and SkyrimPrefs ini](#skyrimvr-and-skyrimprefs-ini)**

- **[9] [DO NOT SORT LoSVR WITH LOOT](#do-not-sort-losvr-with-loot)**

- **[10] [INSTALL IS COMPLETE](#install-is-complete)**
#
[1]
## INTRODUCTION
![Legend of SkyrimVR 668 Small Logo](https://user-images.githubusercontent.com/78007822/160729993-f8922d2a-b9b5-45d2-8121-fb03ab03e8b9.png)
### Legend of SkyrimVR is a high fantasy theme-based mod list that pays homage to the Zelda series by adding 12 Zelda inspired mods and so much more, this includes:

 - **Green Rupees.**
 - **Hookshot Claw.**
 - **Epona, Links Horse.**
 - **The Abandoned Deku Tree**
 - **Hylian Race - Play as Link.**
 - **A Custom Tri-Force Intro Logo.**
 - **Randomly Enchanted Hylian Loot.**
 - **Princess Zelda Follower and Her Attire.**
 - **A Hyrule Castle Player Home with the Iron Knuckle Follower.**
 - **Discover Unique Monsters Mixed with Old and New Zelda Creatures.**
 - **A Subtle Mix of Vanilla and High Performance Cartoon Stylized Textures.**
 - **A DLC Sized Legend of Zelda Mod - Relics of Hyrule, With So Much to Discover.**
 - **Legend of Zelda Music Intro with Full In-Game Zelda Music & Sound FX Overhaul.**
 - **Legend of Zelda Oracle of Seasons' Tarm Ruins, an Adventure for High Level Players.**
#
[2]
## RECOMMENDED SPECS FOR LoSVR

**Legend of SkyrimVR should run well on medium to high end HMD/PC configurations, I focused heavily on optimizing all performance related settings via ini files, mods, tools and using a low 512k res DynDOLOD configuration for hybrid 3D trees.**

**Minimum Recommended Specs for LoSVR: 20xx graphics card (1080 should still work but it might be laggy without further performance tweaking than this install guide provides, users will need to troubleshoot these issues on their own), AMD Ryzen 7 or Intel 7, 16GB RAM, Solid State Drive (SSD Must be used, Do Not Use a traditional HDD).**

**This should be a good start for decent performance.**

**Additionally, VR controller functionality and physics are all enhanced or improved through various tools, mods and .ini settings.**

**The initial wabbajack install file size is around 3.5 GB with a complete LoSVR install size of 76 GB (roughly 80 GB total), it’s HIGHLY RECOMMENDED that you install this on a NVMe M.2 SSD for optimal performance, although traditional SSD should be fine.**

**Since I use a Rift S, the skyrimvr.ini files will reflect that, so a few of these .ini settings will need to be adjusted to suit your specific HMD and PC. I will go over that and other recommended settings throughout this guide.**

### LoSVR is developed and tested with this HMD and PC setup:

 - **Oculus Rift S**
 - **Win 10 ver.20H2 Fully Updated**
 - **Ryzen 7 3800x AMD Processor**
 - **32 Gigs of G-Skill 14-34 Low Latency RAM**
 - **Kingston NVMe M.2 1tb SSD**
 - **Nvidia 3090 GPU**
#
[3]
## GAMEPLAY PREP
### **From here forward I will be using 2 terms over and over.**
### **HIGHLY RECOMMENDED  and  CRITICAL.**
### **HR is IMPORTANT, but also with flexibility towards other configurations if the user desires.**
### **CR is MANDATORY, to make the game run properly, or as LoSVR was intended to run, in all aspects.**
### **PLEASE pay attention to these words thoughout the rest of this guide.**
#
[3a]
### SkyrimVR Install
 - **It is CRITICAL to have a 100% fresh install of SkyrimVR available & ready to play, It is also CRITICAL to have your SkyrimVR game installed in a folder OUTSIDE of  C:/Program Files  and  C:/Program Files (x86) <- ignore these 2 folders for the entire process of this install guide, due to possible admin rights restrictions.**
 
 - **Steam does not easily allow for new install folders, simply follow [This Easy Guide](https://drive.google.com/drive/folders/1lOBFqblzA23AbXFz-usTejOKR5UFsPjA?usp=sharing) to change that.**
 
 - **After you have confirmed SkyrimVR is installed in a folder outside of those 2 mentioned above, start the default Steam version of SkyrimVR to have the game create the appropriate .ini file in the documents folder on your C drive, once you see the Bethesda logo pop up, you can close the game and continue following this install guide.**
#
[3b]
### Visual C Runtime Installs
 - **It's CRITICAL to install the All-In-One [Visual C Runtime Packages](https://www.techpowerup.com/download/visual-c-redistributable-runtime-package-all-in-one/) available if you don't already have it, as the Feb 2022 release is a requirement for the 3D audio files from the [Binaural 3D Surround Sound for SkrimVR](https://www.nexusmods.com/skyrimspecialedition/mods/26916?tab=description)** mod on the Nexus, simply install the AIO package to cover all Visual C updates.
#
[3c]
### Windows Antivirus and Firewall Settings
 - **It's CRITICAL to add SkyrimVR.exe and ModOrganizer2.exe (LoSVR) to your Windows Antivirus Exclusion settings to prevent random CTD (even if you have antivirus turned off, it still background scans.)**
**Go to Start > Settings > Update & Security > Windows Security > Virus & threat protection, under Virus & threat protection settings, select Manage settings, and then under Exclusions, select Add or remove exclusions.**
**Select Add an exclusion, and then select SkyrimVR.exe and do this a 2nd time to pick the Steam folder and ModOrganizer.exe.**

![v1-420](https://user-images.githubusercontent.com/78007822/147438064-82fd9c74-a749-472e-95f8-4b448e37cd2b.png)
![v2-420](https://user-images.githubusercontent.com/78007822/147438073-0799b866-fbd4-4344-a00f-bc776c81b588.png)
![v3](https://user-images.githubusercontent.com/78007822/147438122-4d442b97-0aa9-45b7-99f6-352a612ad8a2.png)
### **This screenshot above shows a Diabolist VR folder, simply use this same method to direct the exclusions to your Legend of SkyrimVR folder.**
#
 - **It is also CRITICAL to BLOCK SkyrimVR.exe (Inbound & Outbound), within your windows firewall settings, to prevent random CTD produced by Bethesda server pings.**
 - **Open your windows search function and type in Firewall, then click on 'Windows Defender Firewall with Advanced Settings.**
#
![Firewall Settings 1](https://user-images.githubusercontent.com/78007822/140569744-80e05750-decc-48e4-976e-a84ac707259a.png)
 - ### **When the Windows firewall options pop up, follow these steps below:**
 - **1. Click Inbound Rules**
 - **2. Click New Rule**
 - **3. Click Program, then Next.**

![Firewall Settings 2](https://user-images.githubusercontent.com/78007822/140570706-82949ebb-a4eb-47a4-ae45-13f6f6031696.png)
 - ### **Now direct this window to your SkyrimVR root folder and select SkyrimVR.exe**
![Firewall Settings 3](https://user-images.githubusercontent.com/78007822/140577020-ba21dac5-6462-4fdc-b5bf-25893ec53587.png)
 - ### **Make SURE you select BLOCK, another window will pop up with Domain, Private and Public, make sure they are all selected.**
![Firewall Settings 4](https://user-images.githubusercontent.com/78007822/140572008-768a8955-f3a7-4cdc-8a3c-aa9dec013d86.png)

![Firewall Settings 5](https://user-images.githubusercontent.com/78007822/140572430-5546eb0d-5fea-4ed7-8b4c-a9242217ebb2.png)
 - ### **Just name this to whatever you want, or use what I have put in the screenshot provided, then click finish.**
![Firewall Settings 6](https://user-images.githubusercontent.com/78007822/140572798-048e221d-0f9e-43dd-a3af-9984fca91ac8.png)
## **NOTE: MAKE SURE YOU REPEAT THE EXACT SAME STEPS FOR OUTBOUND BLOCK.**
[3d]
### Windows Paging File Size
 - **It is CRITICAL to set your pagefile size to 20GB (20,000mb).**
 - **20GB is the modded SkyrimVR standard if you have 16GB RAM, I personally use 40GB pagefile size with 32GB of physical Ram, as I prefer the extra overhead.**
 - **Use this number for both the initial size and max size on 1 free SSD with enough space.**
 - **There is no need to apply this pagefile size setting to multiple hard drives.**
 - **Keeping your Windows drive (typically the C: Drive) set to SYSTEM MANAGED SIZE Is HIGHLY RECOMMENDED while using the pagefile setup with 1 free hard drive in this fashion & how to configure the Windows Paging File Size is explained [HERE](https://www.howto-connect.com/tweak-paging-file-for-better-windows-10-performance/)**
#
![Virtual Memory](https://user-images.githubusercontent.com/78007822/139851096-1b8f5275-4070-48ed-b974-58e80fb25349.png)
#
[3e]
## Wabbajack and LoSVR Install

### A NEXUS PREMIUM ACCOUNT IS HIGHLY RECOMMENDED, OTHERWISE 500+ MODS WILL HAVE TO BE DOWNLOADED MANUALLY.😵

- **First, download and install the current Wabbajack software linked [HERE](https://github.com/wabbajack-tools/wabbajack/releases)**
- **This Wabbajack software is a hard requirement for LoSVR to install and work properly.**

- **Next, download the current Legend of SkyrimVR install file linked [HERE](https://drive.google.com/drive/folders/1R1UmyClHVED0ivP-J0HBWvv0oqpN9aDR?usp=sharing).**

- **While it's downloading, make a folder on the SSD drive you'll be using and label it LoSVR.**

- **IMPORTANT REMINDER: -DO NOT- install ANYthing into your C:/Program Files or C:/Program Files (x86) folders, due to admin restrictions.**

- **Open your Legend of SkyrimVR wabbajack file and on the bottom right select the Install Location ( 3 Dots ... ) select the LoSVR folder you created, the download section will automatically pick the mod folder for you inside of itself, or you can select a different folder to keep the downloaded zipped mods separate, it’s your choice.**

- **Now click the big blue arrow, sit back & relax while it installs, if you’re curious, you can watch the mod info that pops up to get an idea of what’s being installed, you can also download this file ➡️ [Legend of SkyrimVR 1.0.1.wabbajack.manifest.json](https://drive.google.com/drive/folders/1_5suHgHvNpEzpTxWGui9EegiW9sq31Kc?usp=sharing), then simply drag and drop it into the [Wabbajack Manifest Website](https://www.wabbajack.org/#/modlists/manifest) to see all the mods being installed, you are downloading over 500 mods so just be patient & let it finish, if it freezes then simply start the process over, to do this, open the Legend of SkyrimVR wabbajack file & click the arrow again without doing anything else & it will resume where it left off.**

- **After install is finished, close the Wabbajack window & proceed to your LoSVR folder, open the Game Files Folder, then drag & drop ALL of these files into your SkyrimVR root folder, there *should* be only 1 overwrite notification for the Skyrim.ini file, this overwrite is correct, do it.**
#
[3f]
## SkyrimVR ini Tweaker

**There are a few .ini settings you *should* be aware of, because we don’t all use the same PC / HMD, so it’s best to adjust these based on your HMD resolution and CPU threads.**

### **NOTE**: **Windows 11 users can ONLY USE MO2 2.4.2 or later**

**Look inside the LoSVR folder & open ModOrganizer.exe (2.4.4)
Once it’s open, click on this icon. ![Skyrim ini Tweaker Small](https://user-images.githubusercontent.com/78007822/139736342-91ff8313-2d95-460a-b9ab-b8483e5fbc0b.png)**
### This configuration window will pop up.⬇️
![SkyrimVR ini Tweaker Settings](https://user-images.githubusercontent.com/78007822/139736900-0332834d-5369-47de-add5-c8462af09bec.png)

**Having personalized .ini tweaks will help overall visuals based on SuperSampling settings.**

**Example: using 150% SS with SteamVR works out to 2016 x 2172 per eye on the Oculus Rift S, and this resolution is reflected with two .ini settings.**

**iHudMenuTextureSize = 2172 ... & ... iProjectedMenuTextureSize = 2172**

**These 2 sets of numbers above will always equal the largest number of your headsets resolution & they *should* be adjusted with this ini configuration tool to match your HMD, for best in-game menu texture size.**
#
[3g]
## CPU Threads
**iNumHWThreads & iNumThreads represents how many threads your CPU has, it’s set to 16 threads in the skyrimvr.ini so this will need to be changed to your own CPU threads if it is not 16, (or you can reset these two ini settings to Skyrim's default if you prefer) a good program to find out how many threads your processor is using, would be [CPUID](https://www.cpuid.com/softwares/cpu-z.html), ⬅️️ click to install, if more help is needed with this, please post in the [LoSVR / DVR Discord](https://discord.gg/wWF4Nb6JuB)**
### **You can close the SkyrimVR ini Tweaker now.**
#
[4]
## MCM Recorder Auto-Load Settings
#### Start LoSVR through SKSE on the top right section of ModOrganizer, once you finish creating a new character and you spawn into the starting area it will spam the top of your screen with MCM mods being enabled in LoSVR, It will also Auto-Load and streamline ALL Highly Recommeneded and Critical specific settings for LoSVR. These Auto-Load settings are Highly Recommended and some are CRITICAL for the best LoSVR experience. This process will give users a notification if they try to interrupt and it will warn them to let it finish, when it's done loading you will be notified.
![Please Exit Menu LoSVR](https://user-images.githubusercontent.com/78007822/160779185-30f4e395-4044-4dfb-b87a-cec5137ab18e.png)
![Finished MCM Menu LoSVR](https://user-images.githubusercontent.com/78007822/160780187-94b9d489-c7a4-4097-a1b4-f76143c802b5.png)
#### The [MCM Recorder](https://www.nexusmods.com/skyrimspecialedition/mods/61719) nexus link is provided for further information, the author provides a short YouTube video to help you fully understand how this mod works.
#
[4a]
## Fine-Tuned Challenge
#### LoSVR uses Adept difficulty by default, this is CRITICAL to utilize the Fine-Tuned Challenge mod but not mandatory to use in the game, you can use the vanilla difficulty settings without any problems, however, the dmg & spawn multiplier numbers will not function as intended if any other vanilla difficulty setting is used, this mod simply REPLACES the vanilla difficulty settings with detailed % numbers. Experiment if you want, however, Fine-Tuned DEFAULT % with ADEPT set is a good start if you want easy dungeon crawling, but for the best experience you would set the multipliers progressively higher, for example I use: Easy: 100%, Medium: 125%, Hard: 150%, Very Hard: 200%, then adjust the Dmg taken & Dmg inflicted sliders based on your preferences, I use 75% Dmg Inflicted and 125% Dmg Taken, I also take followers on my adventures, you'll probably want to aswell.
![Fine-Tuned Challenge Settings](https://user-images.githubusercontent.com/78007822/139785982-11c9f46d-1439-4129-a33e-d783dc2c8b3b.png)
-
[4b]
## LoSVR Monster Population
#### LoSVR uses several monster mods at its core which have either been repaired or enhanced with xEdit and CAO (or both), and to optimize and minimize any 4k textures down to 1k or 2k, LoSVR is hosting over 50 Mihail Monsters, Skyrim Immersive Creatures(SiC) & Relics of Hyrule (RoH) Monsters. Additionally, Skyrim Underground has it's own set of monsters spread out between 2 massive underground dungeons.
### NOTE: Adept difficulty is CRITICAL for ALL creature mods in LoSVR to work with Fine-Tuned Challenge, otherwise you will only be using vanilla difficulty settings.
#
[4c]
## Nethers Follower Framework
#### Difficulty Settings for Followers GIVING DAMAGE can be adjusted in the Nethers Follower Framework mod settings inside MCM. It is also possible to ADD custom Followers like Inigo and Lucien into the Framework so they can use the NFF rules, I have tested this feature extensively over months of playtime as I always take these followers with me on ALL playthrough adventures, and it works like a charm, Access their dialogue menu after recruiting them into your party and then simply choose the NFF Import option. Please read this very helpful [PDF Guide](https://www.nexusmods.com/Core/Libs/Common/Widgets/DownloadPopUp?id=153383&game_id=1704) from the author of this mod, if needed, as NFF has a slew of options to get acquainted with. 
#### Also included is [Ashien's Cursed Rings](https://www.nexusmods.com/skyrim/mods/64530) <--click & read the mod page for the rings location, this mod will help your followers effectively TAKE DAMAGE at higher levels, so as to not be god-like DMG sponges.
![NFF](https://user-images.githubusercontent.com/78007822/139795556-8f090a9c-5fd6-473e-98be-26f89e807455.png)
-
[5]
# The Sharper Eye
#### With SteamVR, I recommend using [The Sharper Eye](https://www.nexusmods.com/skyrimspecialedition/mods/46999/) mod with or without TAA, this mod needs to be downloaded manually and simply unziped and placed inside of the main SkyrimVR folder, It includes the preset, the required shader and a custom VR-enabled Reshade build, additionally, these are the settings I use for a relatively sharp image with and without TAA, performance mode is also available on the bottom right corner, click HOME on your keyboard to open and close this window, it will be visible on your desktop VR screen.
![The Sharper Eye](https://user-images.githubusercontent.com/78007822/139843882-792e6293-f0b9-4c05-8564-62e06bfce179.png)
-
[6]
# TAA On or Off
#### TAA makes the distant image in VR have less jaggies (shimmer), and it's turned ON by default with LoSVR, it is also enhanced by a TAA tweaking auto-load feature from FPS Stabilizer, however, if you don't want TAA, then simply disable it via the options in game when you are playing, additionally, it is CRITICAL to open your SkyrimVR ini Tweaker tool, ![Skyrim ini Tweaker Small](https://user-images.githubusercontent.com/78007822/140593759-0e282f42-2d72-472c-8f67-88fc89e86b22.png) and set bTAAWater = 0, otherwise you may see visual anomalies with water.
#
[7]
# NVIDIA Settings
#### The SkyrimVR specific nVidia Control Panel settings I have provided are for better visual clarity for the Rift S, but they likely work fine with a range of other HMDs, do some research online and feel free to experiment with your own settings if these are not sufficient for your GPU.
![SkyrimVR nVidia Settings 1 smaller](https://user-images.githubusercontent.com/78007822/162099592-df80d056-3604-4779-847d-ea3a36b6f6b8.png)
![SkyrimVR nVidia Settings 2 smaller](https://user-images.githubusercontent.com/78007822/162099809-bbbe5c6d-2871-4c45-a337-419a94ce8f6b.png)
#
[8]
# SkyrimVR and SkyrimPrefs ini
#### If you want to reset your Legend of SkyrimVR .ini files back to install defaults: [skyrimprefs.ini & skyrimvr.ini](https://drive.google.com/drive/folders/1YX6sdGIDGVBPIkMNnNCkCNa6JZMBmhul?usp=sharing) ⬅️️ click this link to get both current files and then overwrite them inside your ‘LoSVR\profiles\Legend of SkyrimVR’ folder, also make sure to grab the Skyrim.ini file and place it inside your root SkyrimVR folder.
#
[9]
# DO NOT SORT LoSVR WITH LOOT
#### LoSVR has been manually sorted from top to bottom & using loot WILL destroy the correct plugin order, if you add more mods, you will NEED to know where to place those new plugins and loose files, you will also need to incorporate them into the many custom made patches (if this is needed), additionally, I WILL NOT provide support with changing ANY aspect of this modlist. LoSVR support is EXCLUSIVE to the modlist provided, that being said, _If_ you mess up the plugins order somehow, you can simply click the circular icon on the Mod Organizer window to restore the original plugin order based on the most recent date.
![No LOOT Sorting](https://user-images.githubusercontent.com/78007822/160706286-4ae45da6-198f-4c68-9544-f1c14688a421.png)
-
[10]
# INSTALL IS COMPLETE 
 - ### You’re Ready to Play! 
 - ### Please post on [LoSVR / DVR Discord](https://discord.gg/wWF4Nb6JuB) if you need modlist support. 
# Thanks for downloading Legend of SkyrimVR! 
### ...but most importantly...
# Have Fun!!
![Legend of SkyrimVR Small 440 Logo](https://user-images.githubusercontent.com/78007822/160705710-b166b208-b7f2-4ce9-81fb-71af18df2678.png)

#### - Latest LoSVR Guide Update, 04/18/2022
