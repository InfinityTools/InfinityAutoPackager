# Infinity Auto Packager
https://www.gibberlings3.net/forums/topic/31131-infinity-auto-packager-automatically-generate-mod-packages-when-you-publish-a-release

## What does this tool do?
A tool that automatically generates Infinity Engine mod packages when you publish a release.

## What are Infinity Engine mod packages?
They are standardized, universal and cross-platform Infinity Engine Mod Packages

- .zip package  
Standardized, universal and cross-platform Infinity Engine Mod Package with .zip file extension. It has WeiDU executable for Windows and macOS (for Linux is impossible) and .command file for macOS.
- .iemod package  
The IEMOD format (https://github.com/ALIENQuake/ProjectInfinity/wiki/Specification-of-the-IEMOD-file-format) is intended to be a platform-independent distribution format for modifications for games using the Infinity Engine. The .iemod packages are used mainly by mod managers. Among other things, they offer a "double-click at file>extract>install" feature.

## General info
- can be combined with the [ModRelease](https://forums.beamdog.com/discussion/74811/modrelease-create-new-github-release-from-commandline/p1) tool
- the package name is taken from mod metadata ini file
- the package version is taken directly from the tp2 file
- packages always have the latest WeiDU version, at the time when they were created
- the tool is a serverless microservice - it will work as long GitHub Actions will exist in any form

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
