-------------------------------------------------------------------------------

ReadMe-DvD_Translations-Dragon_Slayer_Jr_Romancia-revA.txt

This file should be viewed using a mono-spaced font like "Courier".
Use a font size where 79 columns are visible.

Please don't distribute the ROM file in patched form.
Please don't distribute the DvD_DSJr.IPS file without this file.
Thanks.

-------------------------------------------------------------------------------

                          Dragon Slayer Jr. - Romancia

                                      AKA

                               Dragon Slayer III

                         Original Game by Nihon Falcom
                Famicom Version Copyright 1987 by Tokyo Shoseki

             English Translation Copyright 2008 by DvD Translations
             Patch Version: Rev A      Release Date: April 23, 2008    

                                DvD Translations
                      dvdtranslations.eludevisibility.org

                  Reverse Engineering by: DvD
                           Code Edits by: DvD
                          Translation by: harmony7
                       Graphics Edits by: DvD
                         Beta Testing by: RadicalR, DvD, & KlD
                 Limited Beta Testing by: Agent Baron
                       Script Editing by: RadicalR, DvD, KlD, & harmony7 
      Game Play Improvements Designed by: DvD & RadicalR
                               ReadMe by: DvD

----------------------------------- CONTENTS ----------------------------------

THE MANUAL

(1)  Dragon Slayer Game Series History
(2)  Game Description
(3)  Controls
(4)  Helpful Hints

USING THE PATCH

(5)  Patching the ROM file
(6)  Playing the game on an emulator

TRANSLATION DETAILS

(7)  Why DvD chose to translate THIS game
(8)  Why YOU should bother playing THIS game
(9)  DvD's Hacking Comments
(10) harmony7's Translation Comments
(11) RadicalR's Beta Testing Comments
(12) Project Timeline
(13) Software Used In This Translation

---------------------------------- THE MANUAL ---------------------------------

(1)------------------- Dragon Slayer Game Series History ----------------------

The Dragon Slayer series consists of the following games:

Dragon Slayer
Dragon Slayer II : Xanadu        (plus at least 2 expansion packs)
Dragon Slayer Jr.: Romancia
Dragon Slayer IV : Drasle Family (English released as "Legacy of the Wizard")
Faxanadu                         (Dragon Slayer II Gaiden)
Dragon Slayer V  : Sorcerian
Dragon Slayer VI : The Legend of Heroes

The series continues to this day, either as sequels to The Legend of Heroes
or sequels to Sorcerian.  Keeping track of them all is pretty confusing.

As with most Falcom games, they were ported to many systems.

Two games in Falcom's Dragon Slayer series were ported to the Famicom and a
gaiden was created specially for the Famicom.  However, only two of these
games ever saw releases in English.  Now, you can play the one we missed out
on.

Dragon Slayer IV : Drasle Family Namco          07/17/87
Dragon Slayer Jr.: Romancia      Tokyo Shoseki  10/30/87 
Faxanadu                         Hudson         11/16/87

Dragon Slayer I and II were only originally released for Japanese 8-bit PCs.

Sorcerian, probably the best game in the series, was released for the Sega
Megadrive and PCEngine CD, but sadly, was not translated.  Still, Sierra did
port the IBM PC version.

Dragon Slayer VI (I & II) were released for the Super Famicom, Sega Megadrive,
and PCEngine CD.  Only the TurboGrafx-CD version was released in English.

(2)---------------------------- Game Description ------------------------------

Romancia is a side-scrolling action RPG.  You control Prince Fan who must heal
the people of Romancia and save Princess Celina.  You will travel to heaven and
hell and back trying to find the legendary Dragon Slayer to rescue the girl you
love.  The original game had a 30 minute timer, but Tokyo Shoseki has increased
the size of the game and gotten rid of the timer.  Now, the challenge in the
game is both trying to figure out what to do and doing all of this without
being able to save.  Although you can buy or find items that will refill your
health or increase your hit points, you cannot get any stronger, and only the
monsters in the first area drop hearts or swords and monsters never drop
money.

--Selectable Items--

You can have a total of 8 selectable items at one time.  You cannot have more
than one of the same item.  People will mention most items before you find
them and items you can acquire are always shown between [square brackets].
There are a total of 16 different items that can be found.

Some of the items can be used up, and some can only be gotten rid of by giving
them away or selling them.  Some items you can re-acquire an infinite number
of times and others exist only in limited quantity.  Not all items are needed
to pass the game.

--Multi-Quantity Items--

[Heart]  HP     Max 30  When it gets to 0, you die, unless...
[Swords] Swords Max 15  Quantity of swords that Prince Fan can throw
[Coin]   Money  Max 30  Quantity of Gold Coins
                        You can buy things with these.
[Staff]  MP     Max 15  Use these to cast spells.
                        You need to select a magical item to use first.
                        If you run out of MP, and you try to use a magical
                        item, it will disappear, so watch out!
[Shield] Shield Max 30  Each shield is equivalent to 1 HP.
                        You will USUALLY have to lose all your shields before
                        you lose any HP, although environmental effects may
                        bypass your shield and simply affect your HP.
[Ring]   Karma  Max 30  You need your Karma to be at least a certain level to
                        do certain things to advance the game.  Usually you
                        want to raise your Karma...

For a reasonable level of challenge, DvD Translations recommends that you use
save-states only at one place in the game, the first church.  Then the game
plays more like Faxanadu, where you could always get a password at the church.
(This isn't counting the unreasonably difficult final boss...)

DvD Translations has done a lot to make this game more playable.  See section
(8) for details.  If you don't want to read it, then know that if you talk to a
person who says "Cheater", that that character was essentially a statue in the
original Japanese game.

(3)-------------------------------- Controls ----------------------------------

Start                 - Start Game
                      - Pause Game = Allow you to Select Item in Inventory
                      - Un-Pause Game

Up, Select, A, & B    - Hold while hitting Start at title screen to enter
                        the "Sound Test" screen

Left, Right           - Select Item in Inventory

Up, Down, Left, Right - Move Prince Fan

Up                    - Jump Up
                      - Talk to a person
                      - Talk to a person again (if you don't move first)
                      - Give item to person

Up, pause, Up         - Double Jump

Down                  - Search

Tap A                 - Use Selected Item in Inventory on Prince Fan

Tap B                 - Swing Sword

Hold B                - Throw Sword

(4)----------------------------- Helpful Hints --------------------------------

As with ALL RPGs, always talk to a person without moving until they repeat what
they say, they may say multiple things and you'll need every hint they give.
And of course, if you do something, they may change what they have to say. 

There's more than one thing worth finding in Paradise...

You can only get limited quantities of some items.  One of the "Cheaters"
allows you to overcome this limitation for one of these key items.  If you seem

to have run out of something you need, visit him.

You can escape from hell.

Your first goal is to raise your Karma all the way.

------------------------------- USING THE PATCH -------------------------------

(5)------------------------- Patching the ROM file ----------------------------

Original game ROM size: 8 16k program ROM banks
                          &
                        0  8k character ROM bank
                      = 128 kBytes
                      = 131072 Bytes

Games designed for the original Famicom/NES hardware have one or two 16k
program banks and one 8k character bank.  Later, all games made for the NES
used special mapper chips to expand the size of the addressable ROM beyond
these limitations.  This game uses the first fancy mapper chip made by
Nintendo, MMC1.  For this game they used it to switch between 8 different
program ROM banks and to use VRAM instead of ROM for the background and
sprite tiles.  Also, for this game, they used the MMC to do a pattern table
swap in the middle of the screen.  It is this last feature which some
emulators do not emualate correctly.

How to patch the ROM file:

You need:

1) A ROM file.  The file needs to include the standard 16 byte iNES header
   followed by the program ROM.  With header, the ROM file is 65552 bytes in
   size.

   The header should be as follows:

               4E 45 53 1A  08 00 10 00  00 00 00 00  00 00 00 00

   I'm not telling you how to get the ROM file, but once you do, call it
   Romancia.nes.

3) Patch File: DvD_DSJr.IPS

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
      (I'll call it Romancia.nes), DvD_DSJr.IPS, and
      Snes-Tool.exe in the same directory.
   c) Run Snes-Tool.exe
   d) Type 'U' for "Use IPS"
   e) Press the down arrow key until DVD_DSJR.IPS
      is highlighted.
   f) Hit Enter.
   g) Press the down arrow key until ROMANCIA.NES is highlighted.
   h) Hit Enter.
   i) Hit 'Q' to quit.

(6)-------------------- Playing the game on an emulator -----------------------

All emulators that can play the original ROM file can play the translation.
No expansion or mapper changes were done and it uses the very common MMC1.

It will RUN in almost all emulators, but Nesticle and RockNES have the same
problem, the don't handle the pattern table switch and so the graphics on half
of the screen look garbled.

I recommend FCE Ultra version 0.94.  Version 0.98 added graphics enhancements,
but screws up save-states and batteries and killed the debugger.  I'm thinking
of giving a link to version 0.94 on my site because it is hard to find.

Nestopia also works well and I'm sure that will be the emulator that most
people play it on.

----------------------------- TRANSLATION DETAILS -----------------------------

(7)------------------ Why DvD chose to translate THIS game --------------------

Well, I like to play games in the order they were released.  At some point
during my collecting of RPG/action RPG games for the NES, I had picked up
"Legacy of the Wizard" and it was getting to be time that I actually played it.
Still, I had always heard how difficult it was, so I was hesitant to play it.

Anyway, with the wealth of game information on the net, I had recently learned
that LotW was actually called Dragon Slayer IV: Drasle Family (why do companies
change game names so drastically?  It always comes back to bite them in the ass
when they try to release sequels to the game...)  So, it was part of a larger
game series, by Falcom, whose other series, Ys, is one of my favorites.  The
problem was that LotW was 4th in the series and all the prequels were in
Japanese.  A good thing, though, was that Faxanadu was part of the series.
Faxanadu is one of the NES action RPGs in my collection that I was given as a
kid and I always liked it.  It wasn't the best game I had ever played, but it
definitely was fun.  So, I thought that the other games would be similar.
Later, I realized that Hudson had taken a lot of liberties with the game engine
when they made Faxanadu, and had improved it a lot.

Anyway, a third game in the series had been released for the Famicom but had
never been translated for the NES.  It was Romancia, a game I had tried since
FCE Ultra, made a point to say that they had gotten the game to work with a
specific release of the emulator, since apparently, it wasn't the most
straightforward game to emulate.  I tried it again, and it looked pretty good.
In the first part of the game, the forest, the graphics and music were pretty
good, and characters dropped hearts and swords to re-fill your inventory.  I
couldn't figure out how to exit the forest, but I had seen enough... or so I
thought!  The game play seemed reasonably fun, plus the title screen did a
cool effect that looked like it would be fun to edit.

Well, Dragon Slayer and Dragon Slayer II - Xanadu were not made for any of
the systems that I was interested in making a patch for.  DS is essentially
in English already, since it practically has no text.  I tried it.  It wasn't
fun.  Xanadu, through, seemed pretty cool; I originally considered translating
it, even though it wasn't for a system I normally produce patches for, but
since I wasn't even going to play Dragon Slayer, why bother?

So, I dove into Romancia, and found that there was just one simple block of
text, with pointers, plus ample room for a good translation and any hacking
room.  It looked pretty reasonable to hack, and so I gave it a try.  Actually,
I'm glad I did.

(8)---------------- Why YOU should bother playing THIS game -------------------

Well, this is the best effort DvD translations has put out to date.  Really,
we polished this turd so much that some people might actually LIKE the game.
Although, we're not holding our breath!  Read on to find out what we did and
why we did it...

If you are a fan of Faxanadu and Legacy of the Wizard, you can see where these
games came from... and see why no one bothered to officially translate this
one!

Actually, the game is pretty fun up through visiting Romancia town.  Everyone
should give it a try to see the title screen translation and graphics fixes.
But more importantly, the text.  Of course, this time, we had the excelent
harmony7 to accurately translate it, and we all worked together to polish the
script.  (For all those who care about Portopia Rev B, he's been 75% done with
the script for the better part of a year now...)  But, what DvD is personally
very proud of is the hacking he did to put a variable-width font in the text
box.  He didn't do it to be flashy, he did it out of necessity.  But, as far
as we know, it has never been done on any NES game before, and it works
perfectly.  (Yes, we know the Japanese Esper Dream 2 had a VWF font but it was
huge font that either was 1 or 2 tiles wide for every character, not ANY width
for each character.)  If you know of another NES game with a VWF, released
before DvD finished his (technically in March of 2007), don't slam us, just
let DvD know.  He'd be interested in seeing how they did it.

The Japanese version of this game was REALLY hard.  Think about it, a
multi-hour action RPG where you CAN'T SAVE with a practically impossible final
boss.  Thank God for save-states.  Plus, there were many places in the game
where it was not obvious what to do.  There were things you could do that you
really couldn't recover from; all you could do was reset and try again.  By the
way, the reason that this was so was that the original Falcom game was only 30
minutes long.  It had a timer.  If you couldn't complete the game in 30
minutes, you had to reset anyway.  So, resetting when you got stuck wasn't
really a big deal.  We realized that that is why the game is called "Jr.".  It
is not because it is easy, but because it was Xanadu, but in a much shorter
form where there really was no need to save.  Unfortunately, Tokyo Shoseki
ruined the game by making it much longer (for example, in the original game,
you start at Romancia castle!) without adding the ability for a password or
battery save.

After RadicalR and DvD finally passed the game (RadicalR playing first, DvD
delving into the code to figure out why RR was stuck) we decided the game
would have been a lot more fun if Tokyo Shoseki wouldn't have coded it like
they had.  RadicalR was given the task of playing as much of the MSX version
as he could stand and we could see tons of changes Tokyo Shoseki had made,
sometimes for the better and but usually for the worse.

DvD realized that if we released the game as is, no one would pass it, no one
would like it, and our translation would seem poor because of it.  We decided
to leave the changes Tokyo Shoseki had made to the game, but make the game
playable for a person who chose to use save-states to emulate a password save,
like Faxanadu.

But, except for the final boss (who we didn't touch), we didn't need to make
the action easier.  We HAD to make this game better in terms of the hints it
gave the player.  Plus, there was a cool item in the game that had been removed
for some reason.  And, there were places in the game where you could screw up,
and not be able to pass the game.  There were limited numbers of certain key
items.  Also, there were a number of places where the original coders just
simply made a mistake and the reason we couldn't figure out something was
because of these mistakes.

But, there are always purists out there, who hate it when a game is changed.
We wanted to make everyone happy, but DvD was very firm in wanting only one
version of the translation available.  Believe us, we thought about this a lot.
To make both groups happy, we made 3 key decisions:
1) Obvious bug fixes were acceptable.
2) Any text enhancement or complete additions, would be acceptable and not
   considered changing the game.
3) Any action that affected your players inventory in a way that couldn't be
   done in the original game would be completely optional for the player and
   obvious to avoid... if they wanted to torture themselves.  Thus, I'll say
   this:  If you want to play without "cheating"
   - Don't walk back to the first 2 guys from the forest
     This was in the ROM but they removed it for some reason...
   - If someone says "Cheater" don't talk to them again, they originally
     didn't say anything at all!  2 of these 3 people simply perform actions
     that existed in ROM (one all the text existed and the other the item did)
     but were removed for some reason.  I really wanted to bring back what
     they had removed, regardless of whether they made the game any easier
     (or harder!).  The last was added so that you wouldn't have to restart
     the game if you did something too many times.  This character was added
     based on RadicalR's request.

With the changes we've made, to maintain a fun level of challenge, let us
recommend using save-states but only creating them in one place, to simulate
a password save.  If you do it at the first church it will be just like saving
in Faxanadu.  The only place we would also reccomend creating save-states is
when you are fighting the final boss; he is unreasonably difficult.

(9)------------------------- DvD's Hacking Comments ---------------------------

There are 3 major parts to this translation:

1. The Variable-Width Font

The variable-width font was added because it was impossible to simply expand
the text box.  The original game does not write tiles to the text box.
Instead the same 30 tiles are permanently used to form the contents of the text
box.  The tiles' pattern tables are in VRAM, and the pattern tables are written
to with the shapes of the letters from PROM, based on the text that needs to be
displayed.

Well, there was no way that English text was going fit in a 30 character box
and there were no more characters to use to expand the size of the box.  The
only thing that was going to work was to display multiple characters per tile.
So, this was my first task.  If I couldn't get it to work, there was no reason
to continue working on the game, and we would abandon the project.  It was a
fun challenge.  I knew people implemented VWFs on Genesis and SNES games, but
I didn't look at any of those.  I just thought about what needed to be done
and wrote the code out.  I kept editing it until it fit in the location where
the original text code existed.

Well, after I tested the code that I wrote and ironed out all the bugs to get
it to write and erase text correctly, it looked like it wasn't going to work.
There was a timing issue.  While it was writing the text, the screen would
scroll randomly.  I had done everything I could think of to make the
routine as efficient as possible, but it still had a problem.  I looked
everywhere in the code to see what I could disable, but nothing worked.  After
days, I stumbled upon a solution.  I simply made the maximum height of the
characters 7 pixels instead of 8.  Most characters aren't 8 pixels high anyway
since you need a blank row of pixels to separate lines of characters.  That was
it.  It now looks like the font you see today with no timing issues.  A 7-pixel
font also had another advantage.  The VWF information could be stored on
8th byte and now it was easy to view the font and its VFW info together.

Now that that was done, Romancia HAD to be done... of course, I had not played
the game much yet...

Soon after I finished this, harmony7 gave me a 65%-complete script which I
inserted... oh yeah, that's right, I added the script inserter to Table
Dumper Pro for this game at this time, in preparation for his script.  With
this, I could finally start playing the game.  I played for about an hour and
at this point I still liked the game...

2. The Title Screen

Hacking the title screen was much more complicated than it looks.  Deja vu.
Hacking it went through several stages:

1) The title screen graphics are all compressed.  I had to write a custom
   compressor to re-insert them from a BMP I made from a screen shot.
   This first version just replaced "ro-ma-n-shi-a" with "Dragon Slayer Jr.".
   
   Although this accomplished what I needed, it still looked bad.  The
   graphics for the princess and prince looked terrible since they were a
   pixel by pixel port of the MSX2 version and the MSX2 could display colors
   without the restrictions of the NES.

2) The compressor was expanded to be able to modify ALL the graphics of the
   title screen.  Now the prince and princess's eyes, the prince's bandanna,
   the princess's hair, her crown and jewels, the castle, flags, sky, grass,
   pathway, etc., could be fixed so that they didn't look so terrible.  The
   only remaining flaw deals with the castle.  Since they imported the screen
   from the MSX2, the bottom of the castle was not put on an attribute table
   boundary.  There is no way to get the castle be completely white and cyan
   unless it was moved up by exactly 5 pixels.  But this would change how it
   looked by a lot since it would now be covered by the prince's hair.  So,
   I decided to leave it like it is.

   Still, something seemed wrong.  The title of the game was Romancia, not
   Dragon Slayer Jr. That bugged RadicalR and was starting to bug me...

3) Now that it was relatively easy to edit the title screen, I decided to
   throw away the work I had done making it say Dragon Slayer Jr. and change
   Romancia at the top to Dragon Slayer Jr. and have it fade in Romancia using
   the same script that was original used to write Romancia at the top.  The
   result is what you see today.

4) There are two other things dealing with the crown.

   While working with the graphics fixes and changing which colors were in
   palettes of the sprites, I had to define the white color to be used in the
   jewels in the crown.  In doing so, I made a small mistake on one of the
   colors.  But this mistake caused them to sparkle when Romancia was being
   shown on the screen.  When I fixed the mistake, I decided I liked the
   sparkling and changed it back.

   The gold color of the crown was not very intense in FCE Ultra and looked
   too close to the color of the princess's skin.  So I changed it slightly to
   look more gold.  Well, this looks kind of green-gold in Nestopia, but it
   still looks ok to me, so I left it with the change.

3. The Game Play Enhancements

Read section (8), all that you need to know is detailed there.

(10)------------------- harmony7's Translation Comments -----------------------

This is the first time I've worked on a complete script of a game before I'd
played through it.  This enough was enough to make working on this game more
challenging than any other translation I've been involved with.

Granted, the script for this game was short.  It was just a bit over 100 blocks
of text.  But this actually made this project much more difficult than anything
I had worked on in the past.

With Final Fantasy V, Dragon Quest 3, Portopia Serial Murder Case, Mother 3,
and anything else I'd attempted before, I'd played through the games (quite
thoroughly, I might add) before taking up their scripts.

Translating games is not like translating a book.  I would imagine that it is
closer to translating a movie, in that the text script by itself is not enough
information to gain a complete understanding of what's happening.  One would
have to experience the full audio and visual elements to see how the parts
fit together.

Each text block was just a few words, taken out of context, from a game I'd
never played... It was quite an interesting experience.

Even still, I feel I might have had an easier time than RadicalR.  I'm sure
the difficulty of this game has come back to haunt him in his dreams.

(11)------------------- RadicalR's Beta Testing Comments ----------------------

I won't say much. This was probably the hardest beta I had to do. Last count of
restarts: 56 (Yes, I actually counted!) However, you shouldn't have to restart
so many times, now we fixed a lot of the bugs.... And I don't care what the
game says. I DO NOT HAVE CONNECTIONS.

(12)--------------------- Project Timeline Highlights -------------------------

Dec 23 2006 - Project Started by DvD
Mar 29 2007 - First VWF Working; DvD decides to complete the project
Apr 25 2007 - Ready for first script
May  1 2007 - First harmony7 script inserted
May  3 2007 - First title screen hack, as Romancia - Dragon Slayer Jr.
Jul 21 2007 - Beta testing by RadicalR begins
Oct 16 2007 - Table Dumper Pro Released, hidden item found
Jan 24 2008 - Game play improvements finished; final beta testing can begin
Apr  9 2008 - Hacking completed, final issue dealing with the added item fixed
Apr 19 2008 - Final beta testing by KlD completed
Apr 22 2008 - ReadMe editing completed

(13)------------------ Software Used In This Translation ----------------------

* Emulators

  PC
   - FCE Ultra 0.94          (debugger, beta testing, version 0.98 sucks!) 
      by Bero & xodnizel
   - Nesticle                (used to isolate sprites from background)
   - Nestopia                (Mac & PSP versions, beta testing)

* Tile Editor
  
  Tile Layer Pro 1.0
   by Kent Hansen

* Disassembler, Table Dumper

  Table Dumper Pro (many versions, but that last one was 7.10.13 INTERNAL)
   by DvD

* Hex Editors, Script Dumper

  - Thingy Version 0.98
     by necrosaro

* Disassembled Code And Table Reverse Engineering

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
