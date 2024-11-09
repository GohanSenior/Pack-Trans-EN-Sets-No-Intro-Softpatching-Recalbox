-------------------------------------------------------------------------------

ReadMe-DvD_Translations-King_Kong_Lives-revA.txt

This file should be viewed using a mono-spaced font like "Courier".
Use a font size where 79 columns are visible.

Please don't distribute the ROM file in patched form.
Please don't distribute the DvD_KKL.IPS file without this file.
Thanks.

-------------------------------------------------------------------------------
                                KING KONG LIVES
                             Megaton Punch of Rage

                                      AKA

                                  KING KONG 2
                             Ikari no Megaton Punch

                            for the Nintendo Famicom 
                            Copyright 1986 by Konami

             English Translation Copyright 2008 by DvD Translations
             Patch Version: Rev A       Release Date: June 9, 2008    

                                DvD Translations
                      dvdtranslations.eludevisibility.org

                            Graphics Editing by: DvD
                                 Translation by: harmony7
                Pointer Table & Text Hacking by: DvD

                   Text Save States Acquired by: Damiano
                 Text Editing & Beta Testing by: DvD
                                      ReadMe by: DvD & Wikipedia

----------------------------------- CONTENTS ----------------------------------

THE MANUAL

(1)  King Kong 2 Game Series & History
(2)  Game Description & Controls
(3)  Secret Messages

USING THE PATCH

(4)  Patching the ROM file
(5)  Playing the game on an emulator

TRANSLATION DETAILS

(6)  Why DvD chose to translate THIS game
(7)  Why YOU should bother playing THIS game
(8)  DvD's Hacking Comments
(9)  harmony7's Translation Comments
(10) Damiano's Save State Acquisition Comments
(11) Project Timeline
(12) Software Used In This Translation

---------------------------------- THE MANUAL ---------------------------------

(1)------------------- King Kong 2 Game Series & History ----------------------

The King Kong 2 series consists of the following 2 games:

KING KONG 2: ikari no MEGATON PUNCH - Famicom - December 18, 1986
KING KONG 2: yomigaeru densetsu     - MSX     -              1987 

Both of these games were based on the Japanese release of an American movie
called "King Kong Lives" which was titled "King Kong 2" in Japan.  Hence,
Konami never made a King Kong 1 video game that these are sequels to.

The following movie spoiler and games description is mostly taken from
Wikipedia:

King Kong, after being shot down from the World Trade Center, is kept alive in
a coma for about 10 years at the Atlantic Institute, under the care of surgeon
Dr. Amy Franklin.  In order to save Kong's life, Dr. Franklin must perform a
heart transplant and give Kong a computer-monitored artificial heart.  However,
he lost so much blood that a transfusion is badly needed.  Enter adventurer
Hank Mitchell, who captures a giant female gorilla in Borneo, bringing her to
the Institute so her blood can be used for Kong's operation.  The transfusion
and the heart transplant are a success, but Kong escapes alongside the female.
Archie Nevitt, an insane army colonel, is called in with his men to hunt down
and kill the two apes.  Lady Kong is captured alive by Nevitt's troops and
imprisoned; Kong falls from a cliff and is presumed dead, but soon returns to
try and rescue his mate.  But as Franklin and Mitchell soon discover, Kong's
artificial heart is beginning to give out.

The Famicom game totally discarded the human aspect of the story and players
played as King Kong who has to travel around the globe fighting giant robots
and certain military forces in order to save the female Kong.  The game is
an action adventure game with some science fiction concepts.

The MSX game, on the other hand, plays from the perspective of Mitchell.
This game is an action RPG game which looks like Konami's Metal Gear 1 (MSX)
but plays more like Zelda.  A complete translation of this game already exists.

(2)---------------------- Game Description & Controls -------------------------

For a nice html copy of the manual with graphics, go to my favorite website
for Japanese manuals:

http://www.geocities.jp/frnyanko/setsumei/famicom/kingkong2/kingkong2.html

and use the language tools of Google to translate it into English:

http://www.google.com/language_tools

For this game, I found that it actually does a pretty good job.

In case you don't want to do that or the page is gone, there are 8 worlds.
Each world has a boss and each boss holds a key.  Collect all the keys to open
the door to Lady Kong in the 9th world.  There are lots of warp doors in the
worlds that will teleport you to different parts of the world or to other
worlds.  You don't have to defeat the bosses in any particular order.

Start                 - Start Game
                      - Switch between menu/game

A                     - Jump
B                     - Punch/Throw Rock
Select                - Switch between punching and rock throwing


(3)---------------------------- Secret Messages -------------------------------

Secret Messages:

Besides the title screen, these messages were the only things that needed to
be translated in the game.

Hold A + B       - During the ending, gives you a secret message based on how
                   many hours it took you to pass the game.  Make sure you are
                   holding them both at the moment the credits stop scrolling.
                   There are 24 different messages.  Many messages end with a
                   number.  The number indicates a word or phrase in Japanese
                   which is related to how well you did in the game.

                   For example, ever wondered why the number 573 comes up all
                   the time in Konami games? Well...

     5 7 3 ==can be pronounced==> go nana mi ==which sounds like==> Konami


------------------------------- USING THE PATCH -------------------------------

(4)------------------------- Patching the ROM file ----------------------------

Game ROM size: 8 16k program   ROM banks
                          &
              16  8k character ROM bank
              = 256kBytes
           = 262144 Bytes

Games designed for the original Famicom/NES hardware have one or two 16k
program banks and one 8k character bank.  Later, all games made for the NES
used special mapper chips to expand the size of the addressable ROM beyond
these limitations.  This game uses the first special mapper chip made by
Konami, VRC1.  VRC1 is simply used to switch in different sections of character
and program ROM as this cartridge has no VRAM.

How to patch the ROM file:

You need:

1) A ROM file.  The file needs to include the standard 16 byte iNES header
   followed by the program ROM.  With header, the ROM file is 262160 bytes in
   size.

   The header should be as follows:

               4E 45 53 1A  08 10 B1 40  00 00 00 00  00 00 00 00

   I'm not telling you how to get the ROM file, but once you do, call it
   KKLives.nes.

3) Patch File: DvD_KKL.IPS

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
      (I'll call it KKLives.nes), DvD_KKL.IPS, and
      Snes-Tool.exe in the same directory.
   c) Run Snes-Tool.exe
   d) Type 'U' for "Use IPS"
   e) Press the down arrow key until DVD_KKL.IPS
      is highlighted.
   f) Hit Enter.
   g) Press the down arrow key until KKLIVES.NES is highlighted.
   h) Hit Enter.
   i) Hit 'Q' to quit.

(5)-------------------- Playing the game on an emulator -----------------------

All emulators that can play the original ROM file can play the translation.
No expansion or mapper changes were done and it uses the very common VRC1.

It will RUN in almost all emulators, but I recommend FCEUXD SP 1.07 as the most
recently updated version of the FCE Ultra line.  The official version's of
FCE Ultra out there that you can download, really messed a lot of things up.

----------------------------- TRANSLATION DETAILS -----------------------------

(6)------------------ Why DvD chose to translate THIS game --------------------

Hmm, why this game...

Well, the MSX game looked pretty cool, it reminded me of Metal Gear 1 on the
MSX.  I was intrigued on why there was no King Kong 1 but that there were 2
seemingly different King Kong 2 games...


(7)---------------- Why YOU should bother playing THIS game -------------------

For the first time, DvD didn't pass it himself.  That role was filled by
Damiano for this project.

It's just an action game with lots of warp zones.  Not really DvD's cup of tea.

Play it if you like.

(8)------------------------- DvD's Hacking Comments ---------------------------


I originally thought this was just going to be a title screen hack which I
could do on my own, w/o the services of a translator.  I had actually made a
title screen which said KING KONG 2 and translated the subtitle differently.

At some point, I realized that the game was based on an American movie called
King Kong Lives and that I needed to redo the title screen anyway, so I asked
harmony7's opinion on the subtitle.  We compromised on the current subtitle.

But then, I found some words in the game that didn't seem like credits.  Even
though they were written using roman letters, the seemed to be Japanese.  What
were these strange words?  harmony7 figured it out from a Japanese web site and
also told me how to display the text.  But now, someone had to play the game
so we could see the ending credits!  That is where Damiano volunteered to help.
And he did a great job getting me save-states at every point in the game where
there was more text, although it turned out that the text after each boss was
the same and was in English anyway.

3 days after harmony7 translated the ending text through IM, the translation
patch was completed and tested by DvD.

(9)-------------------- harmony7's Translation Comments -----------------------

Another classic game that I've owned for ages.  If you like blowing things up
pointlessly, this game is for you.

The text in this game was Japanese, but spelled out using the Western alphabet.
This was a typical design decision back when games didn't have that much memory
available to them.

I personally thought that many of the translated quotes were only applicable to
people who played games during that period, i.e., kids after school.  I don't
think that many adults in Japan played games back then.  However, DvD said
he thinks they're okay, so I said go for it.  But if you get any of the
endings, you'll see what I mean.

Of course, who's going to spend 24 hours playing the game to see one sentence?

(10)--------------- Damiano's Save State Acquisition Comments -----------------

I came to know DvD through one of his other works, which was 
Dragon Slayer Jr. - Romancia. While researching the history of Japanese RPGs I 
had discoverd information about Dragon Slayer, which was rumored to be the very
first JRPG ever. Released in 1984 it even outdated Hydlide, The Legend of Zelda
and Dragon Quest/Dragon Warrior. I was fond of the idea of playing the 
Dragon-Slayer-Series and was overjoyed to learn that Part 1 and 2 were already 
written in English. With Part 3, aforementioned Dragon Slayer Jr. - Romancia, 
this was another story. It was in Japanese and only by coincidence I found
DvD's translation for it. After playing it for awhile I contacted him to thank
him and his friends for their good work on it and to get some help with one
part. I received very kind aid and began to chat with DvD about old games until
he asked me if I would be interested in helping him out with one of his smaller
projects, which was this game: King Kong 2 - Ikaro no Megaton Punch. I was
eager to help since I always admired fan translators for putting their time
into their work so that other gamers could enjoy formerly untranslated games
in English, German, Spanish and so on. And although my role had been a minor
one in this project I am proud to have been able to contribute to one of those
translations. Actually, all that DvD needed me to do was to play through the
game and to collect savestats from right after beating the several bosses, but
before the text sequences this game contains so that he can modify these. 
All in all, this game was tremendous fun, but I experienced it as hard as hell
at first. It sure was irritating with all the warp gates all over the place and
enemies swarming the screen! ;) But after I got a hang of it I was able to get
through the game quite smoothly. I would recommend it to anyone who likes 
action-games or just Japanese games in general. 
It was fun contributing to this project and I enjoyed working with DvD who was 
always eager to answer my questions and to tell me how happy he was with the 
savestats.
I would definitely do this again! :)

(11)--------------------- Project Timeline Highlights -------------------------

Jan  2 2008 - Project Started by DvD
Apr 25 2008 - First new title screen completed
May 14 2008 - Final new title screen completed
Jun  3 2008 - Ending save state acquired
Jun  4 2008 - Ending text translated
Jun  7 2008 - Patch completed, testing completed, readme started
Jun  9 2008 - Readme completed, Patch Released

(12)------------------ Software Used In This Translation ----------------------

* Emulators

  PC
   - FCEUXD SP 1.07
      If you like FCE Ultra, you will love FCEUXD SP.
      Thank you RedComet for pointing this one out.
      It is the emulator that I will be using from now on; it's awesome.
   - FCEUltra v0.94
      by Bero & xodnizel

* Tile Editor
  
  Tile Layer Pro 1.0
   by Kent Hansen

* Disassembler, Table Dumper

  Table Dumper Pro (ver 8.6.7)
   by DvD

* Hex Editors, Script Dumper

  - Thingy Version 0.98
     by necrosaro

* Readme Creation

  Notepad (Win XP)
   by Microsoft

* IPS Patch File Creator

  Snes-Tool Version 1.2
   by The M.C.A./Elite

-------------------------------------------------------------------------------
987654321098765432109876543210987654321 123456789012345678901234567890123456789
