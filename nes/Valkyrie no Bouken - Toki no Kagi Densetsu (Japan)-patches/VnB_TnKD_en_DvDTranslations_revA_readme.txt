-------------------------------------------------------------------------------

ReadMe-DvD_Translations-Valkyrie_s_Adventure-Legend_of_the_Time_Key-revA.txt

This file should be viewed using a mono-spaced font like "Courier".
Use a font size where 79 columns are visible.

Please don't distribute the ROM file in patched form.
Please don't distribute the DvD_VAL.IPS file without this file.
Thanks.

-------------------------------------------------------------------------------
                              VALKYRIE'S ADVENTURE
                             Legend of the Time Key

                                      AKA

                               VALKYRIE NO BOUKEN
                             Toki no Kagi Densetsu

                       for the Nintendo Family Computer
                            Copyright 1986 by Namco

             English Translation Copyright 2009 by DvD Translations
             Patch Version: Rev A   Release Date: February 23, 2009    

                                DvD Translations
                      dvdtranslations.eludevisibility.org

                   Code & Graphics Editing by: DvD
                               Translation by: harmony7 & DvD

                              Text Editing by: DvD
                              Beta Testing by: DvD & harmony7
                                    ReadMe by: DvD

----------------------------------- CONTENTS ----------------------------------

THE MANUAL

(1)  Valkyrie Game Series
(2)  Game Description & Controls
(3)  Advice, Hints & Spoilers

USING THE PATCH

(4)  Patching the ROM file
(5)  Playing the game on an emulator

TRANSLATION DETAILS

(6)  Why DvD chose to translate THIS game
(7)  Why YOU should bother playing THIS game
(8)  DvD's Hacking Comments
(9)  harmony7's Translation Comments
(10) Project Timeline
(11) Software Used In This Translation

---------------------------------- THE MANUAL ---------------------------------

(1)-------------------------- Valkyrie Game Series ----------------------------

The Valkyrie series consists of the following 4 games:

Valkyrie no Bouken: Toki no Kagi Densetsu    - Famicom       - August  1, 1986
Valkyrie no Densetsu                         - PC Engine     - August  9, 1990
Sandra no Daibouken: Valkyrie to no Deai     - Super Famicom - July   23, 1992
Valkyrie no Densetsu Gaiden - Rosa no Bouken - Windows 3.1   - April  26, 1996

None of these were released in North America.
Both Valkyrie no Bouken and Valkyrie no Densetsu have been rereleased in Japan
for the Wii's Virtual Console.
Valkyrie no Densetsu was a port of the arcade game of the same name.
Sandra no Daibouken was released in Europe as Whirlo.
Valkyrie no Densetsu Gaiden is a "digital comic".

(2)---------------------- Game Description & Controls -------------------------

This game has been released on the Wii Virtual Console in Japan.
Check out this link to the manual in Japanese:

http://www.nintendo.co.jp/wii/vc/vc_val/vc_val_01.html

The best thing here is the map that originally game with the game.

The Strategy Wiki site is essentially a manual for the game:

http://strategywiki.org/wiki/Valkyrie_no_Bouken:_Toki_no_Kagi_Densetsu

It tells the plot and lists all items and magic.  Also, it explains how the
Sun Sign and Blood Type you choose affect the development of the Valkyrie.
Watch out for spoilers though, because in the items list it also lists where
they can be found in the game.  Again, if you compare this with the Wii
manual, you can see that only SOME of the items should be explain in the
manual, but all of the magic should be explained.

I really recommend reading them both, but here is the controls list:

Start                 - Start Game
Select                - Choose Start or Continue
Start or Select       - Pause Game (Items & Magic selection mode) / Un-Pause
A                     - Use selected Magic
                      - Teleport from one "Warp Zone" to another
                        based on which direction the Valkyrie is facing
B                     - When not paused: Use selected Item
                      - When paused: Equip Equipable Item/Use Consumeable Item
Control Pad           - When not paused: Move the Valkyrie
                      - When paused (left/right): Select Item
                      - When paused (up/down): Select Magic

(3)------------------------ Advice, Hints & Spoilers --------------------------

Advice:

One important thing to know about the game isn't really discussed in the
Strategy Wiki site at all.  You will die in this game... A LOT.  When you do,
you will only keep the items in your inventory when you continue.  You will
not stay equipped with the items that leave your inventory when you equip them.
So, the correct way to play is to collect the items you want to have AFTER you
die, then visit the Inn.  Now, when you die, although you will lose anything
you've done since you visited the Inn, you will have all the items that were in
your inventory when you last visited the Inn.  When you continue, you can equip
the items in your inventory AND ALL the items you found will be replaced, so
you can get them again.

Hints:

The one hint that is only given in walkthroughs that you need to pass the
game:  you NEED a to have a Sandra Soul in your inventory to pass the game. 
This was never explained in the Japanese manual, and hence many Japanese never
passed the game because of this.  There really is no obvious reason to carry it
at that point, especially since you have such a limited inventory.  The other
hint you really need has been re-inserted in the game since it was in the ROM
but, for some reason, not actually in the Japanese version of the game.

Look at my screenshots for a hint as to what items you need to pass the game...

Spoiler:

As long as you find the healing coin and have the best equipment equipped,
the final boss is not hard, you just have to kill him a random number of times.
So, it's just a matter of luck whether you kill him enough times, or die before
the all important random event happens and have to start again.  Fortunately,
it doesn't take TOO long to try again.

------------------------------- USING THE PATCH -------------------------------

(4)------------------------- Patching the ROM file ----------------------------

Game ROM size: 2 16k program   ROM banks
                          &
               4  8k character ROM bank
              = 64kBytes
           = 65536 Bytes

Games designed for the original Famicom/NES hardware have one or two 16k
program banks and one 8k character bank.  Later, all games made for the NES
used special mapper chips to expand the size of the addressable ROM beyond
these limitations.  This game does not expand the program ROM but it
uses a mapper chip that expands the character ROM and allows it to swap 4k
blocks in and out.  The mapper number is 206.  It work in the same way that
the later developed more sophisticated mapper MMC3 works, and thus you can use
mapper 4, MMC3 to run the game in emulators that do not support mapper 206.

How to patch the ROM file:

You need:

1) A ROM file.  The file needs to include the standard 16 byte iNES header
   followed by the program ROM.  With header, the ROM file is 65552 bytes in
   size.

   The header should be as follows:

       4E 45 53 1A  02 04 E0 C0  00 00 00 00  00 00 00 00 (Mapper 206)
       or
       4E 45 53 1A  02 04 40 00  00 00 00 00  00 00 00 00 (Mapper 4:MMC3)

   The IPS file does NOT change the header, so it will not change the mapper.

   I'm not telling you how to get the ROM file, but once you do, call it
   Valkyrie.nes.

3) Patch File: DvD_VAL.IPS

4) An IPS patching program

   Recommended patching program for IBM PC:

    Snes-Tool.exe by The M.C.A./Elite

   Recommended patching program for Mac:

    UIPS

   Using SNES Tool:

   a) If you haven't already, make a copy of the un-patched ROM.
      You always want to keep the un-patched ROM around for later
      revisions of the patch.
   b) Place an un-patched but expanded ROM file
      (I'll call it Valkyrie.nes), DvD_VAL.IPS, and
      Snes-Tool.exe in the same directory.
   c) Run Snes-Tool.exe
   d) Press 'U' for "Use IPS"
   e) Press the down arrow key until DvD_VAL.IPS is highlighted.
   f) Press Enter.
   g) Press the down arrow key until VALKYRIE.NES is highlighted.
   h) Press Enter.
   i) Press 'Q' to quit.

(5)-------------------- Playing the game on an emulator -----------------------

All emulators that can play the original ROM file can play the translation.
No expansion or mapper changes were done and it can be made to use the very
commonly supported MMC3.

Actually, it should RUN in all emulators, since the mapper doesn't expand the
program code at all, but if the graphics don't switch correctly, it will be a
big mess.

It will run in almost all emulators, but I recommend FCEUX as the most
recently updated version of the FCE Ultra line.  It handles both mappers
correctly.

----------------------------- TRANSLATION DETAILS -----------------------------

(6)------------------ Why DvD chose to translate THIS game --------------------

This is one of the classic games that introduced the genre of action RPG on
the Famicom.  It came after Zelda 1 for the Famicom Disk System, the Famicom
port of Hydlide, and even the first Famicom RPG, Dragon Quest, but before
anything else as far as I can tell.

I was introduced to the game because another group, Some Good S__t
Translations, had translated it.  Some things were translated really well.
But as I played their translation, I was really bothered by the mistranslated
title screen, and the start popup.  Plus, I read on the strategy wiki site
that, although the ending was in English, the translation messed it up.

So, I felt this important game in the history of games deserved a better
translation.  

(7)---------------- Why YOU should bother playing THIS game -------------------

Overall the game is okay.  I preferred Hydlide, but this game is not too bad,
as long as you read how to play it on the Strategy Wiki site, make maps
of the underworld, and contrary to the only FAQ on GameFAQs, cast True Sight
everywhere to find the best items in the game.

The worst thing about it?  It takes WAY to long to level up.  I reccomend a
Water Sign with Type O (or AB if you want to cheat and manipulate your luck on
what you get).

(8)------------------------- DvD's Hacking Comments ---------------------------

As it turns out, there were other things that the previous translators forgot
to translate, such as the Danger sign.  This was the final issue that pushed me
to translate it myself.  It was in kanji, which I can't read!  I really wanted
to know what the sign meant!

When I checked the ROM there were 2 more signs with text that were not
translated.  It turns out, though, that they were never used in the game.  For
some reason even though the original author's wrote them, they were removed
before release.  The final hacking I did was to put these both back in the
game.  One of these gives a key hint to passing the game.

This required me to use Table Dumper to disassemble the game and figure out the
compression of the over world.  It turns out that the whole game is one map.
The over world is in the north and the underworld on the south, with the shop
and inn between them on the far west edge.

Table Dumper's sophisticated table dumping options were key to discovering
the compression of the game map.  It turns out that the entire map is composed
of:
One                             16 x 40 grid of 32x16 tiles.
Each 32x16 tile is made up of a  8 x  4 grid of  4x4  tiles.
Each  4x4  tile is made up of a  2 x  2 grid of  2x2  tiles.
Each of the 2x2 tiles has its own unique palette.

The title screen was pretty easy to hack and the ending text was very easy
because Namco left lots of free space after each screen's text.

I originally didn't plan on editing the ending text since it was in English.
After reading it many times, harmony7 and I noticed that it was more like
Engrish that really needed to be cleaned up.

The title screen was what I hacked first and it wasn't difficult.  But I had
to be careful; some of the graphics were reused with a different palette in the
ending.

I wanted to play the whole game myself, and I did.  That was the reason I
wanted the game to be correctly translated!  So, for once, no beta testers were
used.

(9)-------------------- harmony7's Translation Comments -----------------------

Another classic game that I've owned for ages.

Being a 10-year old at the time I got the game, I had no chance, so it has
spent the next two decades buried under other game cartridges.  It's probably
still in there somewhere, if I looked.

In this project I translated the few snippets of text that existed throughout
the game, and I also helped fix the bad English that composed the ending.
This was one of my shorter projects because there was very little text.

I don't have much to say about the game itself except that it was definitely a
new type of game at the time.  The difficulty is a bit high and the lack of
hints proves to be a bit annoying from today's standards, but this was a common
trait among many games from the day.

If only the Valkyrie's sword were longer and her wings were on her body instead
of her head, I might have been able to complete the game.

But good luck to all of you who are going to attempt this game.

(10)--------------------- Project Timeline Highlights -------------------------

Jan 17 2009 - Project Started by DvD
Jan 31 2009 - New title screen completed
Feb 10 2009 - Configuration screen completed, Inn & Ending text edited
Feb 21 2009 - Sign added to overworld, Incomplete patch released to harmony7
Feb 22 2009 - Exit sign added to Inn/Shop, Inn text cleaned up,
              Patch completed, testing completed, readme started
Feb 23 2009 - Readme completed, Patch Released

(11)------------------ Software Used In This Translation ----------------------

* Emulators

  FCEUX 2.0.3
      If you like FCE Ultra, or FCEUXD SP, you'll love FCEUX.
      This version came out in Nov 2008.
      Thank you RadicalR for pointing this one out.
      It is the emulator that I will be using from now on; it's awesome.

* Tile Editor
  
  Tile Layer Pro 1.0
   by Kent Hansen

* Disassembler, Table Dumper, File Comparator

  Table Dumper Pro (ver 8.6.7)
   by DvD

* Hex Editors

  WindHex32 2005.4.20
   by Genecyst East Software (Finally, I'm done with THINGY!)
  FCEUX 2.0.3

* Readme Creation

  Notepad (Windows XP)
   by Microsoft

* IPS Patch File Creator

  Snes-Tool Version 1.2
   by The M.C.A./Elite

-------------------------------------------------------------------------------
987654321098765432109876543210987654321 123456789012345678901234567890123456789
