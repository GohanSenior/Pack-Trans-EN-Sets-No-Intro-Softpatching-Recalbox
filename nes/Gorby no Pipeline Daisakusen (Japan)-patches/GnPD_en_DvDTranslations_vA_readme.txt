-------------------------------------------------------------------------------

ReadMe-DvD_Translations-Gorby's_Pipeline-revA.txt

This file should be viewed using a mono-spaced font like "Courier".
Use a font size where 79 columns are visible.

Please don't distribute the ROM file in patched form.
Please don't distribute the DvDGorby.IPS file without this file.
Thanks.

-------------------------------------------------------------------------------

                  Gorby's Pipeline - Great Military Operation

                                      AKA

                         GORBY no PIPELINE dai sakusen

                            Original Game by Compile
        Famicom Version Copyright 1991 by Tokuma Shoten Intermedia Inc.

             English Translation Copyright 2007 by DvD Translations
             Patch Version: Rev A    Release Date: January 22, 2007    

                                DvD Translations
                      dvdtranslations.eludevisibility.org

                             Code Editing by: DvD 
                             Tile Editing by: DvD
                             Translation  by: harmony7 & DvD
                             ReadMe       by: DvD

----------------------------------- CONTENTS ----------------------------------

THE MANUAL

(1)  Game Description
(2)  Controls
(3)  Helpful Hints

USING THE PATCH

(4)  Patching the ROM file
(5)  Playing the game on an emulator

TRANSLATION DETAILS

(6)  Why DvD chose to translate THIS game
(7)  Why YOU should bother playing THIS game
(8)  DvD's Hacking Comments
(9)  Project Timeline
(10) Software Used In This Translation

---------------------------------- THE MANUAL ---------------------------------

(1)---------------------------- Game Description ------------------------------

Mikhail Gorbachev, born March 2, 1931, was the last leader of the Soviet Union,
serving from 1985 until its collapse in 1991.  This game makes a joke that his
master plan is actually to take over Japan and that he is going to do this by
running a big oil pipeline from his oil fields in Russia to Japan.

The goal of the game is to complete a certain number of pipes from the blue
liquid on the right side of the screen to the empty pipes on left.  Some stages
have less empty pipes and some have less water pipes from the right.  Each
level contains 9 stages.  Each stage goes faster than the previous stage until
you finish the level.  In level 1 you have to make 2 pipes.  In level 2, you
have to make 3 pipes.

Two Russian children are the people who are building the pipeline.  To make the
pipes, you use tiles made out of groups of 2 pipe segments that the boy drops
from the top.  The segments contain straight pipe segments and 90 degree angle
pipe segments

(2)-------------------------------- Controls ----------------------------------

Up, Down, Left, Right - Choose level to start at, you always start on stage 1

Left, Right           - Move Tile Left, Right

Down                  - Move Tile Down much faster than normal

A                     - Rotate Tile Clockwise
                        Continue the game after viewing the map
                     
B                     - Rotate Tile Counter-Clockwise

Start                 - Start the game at the chosen level
                        Pause the game

Select                - not used

(3)----------------------------- Helpful Hints --------------------------------

* There are three special object that drop that are not pipes.

 GOOD) Water Droplet - Drop on the open end of a vertical pipe that has water
       (Blue)          in it and make an entire pipe!  If instead the pipe is
                       horizontal, then it needs to hit the ground right next
                       to the open end of the pipe.

   OK) Drill         - Drills a single tile wide hole straight down through
       (Grey)          all your pipes.

  BAD) Water Bottle  - Works the same at the Water Droplet except that instead
       (Blue)          of making a pipe, 4 rows of non-pipe tiles are inserted 
                       below your existing pipe tiles!  Yikes!

* Try to make your pipes as close to the bottom as possible.

------------------------------- USING THE PATCH -------------------------------

(4)------------------------- Patching the ROM file ----------------------------

Original game ROM size: 2 16k program ROM banks
                          &
                        4  8k character ROM bank
                      = 64 kBytes
                      = 65536 Bytes

Games designed for the original Famicom/NES hardware could be 1 or 2 16k
program banks and 1 8k character bank.  Later, all games made for the NES used
special mapper chips to expand the size of the addressable ROM beyond these
limitations.  This game uses a simple mapper chip to switch between 4 different
static character ROM banks.  One of these banks is used exclusively for the
graphics on the title screen.

How to patch the ROM file:

You need:

1) A ROM file.  The file needs to include the standard 16 byte iNES header
   followed by the program ROM.  With header, the ROM file is 65552 bytes in
   size.

   The header should be as follows:

               4E 45 53 1A  02 04 30 00  00 00 00 00  00 00 00 00

   I'm not telling you how to get the ROM file, but once you do, call it
   Gorby.nes.

3) Patch File: DvDGorby.IPS

4) An IPS patching program
   Remember to patch the file only after it has been expanded.

   Recommended patching program for IBM PC:

    Snes-Tool.exe by The M.C.A./Elite

   Recommended patching program for Mac:

    UIPS

   Using SNES Tool:

   a) If you haven't already, make a copy of the un-patched ROM.
      You always want to keep the un-patched ROM around for later
      revisions of the patch.
   b) Place an un-patched but expanded ROM file
      (I'll call it Gorby.nes), DvDGorby.IPS, and
      Snes-Tool.exe in the same directory.
   c) Run Snes-Tool.exe
   d) Type 'U' for "Use IPS"
   e) Press the down arrow key until DVDGORBY.IPS
      is highlighted.
   f) Hit Enter.
   g) Press the down arrow key until GORBY.NES is highlighted.
   h) Hit Enter.
   i) Hit 'Q' to quit.

(5)-------------------- Playing the game on an emulator -----------------------

Almost all emulators can play the original ROM file.

All emulators that can play the original ROM file can play the translation.

----------------------------- TRANSLATION DETAILS -----------------------------

(6)------------------ Why DvD chose to translate THIS game --------------------

I decided to translate this game because I really like Compile's Dr. Robotnik's
Mean Bean Machine on the Sega Genesis.  It is my favorite Tetris clone game.

I later found out that DRMBM is simply the English release of Puyo Puyo for the
Japanese Sega Megadrive.  Puyo Puyo was originally released for the MSX and
then ported to the Famicom and a number of other systems.  But it was only
released here as Dr. Robotnik's Mean Bean on the Genesis and Kirby's Avalanche
on the SNES, which are essentially the same game with different graphics and
music.

I looked up all the Compile releases for the Famicom and noticed this game
which was never released in the U.S. for any platform!  It had a funny theme so
I thought that I would give it a try.

Hacking the title screen proved challenging and allowed me to be artistic
with the pipes spelling Pipeline.

(7)---------------- Why YOU should bother playing THIS game -------------------

It's the puzzle game Compile made before they made Puyo Puyo, the greatest
Tetris clone of all time!

Sega's Sonic Team who purchased the license from Compile still makes sequels
of Puyo Puyo to this day for all platforms.

It's easy to learn but tough to master!

Still, Gorby's Pipeline is not as fun as Puyo Puyo.  It is a well made Tetris
clone that definitely shares a number of things with Puyo Puyo.  It has two
segment rotate-able tiles and things that drop to help you when you are doing
poorly.  If you generally like Tetris clone games you might really like this
game.


(8)----------------------------- DvD's Comments -------------------------------

Hacking the title screen was much more complicated than it looks.

First off, the NES didn't have enough tiles to do the title screen with just
background graphics, so random areas of the title have sprites interspersed
with background only graphics.  Gorby's, Pipeline, and the subtitle are all
made with both sprites and background graphics.  Fortunately, I was just able
to fit
the English title in, isn't that how it always is?

Second, the original ROM actually messed up where it positioned some of the
sprites.  After analyzing the code I am convinced that this is NOT a problem
with the dump, but a problem with the original ROM due to the number of places
it needed to be fixed.  I decided to (had to) clean it up before I could go on
with the English title, and so I offer a screen shot of on my site of what the
original title screen should have looked like so you can see this for yourself.

The subtitle went through 2 changes...

I was originally going to put "DvD Translations" as the subtitle as the
subtitle didn't really seem to add to the title to me.  But, this
seemed like it would come off as a little too vain.  So, I decided to hack the
credits screen to put it there, it turned out that once I found the code, the
credits screen was really easy hack and I'm glad I went this way.
Second, I was going with "Great Strategy" as "Big Military Campaign" didn't
sound right.

Lastly, harmony7 put me on the right track, suggesting that the subtitle was
supposed to be taken as a joke, that what sounded best was "Bit Military
Campaign" meaning that Gorbachev's great plan was to invade Japan by running
a big oil pipe from Moscow to Tokyo.

(9)---------------------- Project Timeline Highlights -------------------------

Dec 31 2006 - Original Title Screen Errors Fixed
Jan  1 2007 - English Title on Title Screen Completed
              Credits Screen Edited
Jan 16 2007 - Subtitle Changed
Jan 22 2007 - Patch Released
Jan 23 2007 - ReadMe Spell-Checked

(10)------------------ Software Used In This Translation ----------------------

* Emulators

  PC
   - FCE Ultra 0.94          (debugger)
      by Bero & xodnizel
   - Nesticle                (used to isolate sprites from background)

* Tile Editor
  
  Tile Layer Pro 1.0
   by Kent Hansen

* Disassembler, Table Dumper

  Table Dumper 6.12.23
   by DvD

* Hex Editors, Script Dumper

  - Thingy Version 0.98
     by necrosaro

* Disassembled Code And Table Analysis

  WordPad (Win XP)
   by Microsoft

* Manual Creation

  Notepad (Win XP)
   by Microsoft

* IPS Patch File Creator

  Snes-Tool Version 1.2
   by The M.C.A./Elite

-------------------------------------------------------------------------------
987654321098765432109876543210987654321 123456789012345678901234567890123456789
