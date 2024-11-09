




               Battle Mania Daiginjou / Trouble Shooter Vintage

                         English Translation Patch




 History
-----------------------------------------------------------------------------

061029 Initial release




 Overview
-----------------------------------------------------------------------------

This is a translation patch for the Mega Drive game "Battle Mania Daiginjou".
In what has become something of a trademark, this is a "dual-language" patch,
meaning that it supports both Japanese and English. However, it goes far
beyond simply supporting both English and the original Japanese; it contains
two different English translations and a selection of three English fonts.

The translation is divided into two separate IPS patch files, but the only
differences between the two are the default script and font to use if none
are selected by the user. That is correct; it is possible to select the
desired script and font by holding down certain combinations of buttons
prior to the Sega logo appearing.



 Applying the Patch
-----------------------------------------------------------------------------

Hopefully included with this document are two patch files in the IPS format.
You can use any program that supports this file format to apply one of the
patches to your ROM file.

There are two versions of this game that I am aware of: one released in 1993
and one released in 1995. The two versions are practically identical, except
that the 1995 version gives incorrect results during the system test screen.

There are also numerous hacks and one damaged file circulating around the
internet. This patch will properly overwrite all the hacked versions that
I've encountered, but not the damaged file. It will also revert the 1995
version back to the superior 1993 edition.




 Playing the Game
-----------------------------------------------------------------------------

Once you've patched the ROM file, simply load it up in your favorite
Genesis / Mega Drive emulator, console copier, or flash cartridge.

The game will detect the country code of your machine (real or emulated) and
then switch to English or Japanese mode accordingly. The script and font
that are used will depend on which of the two patches you applied. However,
you can change the default behavior (and override the country code) by
holding down certain buttons while the game is powering up or resetting:


A + Start      Original Japanese script
B + Start      Battle Mania Daiginjou  English script
C + Start      Trouble Shooter Vintage English script

Left + Start   All-capital indigenous font
Right + Start  All-capital indigenous font (thicker)
Up + Start     Upper- and lower-case font

ABC + Start    Normally you'd have to unplug your 'pad to see this...


You can combine buttons to change both the script and the font. As you can
see, you must always hold down the start button to get any effect.

You should hear a sound effect if the above worked (and sometimes even if
it didn't, in case you pressed the wrong buttons). That's your cue to
release the buttons if you want to see the introductory material (otherwise
you'll skip straight to the title screen).




  Patch Differences
-----------------------------------------------------------------------------

The "Trouble Shooter Vintage" version was intended to look and feel like an
official English translation. It follows the naming conventions of "Trouble
Shooter" (which was the official translation of the first game in the series)
and defaults to using an all-capital font, just like in the original. Some
of the language was also toned down a bit, which was typical for games in
that time period. A little bit of stuff (not in the script) got thrown out
as would have undoubtedly happened in an official localization at that time.
The credits sequence should have been axed as well, as it would not have made
it overseas, but I wanted to have two different versions of the credits too.
The translation is also quite a bit looser, although it is still much more
accurate than Trouble Shooter was; although some English idioms were used,
no Western cultural references were permitted in this script.

The "Battle Mania Daiginjou" edition was intended to be much more accurate,
even to the point that you might not understand parts of it if you don't
know anything about Japanese culture. To be honest, you might not fully
understand it even if you are a Japanese native, as a few of the allusions
are somewhat obscure. Many of the graphics were subtitled in this version,
and the original names were used.

The differences are significant enough that you will probably enjoy playing
both versions at least once.




 Q & A
-----------------------------------------------------------------------------

Q: Which of the two patch files should I use?

A: It doesn't really matter; they are basically identical internally; the
   only difference is that one defaults to "Battle Mania" mode and the other
   other defaults to "Trouble Shooter" mode. See the above section for more
   details on the differences. The Trouble Shooter version will probably
   be preferred by the majority of people though.


Q: This patch doesn't work! What do I do?

A: Make sure your ROM file is not in an interleaved format. It's also
   possible that there is more than one version of the game, or that your
   copy is corrupt.


Q: It doesn't work with my copier / flash cartridge! Why not?

   This was tested on a real Genesis so you shouldn't have any problems in
   that respect. The most likely reason is that something went wrong during
   the patching process. See the previous question and try it in an emulator
   to see if that works.

   Another possibility is that you are using a PAL Mega Drive; this game was
   designed for NTSC systems and I didn't make any changes in that respect.
   It should still run (probably at the wrong speed), but you never know...


Q: Why is the text in Japanese?!?

A: This is a dual-language translation patch; if it detects that it is
   running on a Japanese system, it will use the original game script.
   If you are using an emulator, make sure the country code is set to USA.

   Also, the game can be configured to run in any mode, regardless of
   the machine's country code, by holding down certain buttons as the
   game starts. See the relevant section above for details.


Q: Why are the credits written sideways??

A: Although English is more esthetically pleasing when written vertically,
   it is much easier to read when printed sideways. If you doubt this, just
   visit a library and examine the spines of the books.


Q: Why was Mania's name changed to Madison?

A: Mania's name was changed to Madison when Battle Mania was localized for
   the Western market as Trouble Shooter. The "Trouble Shooter Vintage"
   version of this patch tries to maintain consistency with the original
   translation of Trouble Shooter, whereas the "Battle Mania Daiginjou"
   version uses the original names and spellings.


Q: Why was Maria's name changed to Crystal in the original Trouble Shooter?

A: Maria is certainly a normal-sounding name, but I think they might have
   changed it so it would be the same size as "Madison" in the intro.

   Maria is the blue-haired girl, in case you were wondering... (her name is
   not used anywhere in this game).


Q: "She"?? (this question applies to "Battle Mania Daiginjou" only)

A: This is correct. It's very difficult to properly translate certain
   phrases without using gender pronouns (which aren't normally used in
   Japanese), but the pronouns used always accurately represent the
   characters' perceptions.


Q: Why aren't the kanji / kana in the in-game backgrounds translated?

A: It's a lot of work, it's difficult to redraw them while maintaining
   anything close to their original meanings, it detracts from their original
   beauty, it could be distracting, and it wouldn't provide much additional
   meaning anyway. Translations for some of them are included in this file,
   for those who are interested. See below.


Q: What does the text just before you fight Kikokusai mean?

A: Something like "Kikokusai arrives".


Q: What does the text on the Hard Mode ending screen mean?

A: Something along the lines of "Ohtorii Party".




 List of Changes (not exhaustive)
-----------------------------------------------------------------------------

Fixed a rare bug in the original text routines
Fixed a text alignment error in stage 9 in the original
Original Japanese title screen logo was centered
User-configurable fonts and game mode (Battle Mania or Trouble Shooter)
The Vic Tokai screen was translated / subtitled two different ways
Text sprites in the recap animation were translated
The giant logo in the intro was expanded and translated two different ways
Two English title screens, one for each version
Minor fixes to the advertisement and options screens
Text routines were modified for 8x8 fonts
The entire game script was translated two different ways
Subtitled the logo that appears between certain stages (BMD only)
The English credits font is dynamically rotated
The credits were translated two different ways




 Transliteration Notes
-----------------------------------------------------------------------------

The following table shows how the various names were translated or
transliterated. The first column shows the original names while
the other columns represent the names used in the two translations.
They were based in part on the first game: Battle Mania / Trouble Shooter.


BATORUMANIA Daiginjou   Battle Mania Daiginjou  Trouble Shooter Vintage
---------------------   ----------------------  -----------------------
DON MORUGUSUTEIN *      Don Morgstein           Blackball
Ootorii MANIA           Mania Ohtorii **        Madison
MANIyan (nickname)      Mani-yan                Madison
Haneda MARIA            Maria Haneda            Crystal
PATCHI Taisa            Colonel	Patch           Col. Patch
KIKOKUSAI               Kikokusai               Pure Ghost Wail ***


* Due to technical limitations, the game spells this TEI, but it was written
in the manual as TE+I (little I).

** This spelling is for consistency with Battle Mania, where the "oo" in
Ootorii is romanized as "oh", which is an acceptable alternative.

*** A rough translation of the kanji that make up this name. A perfect
translation is absolutely impossible, of course. According to the
instruction booklet, Kikokusai is the character's given name; the full name
is Kikoku Kikokusai (surname first).

Please note that many of the above names are not actually used in the game
itself, so don't be surprised if you don't see them in the translation.




 Cultural Notes (not exhaustive)
-----------------------------------------------------------------------------

Baania (Vernier) 

The word "vernier" is sometimes used to refer to small rockets or other
propulsion devices used to make small adjustments to a flying object's
trajectory. The term as used in Gundam and other Japanese creations
seems to have a somewhat different meaning, however, but still refers
to a type of propulsion device. Here, it was translated as "jet pack".


Benten

Benten is a Japanese goddess associated with the island of Enoshima.
She originated in Hinduism and was introduced to Japan by Buddhist monks
while they were ruining Japan's indigenous culture. Also called Benzaiten.


Enoshima

Enoshima refers to both a Japanese seaside town and a nearby small island.
Aside from the Benten connection, which is not important to the story anyway,
there's not a lot to say about it except that it has nice beaches. Maria
wants to go swimming while they are there, but Mania is disappointed that
they don't have enough money left to buy much in the way of treats.


Gachapin

Gachapin seems to be a kind of spokesperson on Japanese television.
He is a green dinosaur that appears occasionally in cultural or
sports-related contexts. He is played by a person wearing a costume.


Food

There are many Japanese foods / restaurants listed during the credits.
Presumably these are places where the team dined during development.


Garage Kits

This term refers to hobby items, such as plastic models.


Heisei Babylon, 1995

This bit of text establishes the initial setting for the game. Heisei was
the contemporaneous name of the Japanese era, so the date is 1995 AD and
"Babylon" is the location. The short manga in the instruction booklet has
Morgstein telling Mania that he's waiting for her at "Heisei Babylon" and
goes on to explain that it refers to the offices of the Tokyo Government.


Inflatables

In the apartment, Maria is wearing a swim suit and carrying an inflatable
alligator (or some similar reptile), while the portrait shows her holding
an inner-tube. She's ready to go swimming at Enoshima.


Moon

Supposedly a reference to Sailor Moon. The sentence it is used in
is a parody of a line from one of the episodes, or so I've been told.


Tamegoro-

Tamegoro- is a pretend character (i.e. never actually appearing on the show,
much like Vern) from a 1960's television show called GEBAGEBA90Fun.
The phrase "atto odoroku TAMEGORO-" was often used during the show,
and it became something of a pop-cultural saying, although it's fairly
obscure today. It was spelled "Tamegoro" in the translation, but including
the "dash" is the correct way to write it.


Uterundesu

It isn't clear exactly what this is referring to. It might be a somewhat
obscure reference to some sort of comedy act, or it could be a misspelling
of utsurundesu. In the latter case it could refer to several things,
including a brand of camera or a manga. (The former is supposedly a play
on words of the same camera brand, if my information is correct.)
