-------------------------------------------------------------------------------

ReadMe-DvD_Translations-TwinBee_2.txt

This file should be viewed using a mono-spaced font like "Courier".
Use a font size where 79 columns are visible.

Please don't distribute the ROM file in patched form.
Please don't distribute the DvD_TwinBee_2_revA.ips file without this file.
Thanks.

-------------------------------------------------------------------------------
                                BURNIN' TWINBEE
                          The Rescue of Dr. Cinnamon!

                            for the Nintendo Famicom
                         Copyright 1987/1993 by Konami

             English Translation Copyright 2018 by DvD Translations
             Patch Version: Rev A      Release Date: April ??, 2018

                                DvD Translations
                      dvdtranslations.eludevisibility.org

                                      GAME

                            Translation: aishsha
                         Script Editing: DvD
                           Code Editing: DvD
                       Graphics Editing: DvD
                          Alpha Testing: DvD
                           Beta Testing: KlD, 1AM, R1D2

                                 ReadMe: DvD

----------------------------------- CONTENTS ----------------------------------

INFO 

(1)  TwinBee Game Series
(2)  If You Read Anything, Read This
(3)  How to Get the Most Out of TwinBee 1

USING THE PATCH

(4)  Patching the ROM File
(5)  Playing the Game on a Flash Cart or Emulator

TRANSLATION DETAILS

(6)  Why DvD Chose to Translate THIS Game
(7)  Why YOU Should Bother Playing THIS Game
(8)  DvD's Hacking & Script Editing Comments
(9)  1AM's Beta Testing Comments
(10) R1D2's Beta Testing Comments
(11) Project Timeline
(12) Software Used In This Translation

------------------------------------- INFO ------------------------------------

(1)-------------------------- TwinBee Game Series -----------------------------


TwinBee is a huge series of games by Konami.
The first, simply titled "TwinBee", was released for the arcade on March 5,
  1985.  "TwinBee" was ported to the Famicom in Japan on January 4, 1986.
The second game was released released soon after as "Moero TwinBee:
  Cinnamon-hakase o Sukue!" on November 21, 1986 for the Famicom Disk System.
  Konami ported it to the US NES releasing it as "Stinger" in September of
  1987.  Unfortunately, they completely removed the 3rd player and both Bee
  cut-scenes.
Konami released "TwinBee 3: Poko Poko Dai Maou" for the Famicom on September
  29, 1989.
Konami released the fourth game in the series, "Pop'n TwinBee" for the Super
  Famicom on March 26, 1993 which they quickly localized in Europe for the
  Super NES.
On the very same day, Konami finally released "Moero TwinBee: Cinnamon-hakase o
  Sukue!" for the Famicom restoring all the content that was changed or removed
  for the US release and adding a difficulty selection.  Because of the late
  release, this is a relatively rare and expensive game.
Many other TwinBee games have since been released plus many games in the
  excellent "Parodius" series and "Wai Wai Racing" where a TwinBee always plays
  a major role as a playable character in every game.

(2)-------------------- If You Read Anything, Read This -----------------------

For this game, DvD Translations has released scans of some of the pages of the
FDS version of the manual.  They are available from our website on the web page
where this patch was found.  The manual pages included show the story, bells,
power-ups, enemies for two levels, and stage bosses.

The main reason we re-translated this game is that the 3rd player was not
supported in Stinger and every other translation did not correct the 3rd player
so that it actually worked on a real NES with a 4-Score or NES Sattelite.
Playing with 3 players at the same time is a blast and the only thing that
makes this game standout amongst other TwinBee games.

Don't buy repro carts!  They are expensive.  They don't support bug fixes for
patches because they can't be modified in the future.  If they aren't built
from scratch they destroy a real cart.  Every time a donor cart is used to make
a repro, it raises the scarcity and price of that real cart.  If you must buy a
real cart, buy one from a vendor who only makes carts from scratch with new
boards, chips, and housings.

(3)------------------ How to Get the Most Out of TwinBee 1 --------------------

The original TwinBee Famicom game uses mapper 87 simply to do a graphics swap
for stages 4 and 5.  It does nothing to the code.  Most ROMs of the game have
it set to the wrong mapper.  Thus, the graphics for the 4th and 5th levels
don't get swapped in when they are supposed to and so the levels look scrambled
as they use the tiles for the first 3 levels.  For some reason, many emulators
do not correctly support mapper 87, but the PowerPak handles it perfectly.

TwinBee has two built in cheat codes.

The first gives two players 5 lives each instead of 3:
- At the title screen, start a "2 Players" game.
- While on the black screen with "Today's Score", on controller 2,
  hold B and press Up, Down, Left, Right all at least once in any order
  before the screen changes.

The second gives a single player 10 lives, instead of 3:
- At the title screen, start a "1 Player" game.
- While on the black screen with  "Today's Score", on controller 1,
  hold A, Up, and Right all at the same time before the screen changes.

Unfortunately, there is no way to tell if you entered the cheat code in
correctly until you die enough times or pass stage 1 because the game always
states that you only have 3 lives left when you start stage 1.  To cure this,
DvD created two game genie codes that automatically enter the cheat codes.  And
for those who still can't pass the game with 10 lives here's a 30 lives cheat
like the Contra Konami code.

2 player,  5 lives each: TAGATX
1 player, 10 lives     : LZGAAX
1 payer,  30 lives     : TPTEIX (To have the code automatically entered,
                                 you must enter the 10 lives code as well)
					   
------------------------------- USING THE PATCH -------------------------------

(4)------------------------- Patching the ROM File ----------------------------

How to patch the ROM file:

You need:

1) A NES file.  The file needs to include the standard 16 byte iNES header
   followed by the program disk image data.  With header, the ROM file is
   135,168 bytes in size.

   The header should be as follows:

       4E 45 53 1A  08 00 21 00  00 00 00 00  00 00 00 00

   You must have a 16 byte header for this patch, but even if your header
   is wrong, this patch will fix it because it replaces the whole thing.  So,
   if you have a file without a header, you can just insert 16 of any byte at
   the start of the file.
   
   I'm not telling you how to get the NES file, but once you do, call it
   "Burnin' TwinBee - The Rescue of Dr Cinnamon!.nes".

3) Patch File: DvD_TwinBee_2_revA.ips

4) An IPS patching program
   Remember to patch the file only AFTER it has a header.

   Recommended IPS patching program for IBM PC:  Lunar IPS.exe by FuSoYa
   Recommended IPS patching program for Mac:     UIPS          by Lucas Newman
   
   Using Lunar IPS / UIPS:

   a) Double-click "Lunar IPS" / "UIPS"
   b) Click  "Apply IPS Patch" / "Apply Patch"
   c) Choose "DvD_TwinBee_2_revA.ips"
   e) Choose "Burnin' TwinBee - The Rescue of Dr Cinnamon!.nes"
   
(5)------------- Playing the Game on a Flash Cart or Emulator ----------------

All emulators and flash carts that can play the original Famicom file can play
the translation.  The 3rd player is supported by NES 4-Score or NES Sattelite
emulation and, thus, is not supported by Famicom 3rd player emulation.

The PowerPak flash cart emulates it perfectly.

Games designed for the original Famicom/NES hardware have one or two 16k
program banks and one 8k character bank.  Later, all games made for the NES
used special mapper chips to expand the size of the addressable ROM beyond
these limitations.  Some even included RAM for the character bank,
instead of ROM.  This is one of those games.

Game file size: 8 x 16 kBytes of Program   ROM
                0 x  8 kBytes of Character ROM
                   128 kBytes
             = 131,072  Bytes
             +      16  Byte Header
             = 131,088  Bytes

This game uses mapper 2, known as UNROM, which is a very common mapper.  The
mapper simply swaps one of the program banks and uses 8k of RAM for character
memory.  This was done because the original game was made for an FDS which
is RAM for both the Program and Character banks.  Because the Character banks
are RAM, the graphics are stored compressed in the Program ROM.

----------------------------- TRANSLATION DETAILS -----------------------------

(6)------------------ Why DvD Chose to Translate THIS Game --------------------

The main reason I wanted to work on this game is that the 3rd player was not
supported in Stinger and every other translation did not correct the 3rd player
so that it actually worked on a real NES with a 4-Score or NES Satellite.

Playing with 3 players at the same time is a blast and the only thing that
makes this game standout amongst other TwinBee games.  I personally think this
is the best multi-player NES game ever made.

(7)---------------- Why YOU Should Bother Playing THIS Game -------------------

If you have a NES Satellite or 4-Score and at least 3 controllers, you will
finally have a new game you can play with them.  Playing a Konami shooter on a
real NES with 3 simultaneous players is really fun.  Invest in a flash-cart and
play this an many other awesome translations.

(8)---------------- DvD's Hacking & Script Editing Comments -------------------

I've been on a kick to play the games on which Parodius and Wai Wai Racing are
based on.  I had played TwinBee, but not Stinger.  When I saw that the original
Japanese game had three players, I was excited to play with the 3rd player, but
when I found that the Famicom 3rd player wasn't supported by my NES Satellite,
I knew I had to figure out what needed to be changed.  Really, it was an easy
fix.  But, then, what to do, release it as a hack, add my hack to another
existing translation, or release my own translation?  First, I worked on the
things that hadn't been done in the other translations, the BoooM! sprites and
compressed graphics and layout of the title screen.  To do the compressed
Graphics I edited Table Dumper Pro's Romancia compressed graphics inserter to
be something more generic.  After I completed that, I realized with all the
work I put into it I might as well release my own translation.

(9)---------------------- 1AM's Beta Testing Comments -------------------------

I played the game with R1D2 and DvD using an NES Satellite and a PowerPower
pack.  It's too bad that the NES can't handle more than 8 sprites in a row as
it makes the BoooM! look bad.  As the 3rd player, the game was nice but it was
hard since R1D2 kept shooting all the good bells.  It thought stage 13 was
especially tough, even on easy.  Be careful, don't press any buttons during the
ending or you wont get to see what the Bees are saying!  Remember to read the
Dr.'s speech quickly as it will fade away before you read it if you read too
slow...

(10)--------------------- R1D2's Beta Testing Comments ------------------------

It wasn't fun losing every single time.  I guess I need to practice more. 

(11)---------------------- Project Timeline Highlights ------------------------

Mar 15 2018 - Project started

Mar 17 2018 - Reverse engineered Bomberman II to confirm how 3rd player works
              on a NES
            - Added 3rd player support to TwinBee 2
		- Alpha tested 3rd player support on a NES Satellite with 1AM and
		  R1D2

Mar 20 2018 - BoooM! sprites first inserted
            - Intro font inserted

Mar 25 2018 - Bee intro text inserted
            - Table Dumper Pro modified to insert compressed title screen
		  graphics
            - New title screen completed

Apr  3 2018 - Bee ending text inserted

Apr  4 2018 - ReadMe and Website Created

Apr  8 2018 - Dr. Cinnamon Ending Speech and Credits Added
              Credit new credits font added and credits modified
		  BoooM! sprites modified to match original colors
              Beta testing by KlD performed / Text edited
		  Final ROM comparison performed and any unused changes removed
		  
Apr  9 2018 - Comments received from contributors
            - ROM translation released along with Cleopatra
            - Website released

(12)------------- Software & Hardware Used In This Translation ----------------

* Emulator

  FCEUX 2.2.2 & 2.2.3
* Disassembler, Table Dumper, Text/Compressed Graphics Inserter

  Table Dumper Pro (ver 18.03.25)
   by DvD

* Hex Editor

  Beyond Compare 4
   by Scooter Software

* Tile Editors
  
  Tile Layer Pro 1.0
   by Kent Hansen
  
* Disassembled code manipulation, script editing, ReadMe creation, &
   ROM Expander Pro file editing

  Notepad++
   by Don Ho and the rest of the Notepad++ team

* Graphics Editing

  PaintShop Pro
   
* Project management

  OpenOffice 4 Calc
    by Apache

* IPS Patch File Creator

   Lunar IPS
    by FuSoYa

-------------------------------------------------------------------------------
987654321098765432109876543210987654321 123456789012345678901234567890123456789