# Infinity Auto Packager

## What does this tool do?
It automatically generates Infinity Engine mod packages and adds them to release when you publish it.

## What are Infinity Engine mod packages?
- .zip package  
Standardized, universal and cross-platform Infinity Engine Mod Package with .zip file extension. It has WeiDU executable for Windows and macOS (for Linux is impossible) and .command file for macOS.
- .iemod package  
Only for mod managers. Offers a "double-click at file>extract>install" feature.

## General info
- the tool is serverless aka it will work as long GitHub will exist in any form
- packages always have latest WeiDU version
- the package version is taken directly from tp2 file

Example:
(from https://github.com/ALIENQuake/InfinityAutoPackager-Example)

![](https://camo.githubusercontent.com/dd9fba57de0ba54dd2fd176672c8998ed7e44f0f/68747470733a2f2f73352e67696679752e636f6d2f696d616765732f4e6167727977616a5f323032305f30325f31375f31355f31315f34395f3932392e676966)

## How to do the one-time installation inside you mod repository  
- By committing to the repository  
1. Open repository Settings, go to "Actions", check if you have "Enable local and third party Actions for this repository" enabled  
![Settings-Actions](https://i.imgur.com/i4fzaVf.png)
1. Download [Infinity Auto Packager](https://github.com/InfinityTools/InfinityAutoPackager/archive/master.zip) repository, extract InfinityAutoPackager-master.zip file
1. Copy '.github' folder into you top-level folder of the mod repository
1. Commit and push changes to the remote repository

- By using Github webpage directly  
<details>
<summary>Spoiler</summary>
1. Open the main page of your mod, locate "Create new file" button 
<img src="https://i.imgur.com/AdQe2jf.png">
2. paste this into the filename `.github/workflows/InfinityAutoPackager.yaml`, do not skip dot at the beginning 
<img src="https://i.imgur.com/kazdfBr.png">
3. Open <a href="https://raw.githubusercontent.com/InfinityTools/InfinityAutoPackager/master/.github/workflows/InfinityAutoPackager.yaml">Infinity Auto Packager</a> file, copy all content and paste it into the editor, then click "Commit new file" in order to save changes
<img src="https://i.imgur.com/N6PKhUW.png">
</details>


## How to use it  
1. Publish release

After a few moments, the .iemod and .zip packages will be automatically created and added to the published release. How long it takes depends on how big the mod is.
