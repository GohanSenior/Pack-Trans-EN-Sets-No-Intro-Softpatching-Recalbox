




                                Twinkle Tale
                         English Translation Patch




 History
-----------------------------------------------------------------------------

070328 Initial release




 Overview
-----------------------------------------------------------------------------

This is a translation patch for the Mega Drive game "Twinkle Tale".
It sports a variable-width font engine with kerning support and, as usual,
it is a "dual-language" patch, meaning that it supports both Japanese and
English, depending on the country code of your machine.




 Applying the Patch
-----------------------------------------------------------------------------

Hopefully included with this document is a patch file in the IPS format.
You can use any program that supports that file format to apply this
translation patch to your ROM file.




 Playing the Game
-----------------------------------------------------------------------------

Once you've patched the ROM file, simply load it up in your favorite
Genesis / Mega Drive emulator, console copier, or flash cartridge.

The game will detect the country code of your machine (real or emulated) and
then switch to English or Japanese mode accordingly. This permits you to play
the game in the original Japanese, if you so desire, while taking advantage
of the improvements that this patch offers (see the list of changes).




 Q & A
-----------------------------------------------------------------------------

Q: This patch doesn't work! What do I do?

A: Make sure that your ROM file is not in an interleaved format. It's also
   possible that there is more than one version of the game, or that your
   copy is corrupt.


Q: It doesn't work with my copier / flash cartridge! Why not?

   This was tested on a real Genesis so you shouldn't have any problems in
   that respect. The most likely reason is that something went wrong during
   the patching process. See the previous question and try it in an emulator
   to see if that works.

   Another possibility is that you are using a PAL Mega Drive. This game was
   designed for NTSC systems and I didn't make any changes in that respect.
   It should still run (probably at the wrong speed), but you never know...


Q: Why is the text in Japanese?!?

A: This is a dual-language translation patch. If it detects that it is
   running on a Japanese system, it will use the original game script.
   If you are using an emulator, make sure the country code is set to USA.


Q: What's with the ugly horizontal black lines?

A: That's a clever trick the programmers used to get a cheap translucency
   or shading effect. If your emulator has a "TV" mode, you may want to
   enable it.




 List of Changes (not exhaustive)
-----------------------------------------------------------------------------

Adjusted timings in the intro and opening
Modified internal sprite structures for the stage names
Reversed directions in configuration (i.e. press right to increment)
"S.Hard" mode unlocked (probably non-functional)
Variable width font with automatic kerning




 Transliteration Notes
-----------------------------------------------------------------------------

The following table shows how some of the various names were transliterated.


SARIA   Saria
O-ROFU  Olof
DO-RA   Dohla
ERAN    Elan
GADOU   Gadou
KAIZA-  Kaiser

TARON   Talon
BAIN    Vine
ZA-DO   Zard


The name suffix "sama" was translated as "Sir". Pay attention to how it
is (and isn't) used, as it is significant.




 Hacking Notes
-----------------------------------------------------------------------------

As you may know, this is the part where I discuss various technical aspects
of the translation and complain about some of the things that annoyed me
during the development.

This project provided quite of bit of material for the latter category,
although it really wasn't that bad in retrospect.

The first great irritation came from the game's excessive use of "Line F"
simulated instructions. This made disassembly a real hassle and slowed the
process down tremendously. As if to spite me further, the developers also
decided to use the F Line (instead of Line A) which my disassembler often
interprets as FPU instructions. Although many parts of the code were quite
normal, there were entire subroutines that were completely exception driven,
right down to the simulated RTS.


The other unusual frustration came during testing on a real machine. One
never wants to find bugs on real hardware that don't show up in an emulator,
as it is much more time consuming and inconvenient to fix problems when you
have to re-flash your development cartridge every time you make a change.

In this case, it was a minor graphical glitch that was occuring occasionally,
appearing as a dark horizontal line (sometimes more than one) of varying
width. It was apparently not being caused by anything wrong in the VRAM.
After a long night of experimenting, I finally isolated the problem and fixed
it by waiting for horizontal blanking before writing to the tile map in VRAM.

Why was this a problem? While it is not unusual for game machines to have
restrictions on when VRAM can be written to, I'm not aware of any caveats
about this sort of thing for the Genesis. I suspect that the extended
processing time for my variable-width font code was exceeding the vertical
blanking time, although I didn't confirm it, and that writing to VRAM during
the display turns off the gun, or something like that. Another point of
interest is the fact that the tile loading, done immediately prior to the
tile map update, does not cause a problem, possibly because it is done via
DMA.


So, now let's talk a little bit about kerning. Kerning is a process by which
font characters overlap each other (although it's only the spacing that is
overwritten) to make certain combinations of letters look better. Before any
character is printed, the kerning function checks the preceding character to
determine if the combination needs to be adjusted, usually by looking in a
table.

Some fonts are designed such that they still look good even without kerning.
The font I wanted to use this time was not one of them, so I reworked the
variable-width font code from one of my previous translations and added
kerning support.
