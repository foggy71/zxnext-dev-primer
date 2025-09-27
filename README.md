# My ZX Spectrum Next Dev Primer

So you want to start developing for the ZX Spectrum Next?
This guide tries to provide an up-to-date overview of the best options to start your development journey.

## Who's This Guide For

This guide is for those with some experience writing software for other platforms - like myself - but without past experience of C or Z80 assembly language (or would prefer to avoid). 

> Aside: On-Device Development
>
> Some people prefer to embrace the full retro experience and develop games and other applications for the Spectrum Next on the device itself. This is a perfectly valid way to go about things and I tip my hat off to those people.  I have chosen not to cover this option in the guide as I prefer the convenience of modern day hardware, operating systems and tools to make my life easier. I guess I'm just lazy.

The rest of this guide will focus on off-device development using Windows, Mac or Linux.  

I deliberately call out all three platforms because I want to ensure this guide supports users on any of the three platforms. The ZX Spectrum Next is a niche platform (though happily growing).  I feel it's important we support as many people as possible developing software for it - creating a vibrant community of new software.  Using cross-platform software ensures we don't exclude anybody based on their existing equipment. I myself am a MacOS user and find it frustrating when I find a useful tool that's Windows only. In that same spirit I'm also trying to build this guide around free or pay what you like tools.

## Language Choice: Boriel Basic with NextLib

[Boriel Basic](https://zxbasic.readthedocs.io/en/docs/) seems to provide a good balance between power, performance and complexity. Using the NextLib library for Boriel gives access to most (all?) of the Next's unique hardware features.  Boriel Basic is also a good choice for development for other Z80 based systems so there is lots of books, articles and forums for help as well as some IDE support. Many games have been written using Boriel Basic - including some "Crash Smash"-es.

Options ruled out:

- [NextBASIC](https://wiki.specnext.dev/NextBASIC) - Easy to use, ok performance and new commands cover all the Next's unique hardware features.  Isn't compiled and doesn't support inline Assembly.
- [C with z88dk](https://github.com/z88dk/z88dk) - High performance and libraries cover most (all?) Next's unique hardware features. Steep learning curve. Good choice for those already proficient in C.
- [ASM with sjasmplus](https://github.com/z00m128/sjasmplus) - Ultimate performance and hardware access.  Super hard mode!  Good choice for those already proficient in assembly language.

