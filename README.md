# ZX Spectrum Next Dev Primer

So you want to start developing for the ZX Spectrum Next?
This guide tries to provide an up-to-date overview of the best options to start your development journey.

## Who's This Guide For

This guide is for those with some experience writing software for other platforms - like myself - but without past experience of C or Z80 assembly language (or would prefer to avoid). 

> Aside: On-Device Development
>
> Some people prefer to embrace the full retro experience and develop games and other applications for the Spectrum Next on the device itself. This is a perfectly valid way to go about things and I tip my hat off to those people.  I have chosen not to cover this option in the guide as I prefer the convenience of modern day hardware, operating systems and tools to make my life easier. I guess I'm just lazy.

The rest of this guide will focus on off-device development using Windows, Mac or Linux.  

I deliberately call out all three platforms because I want to ensure this guide supports users on any of the three platforms. The ZX Spectrum Next is a niche platform (though happily growing).  I feel it's important we support as many people as possible developing software for it - creating a vibrant community of new software.  Using cross-platform software ensures we don't exclude anybody based on their existing equipment. I myself am a MacOS user and find it frustrating when I find a useful tool that's Windows only. In that same spirit I'm also trying to build this guide around free or pay what you like tools.

So choices must be: **cross-platform**, **free (or pay what you want)**, **easy to use**.

## Language: Boriel Basic with NextLib

[Boriel Basic](https://zxbasic.readthedocs.io/en/docs/) seems to provide a good balance between power, performance and complexity. Using the [NextLib](https://github.com/em00k/NextBuild/blob/master/Scripts/nextlib.bas) library for Boriel gives access to most (all?) of the Next's unique hardware features.  Boriel Basic is also a good choice for development for other Z80 based systems (including Spectrum 48k/128k) so there is lots of books, articles and forums for help as well as some IDE support. Many games have been written using Boriel Basic - including some "Crash Smash"-es.

> Warning
>
> I recall reading that not all version of the Boriel Basic compiler work with all versions of NextLib.  Can't find the reference at the moment.

Options ruled out:

- [NextBASIC](https://wiki.specnext.dev/NextBASIC) - Easy to use, ok performance and new commands cover all the Next's unique hardware features.  Isn't compiled and doesn't support inline Assembly.
- [C with z88dk](https://github.com/z88dk/z88dk) - High performance and libraries cover most (all?) Next's unique hardware features. Steep learning curve. Can also be used for 48k/128k development. Good choice for those already proficient in C.
- [ASM with sjasmplus](https://github.com/z00m128/sjasmplus) - Ultimate performance and hardware access.  Super hard mode!  Can also be used for 48k/128k development. Good choice for those already proficient in assembly language.

## IDE: Visual Studio Code

[Visual Studio Code](https://code.visualstudio.com) (VS Code) is probably one of the most popular free coding environments.  Its free and cross-platform. Yes **you** can use VIM if you like - I'm trying to make things simple.  A custom IDE would probably give the smoothest experience but it will be hard to compete with the quality of life features and support of VS CodeThe VS Code extension [ZX Basic](https://marketplace.visualstudio.com/items?itemName=jsjlogin.zxbasic) provides syntax highlighting support.

Options ruled out:

- [BorIDE](https://github.com/em00k/NextBuild/tree/master/BorIDE) - Bundled with NextBuild. Windows-only so would require Wine or similar. Abandoned?
- [ZXBasicStudio](https://github.com/boriel-basic/ZXBasicStudio) - A custom built IDE for Boriel Basic.  Multi-platform. Can be used for 48k/128k. Need to evaluate.

For future consideration: 

- (New) [NextBuild Studio](https://github.com/em00k/NextBuildStudio) - New kid on the block.  Currently in closed beta.

## (Game Dev) Sprite Editor: Remy's Sprite Editor (Needs more investigation)

[Remy's Sprite Editor](https://zx.remysharp.com/sprites/)  is a beginner-friendly free online (works offline too) sprite editor that runs in the browser and seems to have basic functionality required.

Options ruled out:

- [UDGeeNext](https://www.specnext.com/forum/viewtopic.php?f=7&t=351) - Bundled with NextBuild. Windows-only so would require Wine or similar. Abandoned?

For future consideration:

- [Aseprite](https://www.aseprite.org) with [Spectre Plugins](https://github.com/spectrepaul/blog/tree/main) - Richly featured cross platform sprite editor, which I believe is free, if you compile from source.  Spectre plugins make Next compatible assets. Compilation needs investigation - if easy could be good choice.
- (New) [NextBuild Studio's Sprite Editor](https://github.com/em00k/NextBuildStudio) - New kid on the block.  Currently in closed beta.

## (Game Dev) Tile Map Editor: Remy's Tile Map Editor (Needs more investigation)

[Remy's Tile Map Editor](https://zx.remysharp.com/sprites/#tiles)  is a beginner-friendly free online (works offline too) tile map editor that runs in the browser and seems to have basic functionality required.

For future consideration
- [Tiled](https://thorbjorn.itch.io/tiled) with [Spectre Plugins](https://github.com/spectrepaul/blog/tree/main) - Richly featured cross platform tile map editor which you can pay what you want.  Spectre plugins make Next compatible assets.
- (New) [NextBuild Studio's Map Editor](https://github.com/em00k/NextBuildStudio) - New kid on the block.  Currently in closed beta.

## (Game Dev) Music/Sound Editor: Remy's AYFX Editor (Needs more investigation)

[Remy's AYFX Editor](https://zx.remysharp.com/audio)  is a beginner-friendly free online (works offline too) audio editor that runs in the browser and seems to have the basic functionality required.

Options ruled out:

- [Vortex Tracker](https://bulba.untergrund.net/vortex_e.htm) - Windows-only so would require Wine or similar.

For future consideration:

- [Arkos Tracker](https://www.julien-nevo.com/arkostracker/index.php/download/) - Looks fully featured is free and cross platform.
- (New) [NextBuild Studio's AYFX Editor](https://github.com/em00k/NextBuildStudio) - New kid on the block.  Currently in closed beta.

## Emulator: CSpect (Needs more investigation)

[CSpect](https://mdf200.itch.io/cspect) seems to be the most common choice.  Reportedly more user friendly and suitable for development. Has a built-in in debugger but unless developing in asm then is it that useful. It is a .NET binary so needs Mono installed :(.

Options ruled out:

- [ZEsarUX](https://github.com/chernandezba/zesarux) - Has many more features, and can emulate many different platforms but is perhaps a bit more complex to use?  More suitable for users than for development?


## Putting It Together:  Unclear

How are all these tools installed and kept up-to-date?

The options worth considering:

### Option 1: NextBuild + Remy's Specturm Tools Website

The [NextBuild](https://github.com/em00k/NextBuild) project is designed to make it easy for developers to install and configure their dev environments.  This would involve:

- Install VS Code
- Install Python + Mono on dev machine
- Copy project zip to dev machine.
- Open the `Sources` folder in VS Code
- Choose your example and use the provided VS Code tasks to build and run.
- For sprite and sound tools use Remy's online tools.

Tool and library updates can be through VS Code Task (Needs Powershell?)

> I have some difficulties with NextBuild:
> 
> - It contains some tools that aren't easy for me to run - namely BorIDE and UDGeeNext (these might be abandoned?),
> - I think it has been recently re-worked to use Python scripts to perform builds (which is good) but the older Windows-specific scripting is still there (for backwards compatibility?)
> - Adding my own projects to the `Sources` folder which contains the examples is not a way I'm used to working.
> - It seems to contain two copies of NextLib - one in Scripts and one in zxbasic.  Which one is used?
> - It's a bit weird storing application binaries in Git.

### Option 2: NextBuild fork + Project Template + Remy's Specturm Tools Website

Address some of my difficulties with NextBuild by forking the project to:

-  Remove BorIDE, UDGeeNext
-  Remove all .bat files
-  Remove NextBuildLaucher.exe
-  Set env vars to point at tools

Create a reusable project template used as the basis for each new dev project. The template project has the `.vscode` folder from NextBuild but:

- Update task paths to use env vars
- Address tasks using powershell
  - Could probably remove task "Update Nextbuild..."
  - What to do with task "Run compiled TAP"?

### (New) Option 3: NextBuild Studio

NextBuild Studio from its description looks amazing.  Based on VS Code + Boriel Basic with built-in sprite and audio editor. However, the only build currently available is a Windows only build so I'd have to mess about with Wine to evaluate how this works.  I'm waiting on a MacOS build :).

If it:

- is cross platform
- free (or pay what you want)
- bundles all the required tools into a single installer/package
- allows me to manage my own development projects in my own separate GitHub repositories

This could be the perfect solution! I think this could really open up development for the Next.  Exciting!
