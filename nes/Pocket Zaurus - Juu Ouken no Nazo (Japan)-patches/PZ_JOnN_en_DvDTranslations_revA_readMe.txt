-------------------------------------------------------------------------------

ReadMe-DvD_Translations-Pocket_Zaurus.txt

This file should be viewed using a mono-spaced font like "Courier".
Use a font size where 79 columns are visible.

Please don't distribute the ROM file in patched form.
Please don't distribute the DvD_PocketZaurus_revA.ips file without this file.
Thanks.

-------------------------------------------------------------------------------
                                 POCKET ZAURUS
                            Swords of the Ten Kings

                                for the Famicom
                            Copyright 1987 by Bandai

             English Translation Copyright 2015 by DvD Translations
             Patch Version: Rev A        Release Date: May 25, 2015

                                DvD Translations
                      dvdtranslations.eludevisibility.org

                                      GAME

                     Script Translation: geishaboy, harmony7
                         Script Editing: harmony7, DvD
                           Code Editing: DvD
                       Graphics Editing: DvD
                     Production Support: Pennywise 
                          Alpha Testing: DvD
                           Beta Testing: Lord Oddeye, Radical R
                                 ReadMe: DvD

                                     MANUAL

  Manual, box, & toy scans collected by: DvD, harmony7
                     Manual Translation: geishaboy, harmony7, Google, DvD
           Graphic Editing & Formatting: DvD

----------------------------------- CONTENTS ----------------------------------

INFO 

(1)  Pocket Zaurus Game Series
(2)  If You Read Anything, Read This

USING THE PATCH

(3)  Patching the ROM File
(4)  Playing the Game on a Flash Cart or Emulator

TRANSLATION DETAILS

(5)  Why DvD Chose to Translate THIS Game
(6)  Why YOU Should Bother Playing THIS Game
(7)  DvD's Hacking & Script Editing Comments
(8)  harmony7's Translating Comments
(9)  Lord Oddeye's Beta Testing Comments
(10) Project Timeline
(11) Software Used In This Translation

------------------------------------- INFO ------------------------------------

(1)----------------------- Pocket Zaurus Game Series --------------------------

This is the only Pocket Zaurus game ever made!

(2)-------------------- If You Read Anything, Read This -----------------------

For this game, DvD Translations has attempted to fully translate an html
version of the manual.  Although it wasn't completed, a lot of it has been
translated.  Please read it before playing the game.  It's available from our
website on the web page where this was found.

This platformer is based on Bandai's line of pocketzaurus stationary product
robotic dinosaur toys.  The toys were also released in France and Germany as
Diplodos.  In cooperation with Bandai, a French/Japanese Diplodos animation
series was made, which was then translated into English.  Our web page for the
game contains a large number of scans and details of this.

The game calls itself a "Quiz Adventure" and it is quite unique; you will need
to do a number of things to pass the game without cheating:
* You'll want to have a fully translated manual. The manual contains crossword
  puzzles, one for each level.  If you answer a whole puzzle, which has clues
  based on things in the game, it gives a clue as to what to do to defeat the
  final boss.
* When you play the game, it gives you in-game quizzes that, if you get them
  right, give you bonuses.
* When you beat the optional mini-bosses in each level, the game gives you a
  clue that allows you to get a clue from that level's boss.  If collect all
  the clues from the level bosses it will tell you what you need to do to
  defeat the final boss.
* Whenever you die without having a Continue Mark, you will be given the option
  to face the final boss.  You can do this to practice fighting the final boss,
  but you'll never win unless you've defeated all the level bosses.

------------------------------- USING THE PATCH -------------------------------

(3)------------------------- Patching the ROM File ----------------------------

How to patch the ROM file:

You need:

1) A NES file.  The file needs to include the standard 16 byte iNES header
   followed by the program disk image data.  With header, the ROM file is
   262160 bytes in size.

   The header should be as follows:

       4E 45 53 1A  08 10 80 90  00 00 00 00  00 00 00 00

   You must have a 16 byte header for this patch, but even if your header
   is wrong, this patch will fix it because it replaces the whole thing.  So,
   if you have a file without a header, you can just insert 16 of any byte at
   the start of the file.
   
   I'm not telling you how to get the NES file, but once you do, call it
   "Juu Ouken no Nazo - Pocket Zaurus.nes".

3) Patch File: DvD_PocketZaurus_revA.ips

4) An IPS patching program
   Remember to patch the file only AFTER it has a header.

   Recommended IPS patching program for IBM PC:  Lunar IPS.exe by FuSoYa
   Recommended IPS patching program for Mac:     UIPS          by Lucas Newman
   
   Using Lunar IPS / UIPS:

   a) Double-click "Lunar IPS" / "UIPS"
   b) Click  "Apply IPS Patch" / "Apply Patch"
   c) Choose "DvD_PocketZaurus_revA.ips"
   e) Choose "Juu Ouken no Nazo - Pocket Zaurus.nes"
   
(4)------------- Playing the Game on a Flash Cart or Emulator ----------------

Games designed for the original Famicom/NES hardware have one or two 16k
program banks and one 8k character bank.  Later, all games made for the NES
used special mapper chips to expand the size of the addressable ROM beyond
these limitations.  Some even included RAM for the character bank,
instead of ROM.

Game file size: 8 x 16 kBytes of Program   ROM
                16 x 8 kBytes of Character ROM
                256 kBytes Bytes
		  = 262144 Bytes
                +   16 Bytes
              = 262160 Bytes

This game uses mapper 152 which is almost the same thing as mapper 70 except
that the mirroring is selectable.  It's a very simple mapper.

Unfortunately, it is not currently supported by the PowerPak flash cart.
Fortunately, it is supported by the EverDrive-N8 flash cart.

It plays fine in FCEUX and Nestopia.

----------------------------- TRANSLATION DETAILS -----------------------------

(5)------------------ Why DvD Chose to Translate THIS Game --------------------

I wanted translate a game that harmony7 wanted to see translated.  He had
played this game as a kid and wanted to see it translated.  Otherwise, I would
have never chosen this game.

(6)---------------- Why YOU Should Bother Playing THIS Game -------------------

Should you bother?  It's a well made but difficult platformer with a lot of
humor.  Play it if that sounds interesting or if you are a fan of pocketzaurus
toys or the Diplodo cartoon.

(7)---------------- DvD's Hacking & Script Editing Comments -------------------

I really wasn't that interested in the game, so I tried to give the project a
boost by asking Pennywise to help manage the game.  That kinda got me
interested.  The game had in-game kanji and a complicated multiple nested
pointer structure.  While figuring them out I completed the initial hack of the
title screen which remained the same until days before the patch was released. 

But then, harmony7 wasn't interested in working on the script.  Pennywise found
geishaboy, who translated the script.

The text for this game always consists of 3 lines, each with their own pointer.
To fit the English text, I modified the code so that it displays each of these
lines as a double line.  I modified Table Dumper to handle multiple pointers to
the same block of text so I could efficiently insert the script.

Once our first incomplete script was inserted and he was presented with a
script with parts he didn't approve of, harmony7 was much more interested in
editing the script.  While this was going on, I coded up my first DTE using
ScriptCrunch.  This went great and the whole script fit without the need for
expansion.

Then the hard part started: trying to view every line in the game.  Finding
all the text in the game was easy.  It was all listed in one block, called by
list in a second block, which itself was called by a third list.  It was
calling this third block that is done in a ton of different ways.

It turns out that many times the search was futile because there is also a lot
of unused text.  Proving that everything I thought was unused was actually
unused, or finding where it was actually called from took a very long time.  In
the end I still can't be 100.00% sure that all the text I believe is unused is
actually unused.  This really bothers me, but I don't want to search forever
for something the probably doesn't exist.  Beta testing did not find any text
that I hadn't found, so it's unlikely that anyone else will.

I also spent a lot of time trying to clean up what I had received as the
translation of the manual.

I released the title screen in hopes that someone would help finish the
manual's translation.

Once I decided that I had waited long enough, I had to wait some more time
until I had some free time to work on completing the project and working on
my next project.  While searching the net for scans of the back of the box, I
discovered that pocketzaurus are actually toys!  I also got a high-res scan of
the box that showed the official English pocketzaurus logo matched the logo on
the toys.  I really liked the English logo I decided it must go into the game.
So, I hacked it in, modifying the title screen which had remained the same for
4 1/2 years.

Even though the logo is written as a single lower case word "pocketzaurus"
harmony7 decided to keep it as two separate mixed case words in the game for
a number of reasons.  One obvious one is that the title screen originally
showed it as two separate words in English, POCKET ZAURUS.  The second was
that, although it looked good in the logo, "Pocketzaurus" or "pocketzaurus"
just didn't look as good in the game.

In the end, my favorite part was finding all the pocketzaurus toys and how
they are represented in the game and hacking in the new official logo.  Finding
this logo, like the King Kong Lives logo before, made me glad I had waited so
long to finish the project.

(8)-------------------- harmony7's Translating Comments -----------------------

I received this game originally as a gift back in 1988, when I was but a third
grader.  It was incredibly challenging and I gave up on it many times since.

Even so, the game left an impression on me because of the catchy music and
cutesy graphics, as well as the silly jokes scattered throughout.

Translating this game turned out to be simpler than I had originally imagined.
It was simple since much of the text was very short.  Additionally, I was so
familiar with the game that there were not many quotes that I did not
recognize.

This project unfortunately underwent several delays, but I hope it will have
been worth the wait.  Enjoy!

(9)------------------ Lord Oddeye's Beta Testing Comments ---------------------

A light-hearted platformer with a few shooter sections and increasingly 
challenging bosses.  Other than a quirky level order, regular quizzes for
points and semi-hidden screens, there isn't much to comment about.  One thing
of note is that you get to practise fighting the final boss whenever you lose
all your lives.  Defeating it is another story though, as it takes an entire
play-through to obtain the means to set up the kill.  That being said, I
couldn't find a definitive ending to this adventure, which might leave some
players a bit disappointed.  Still, not a bad game at all! It was worth my few
play-throughs trying to find an alternate ending that never came.

(10)---------------------- Project Timeline Highlights ------------------------

Nov 10 2007 - Started translation based on suggestion from harmony7

Nov  4 2010 - Asked Pennywise to help manage the project to help get it done
            - The Title screen hack completed. 
            - The in-game kanji graphics were changed to English. 
            - English font inserted 
            - Kanji font tiles translated and inserted 
            - Complicated multiple nested pointer structure figured out 

Mar 27 2011 - harmony7 has decided he was too busy to work on the script

Apr 26 2011 - Pennywise found geishaboy to translate the game

Jun 17 2011 - Modified the code so that it displays each of line as a double
              line
            - Table Dumper was modified to handle multiple pointers to the
              same block of text
            - First incomplete script was inserted. 

Dec 22 2011 - harmony7 went cleaned up some of the translations of the script
            - DTE font created and now full script inserted 
            - Manual translated, but being edited 
            - Playing game to look for and fix bugs 

Aug  7 2014 - All the text that we are sure is actually used in the game has
              been verified by displaying it in the game
            - RadicalR and Lord Oddeye started beta testing
            - Partially translated manual released

Aug 11 2014 - Title screen shot released 

Apr 28 2015 - Strategy guide, toy, and Diplodo scans added to website
            - Logo on title screen changed to match official English
              pocketzaurus logo
            - IPS patch file completed

May 25 2015 - Comments received from contributors
            - ROM translation released

(11)------------- Software & Hardware Used In This Translation ----------------

* Emulator

  FCEUX 2.1.4a & 2.1.5
   by zeromus, adelikat

* Disassembler, Table Dumper, Script/Items/Menus Inserter, File Comparator

  Table Dumper Pro (ver 12.9.9)
   by DvD

* Hex Editors

  WindHex32 2005.4.20
   by Genecyst East Software

  Frhed 1.7.1
   by Raihan Kibria

* Tile Editors
  
  Tile Layer Pro 1.0
   by Kent Hansen
  
* Disassembled code manipulation, script editing, ReadMe creation, &
   ROM Expander Pro file editing

  Notepad++
   by Don Ho and the rest of the Notepad++ team

* IPS Patch File Creator

   Lunar IPS
    by FuSoYa

-------------------------------------------------------------------------------
987654321098765432109876543210987654321 123456789012345678901234567890123456789