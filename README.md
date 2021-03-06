# Sonic Unleashed/Sonic World Adventure
This is a **very early** WIP decompilation of the Xbox 360 version of Sonic Unleashed.

## Current Status - Stub
The tool that will be used for this project, IDA Pro, is perfectly capable of creating a disassembly for this game based on its XEX file. However, its decompiler addon is not compatible with all of the instructions used by the Xenon CPU, which is a built-in limitation of the [addon](https://hex-rays.com/products/decompiler/manual/limit.shtml). 

Because of this, about 15.4% (9,750 of 63,229) of the functions used in the game cannot have proper pseudocode created for them. Therefore, a microcode filter for the Hex-Rays Decompiler must be developed to add support for the unimplemented instructions. The list of unimplemented instructions will be given [here.](https://github.com/draiN-NEO/sonic-unleashed-decompilation/blob/main/instructions.md)

Unfortunately, I am relatively inexperienced working with the IDA SDK so if anyone is experienced with creating plugins for IDA and has extensive knowledge of PPC assembly, consider joining the Discord server and helping with the creation of this plugin so further progress can be made.

Other than that, the executable contains quite a bit of information left over in the form of strings and RTTI info (along with the associated vtables) which should allow some level of decompilability, if not all.


## Goals
* Have the functions and variables given closely-accurate and meaningful names
* Restore as many of the game's data types as possible (enums, structures, unions)
* Restore the overall class hierarchy of the program as accurately as possible
* Construct a basis from which future ports of the game can be made for other platforms


## Non-Goals
* Creating a "matching compilation"
* Recompatibility for the Xbox 360 platform


## Tools
* IDA Pro - Currently the only tool capable of creating a disassembly for an Xbox 360 XEX executable
  * HexRaysCodeXplorer - used to recreate data structures with a provided name
  * HexRaysPyTools - used to display the pieces of data stored in a variable (I found that creating structures with this addon is a bit buggy so this will only be used to see the data stored in a variable while HexRaysCodeXplorer will be used to actually create the data structures).


## Discord Server
If you're interested in helping out with the decompilation project, feel free to join the Discord server where I'll share more information about my current findings: https://discord.gg/PB7hkVBswG

## Disclaimer
All of the information in this repository is subject to change, such as the tools used for the project and the scope of the goals.
