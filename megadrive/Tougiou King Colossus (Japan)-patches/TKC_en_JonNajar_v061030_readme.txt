




                               King Colossus

                         English Translation Patch




  History
-----------------------------------------------------------------------------

061030 Works on a real Genesis now. Script revised slightly.
060114 Fixed checksum error introduced in the previous release.
060108 Now works with a hacked version of the ROM file.
051203 Fixed a compatibility problem. Q & A section updated.
051123 Initial release.




 Overview
-----------------------------------------------------------------------------

This is a translation patch for the Sega Mega Drive game "King Colossus".
It was probably the first "dual-language" (i.e. supporting both Japanese
and English) fan translation of a video game.




 Applying the Patch
-----------------------------------------------------------------------------

Hopefully included with this document is a patch file in the pretentiously-
named IPS format. You can use any program that supports this file format
to apply the patch to your ROM file.




 Playing the Game
-----------------------------------------------------------------------------

Once you've patched the ROM file, simply load it up in your favorite
Genesis / Mega Drive emulator, console copier, or flash cartridge.

Since this is a dual-language game, you must set your emulator's country
code to USA to play it in English. If you want to play it in the original
Japanese, set the country code to Japan. Note that in this mode it will
not be identical to the original Japanese version; the windows are larger,
some bugs have been fixed, and many name limitations were changed.
Also, some of the non-script text will still be in English.




 List of Changes (not exhaustive)
-----------------------------------------------------------------------------

Name limit increased from 4 to 8 bytes ([han]dakuten characters take 2 bytes)
Changed various string size limitations
Added or changed several glyphs in the font
Added a new control code to make use of the last line of text w/o limitations
Increased the size of the normal text window
Increased the size of the location name window
Increased the size of the arena rankings window
Increased the size of the weapon rental window
Arena rankings now have an appropriate suffix (i.e. "1st" instead of "No. 1")
Many modifications to the name entry screen:
 Lower-case characters can now be used
 Starting location changed
 All kana characters are still available
 Added katakana 'VU' (voiced 'U') just for completeness
Many modifications to the pause menus:
 Changed the size and location of the windows
 Translated the text
 Fixes to the window movement and overlapping
Workaround for unlimited string bank sizes
Subtitled the kanji in the opening credits
Fixed some spelling errors in the ending credits (required additional fonts)
Auto-detects the country code and shows English / Japanese text accordingly




 Transliteration Notes
-----------------------------------------------------------------------------

When transliterating names I normally took a direct romanization and then
tried to make it look and sound better for English speakers. I generally
used whichever I felt was the better choice for the r/l, b/v, and s/th pairs
and dropped extraneous vowels. Occasionally the letter 'h' was used to help
clarify pronunciation and 'ph' was often used in place of 'f'. Finally,
once or twice I replaced long 'a' vowels with 'ar'. Other than that, I
rarely changed the vowels, so they should generally be given a Japanese
pronunciation, if you know how. This even applies to 'oo', which is NOT the
rather ill-conceived romanization of 'ou' but represents 'o-'.

The following names were translated, rather than simply transliterated,
and should be pronounced as in English

 DEZAIA   Desire
 SHIRIOSU Sirius
 GANI-ME  Ganyme(de)
 KURISU   Kris

...and some that are (probably) French (pronounced as in English, however).

 ROA-RU   Loire
 PARISU   Paris

Finally, it wasn't clear whether or not they meant Orpheus for this one, as
the pronunciations are significantly different, so I just transliterated it.

 ORUFESU  Orphus

That was one of the few vowel changes; I didn't like "Orphes" or "Orfes".
And speaking of vowel changes, here's the other major one:

 KARURIMU Carleem

As with Orphus, I imagine most people would instinctively give the word
the correct pronunciation, based on the way it looks.

Oh, and yes, Iria is the exact romanization for that particular name.




 Hacking Notes
-----------------------------------------------------------------------------

This hack required a lot of work. I had to do quite a bit of disassembly
and ended up getting pretty familiar with the inner workings of the code.
It took about two weeks of full-time (all day, every day) hacking, not to
mention a few days worth of minor bug fixing and adjustments during the
translation phase.

One of the more annoying aspects of this translation hack was the excessive
amount of inlining and hard-coding employed by the original programmers.
For example, the code for the save menu uses the same value hard-coded
in six different places. And from a quick look at my patch source file,
I can see that those changes only amount to about half of what needed to be
changed for that particular menu, not including the hooks into my assembly
language subroutines. Another example is that there are probably half-a-
dozen text decoding routines, all with minor variations. And simply
changing the size of a window was never sufficient; there were always two
to six subroutines for actually rendering that specific window that needed
to be changed as well.

Attention to detail ended up requiring many additional days of work. It is
difficult to convey the amount of effort it took to get everything "perfect".
The pause menus alone took around half of a week to finish, as so many things
had to be changed, even the way the windows scroll. Many of the things I
fixed probably would not even have been noticed, but I am something of a
perfectionist; I could have taken the easy route and not bothered to increase
the window sizes and string length limits, which probably would have saved me
a week of overtime hours working on this hack.

Another problem was the overuse of buffers. I had to fix several buffer
overflow errors cause by the increased size of the strings. In many cases
there was no practical reason for some of the strings to be copied to
memory (or sometimes even the cartridge RAM!) Rather than increasing the
size of the buffers (and risking address conflicts), I used some clever
code hacks to increase the limits without changing the sizes of the original
buffers.

On the positive side, the credits and the game-over screen were already
in English, although I still ended up having to fix a few things. The
ending credits were particularly annoying because of the variable width
font; I had to make some additional character combinations in order to
correct their English.

So far I've found at least four different compression schemes used in this
game; it seems like every kind of data has its own compression method.
I didn't bother trying to recompress anything as there was plenty of free
space left in the ROM. I ripped all the decompression code, which came
in handy several times.

My code is usually pretty efficient, but you might notice some seemingly
unnecessary stuff. The reason is because I always try to be as careful
as possible when patching foreign programs, so there is some code in there
to emulate calculations that my subroutines didn't need. I also refused to
trash any registers unless the original code was obviously doing so
immediately after me. Even the upper word of data registers was preserved,
and if the original programmers felt it necessary to clear an entire
register, so did I. In my opinion, it's not worth the risk of introducing
subtle bugs just to save a few bytes or make the program run unnoticeably
faster.

Sadly, there was one thing I missed and that was the fact that certain
control codes mixed in with some of the strings are read as words instead
of bytes. This can cause misalignment errors, a misfeature of the 68000
which will crash the game on a real console and can cause problems on
some emulators. The original developers handled this by inserting a dummy
byte for alignment purposes, when necessary, but this was a very poor
solution to the problem. Since my emulator completely ignored misaligned
accesses, I was unaware that some of my translated strings had the control
codes in the wrong places.

Alignment errors are an amateurish mistake, so that was quite embarrassing,
although the way it occurred in the data could have been missed even by
an expert. The only practical difference between the first and second
release is that a few of the strings were padded for alignment purposes.




 Consistency Notes
-----------------------------------------------------------------------------

Much of what I've written could be construed as advice to other hackers
and translators. With that in mind, here is a partial list of the
consistency checks I performed after the script was translated and edited.
Inconsistencies often go unnoticed, but eliminating them makes your work
look much more professional.


	all proper names
	inconsistent stuttering (search for '-')
	inconsistent capitalization of names. For example...
	 Castle <X> but "the castle of X"
	 King <name>, else king (lowercase) (same with prince(ss) and queen)
	 "The" (e.g. The <name>) vs. "the"

Inconsistent alternate spellings
	Goodbye vs. Good-bye (both are considered correct, at least by some)
	OK Ok ok okay
	(For the next two, I use both spellings for their different nuances)
	alright (more of an expression) vs. all right ("allright" is wrong)
	anytime vs. any time
	anymore (from now on, at present) vs. any more (additional meanings)

Spell-checkers can't catch typos that are correctly spelled
	your you're
	it's its
	their there they're
	were where we're
	then than

	unintentional double spaces
	comma not followed by a space
	repeated words (e.g. the the) (make sure the spell-checker does this)
	that that (not all spell-checkers check this; it can be legitimate)
	repeated words between lines (line breaks can mess up spell-checkers)

There are many, many more homophones (as well as homonyms and homographs)
in English, but there isn't much point in listing them; I only included
the most common ones that I could think of.

Some of those checks require manually searching for and checking every
instance of a word, which can be tedious. All in all, I probably found
less than half-a-dozen typos or inconsistencies during this phase, but
that was after lots of editing.


"How to Stutter Correctly"

Right       Wrong    Sound
-----------------------------
W-Who	not Wh-Who  (hu sound) (note the irregularity of this one)
Wh-What	not W-What  (wh sound)
Th-This	not T-This  (th sound)
Sh-She	not S-She   (sh sound)
Th-That not Th-that            (watch out for inconsistent capitalization)
I, I    not I-I                (personal pronoun 'I' is a special case)
I, I'm  not I-I'm              (same with 'd, 'll, etc.)
I-It    not I, It   (ih sound)




 Original Bugs
-----------------------------------------------------------------------------

These are all the bugs in the original game that I have found.

Note that there are a few minor plot spoilers in this section.


In the very beginning, if you try to leave the room before talking to Muuk,
the color of the text will be wrong. This is a bug in the game flow, not the
script, and is not trivial to fix.

There's another one at the end of the first chapter, when Muuk speaks
to Flora as you are leaving.

Before you fight Desire, her text is green at one point.

It's actually not an original bug, but there is a slight textual error
during the "second audience" scene. You probably wouldn't notice it, even
if you were looking for it, and it was necessary to make the text appear the
way I wanted it.


The statues in the shrine will give you garbage messages if you return
there later on. Sometimes they'll give you real messages too; the game is
reading the right string number in the wrong bank. Actually, sometimes it
will read from the correct bank, which might explain why this bug went
unnoticed.

I fixed some of the garbage by adding extra strings to one of the banks that
it reads from, but I couldn't do this for the other bank because there was
already a string assigned to that number. Hence you will get to read part
of the ending.

As with the color errors listed above, there's no easy way to fix this
because the error is probably in the game's data, which is likely compressed,
and would require a lot of reverse engineering. Since there is no reason
to go back to that area anyway and since most people probably don't know how
to retrigger these messages, I didn't think it was worth the time to try
fixing this bug.

Everyone in Sirius gives garbage messages later in the game. Once again,
the strings are being read out of the wrong bank. I was able to fix the
strings for everyone except the dead guy; his string is the same as the
old man's, so there's nothing I can easily do about that.

Update: talking to anyone in Sirius later in the game will also screw up
the messages for just about everyone else! To fix this, talk to anyone
in Distaria or get the "gate is firmly shut" message in Distaria Coliseum.
As with all of the above, this is an original bug and I'm not inclined
to try fixing it. Based on what I know, the problem is probably in the
game's data, and it could take weeks to figure out how the internal
structures are arranged. I'm less enthusiastic about fixing other
people's bugs than my own.


When there is more than one color of text being displayed simultaneously,
all the text will be the same color as the last one used, when the lines are
scrolled out of the window. My script has been arranged to avoid this.

Moving off of "other items" onto a valid item won't print the string.
You can't normally get enough items to do this anyway, so it's no big deal.

The pause menu is too short and the sword pointer overlaps part of it.
The original game designers didn't seem to care, and fixing this would be a
lot of trouble due to the way the menu is rolled up and moved around.

In the ending, it looks as if some of the scenes are cut off. This was
intentional; if you pay attention, you'll notice that each scene shows
less and less on both the top and bottom. Quite an interesting bit of
direction, especially considering that it's a game, and an old one at that.


 ---------------------------------------------------------------------------
| The rest of these are things that probably wouldn't get blamed on me,     |
| but have been documented for your interest anyway.                        |
 ---------------------------------------------------------------------------


Sometimes sprites will change position slightly during the cutscenes.

It is possible to get a character who is following you (but not closely)
to walk through solid walls.

It is also possible to attack through solid walls.

The way the game handles tile overlays (i.e. either on a second plane or
using sprites) isn't perfect. You can occasionally see parts of your weapons
appear when going through an underpass. You can also see similar effects
if you jump in certain places, such as the first cave.

It is possible to place the Lost Eyes in the statue without triggering the
message. The door opens, however, and you can elicit the message later,
if you want.

In Kazard, it isn't necessary to light the torches if you jump correctly.
It isn't a big help and it might have other consequences, so I wouldn't
recommend skipping that part. Also, once you jump to the other side, it's
possible to enter the king's chamber by jumping diagonally on either side
of the walkway near the door. This is absolutely no help, since you can
just walk through the door once you're across, but it's interesting.

In Lufelia, some of the sword pointers in the pause menu are gray, while
others are not.

It's possible to get trapped in Ganant's hidden room if he isn't there to
send you back out. You can't save, so if you don't have enough MP to cast
Exodus there's nothing you can do.

There's a fake passage in Lina's room later in the game. It seems to be the
same as in the dragon cave; there's a hole in the wall, you just can't enter
it. Also, earlier in the game it is possible to get underneath the throne
in that room.

The ending credits are cued to the music, so they don't start for quite
a while; the game has not crashed.




 Q & A
-----------------------------------------------------------------------------

Q: This patch doesn't work! What do I do?

A: Make sure your ROM file is not in an interleaved format. It's also
   possible that there is more than one version of the game, or your copy
   is corrupt.


Q: Why is the text in Japanese?!?

A: This is a dual-language translation patch. If it detects that it is
   running on a Japanese system, it will use the original game script.
   If you are using an emulator, make sure the country code is set to USA.


Q: Are state files from the original Japanese version still compatible?

A: No. They may work partially, but some stuff will definitely be missing.
   Ideally, you should save your game on the original version and use that
   same SRAM file for my version of the game, as saved games should still be
   compatible.


Q: Why is everyone giving me messages from earlier in the game?

A: You went back to Sirius, didn't you...
   This is a bug in the original. I wrote more about it elsewhere in this
   file, but to fix it all you need to do is talk to anyone in Distaria, or
   attempt to enter Distaria Coliseum. Once any of these correct messages
   are displayed, everything will be back to normal.

   To avoid triggering this bug in the first place, don't talk to anyone in
   Sirius after you finished the Lufelia area. Not that they have anything
   interesting to say anyway...


Q: I see "s's" in your translation. Don't you know that you're supposed to
   leave off the 's' of possessives for proper names which end in 's'?

A: Although that practice is common in journalism, many authorities
   discourage its use.


Q: You put a comma after the final element in a series. Don't you know that
   you're not supposed to do that anymore?

A: Yes, that's what my elementary school teacher said as well. However, as
   in the previous case, this is "newspaper grammar". It can cause ambiguity
   and it removes a valuable visual cue, just to save a little space.

   Perhaps you too might come to believe that some of the rules of English
   that you were taught (like the prohibition against ending a sentence with
   a preposition, for example) are actually questionable.


Q: Who is Makoto Ogino? Is this based on a manga?

A: Makoto Ogino is the author of the manga "Kujaku Ou", which translates as
   "Peacock King". Based on what I've read of the game box and instruction
   booklet, it seems Makoto Ogino was brought in to direct and write the
   script for King Colossus, or "Tougi Ou". I am confident that it was a
   completely original work.


Q: Why does my character's name get truncated sometimes?

A: The name buffer is eight bytes, but the (han)dakuten characters (the kana
   with accent marks) take up 2 bytes each, so it will truncate your name if
   necessary. If it does, you will see the truncated version in the
   confirmation window, so pay attention. If you are only using Romaji
   (i.e. English) characters, as most people are likely to do, your name can
   be up to eight characters long and will never be truncated.


Q: What is the main character's default name?

A: There isn't one. The instruction booklet refers to him as "the hero of
   the story", or something like that. In the original game, if you select
   "END" without entering anything, you get four blank spaces for a name.
   This was fixed; now it is impossible to have a completely blank name -
   you will get a katakana placeholder name instead.


Q: I don't want to read your translation carefully. How can I speed it up?

A: In addition to the normal speed-up activated by holding the C Button,
   you can hold down any direction on the D Pad to skip the pauses as well.


Q: Is it OK to say "no" to people?

A: Yes; if you want to give the obvious wrong answer to any of the "yes or
   no" questions in the game, go right ahead - it doesn't appear to have any
   drawbacks and you'll get to see their reactions. As with many games, the
   plot won't continue until you give the correct answer. The only exception
   is at the end of the game: your answer determines the ending you will get
   (and they are merely different; there is no "good ending").


Q: What is "Demiglace Sauce"?

A: It's a French term for a type of thick sauce.


Q: What about the "Shura Sword"?

A: 'Shura' doesn't translate well, particularly as the name of a sword.
   It definitely connotes violence, however. It is written using the same
   kanji as the word Ashura.


Q: And what do the kanji on the title screen mean?

A: They are pronounced "Tougi Ou", which I translated within the game as
   "King Colossus". Therefore, the title screen is already "translated".

   I considered subtitling it, like I did with the opening credits,
   but I couldn't get it to look good; it either obscured the background
   too much or had an odd-looking location.


Q: I can't enter Castle Lufelia! What do I do?

A: Even though Lufelia dramatically appears on the map, you're not supposed
   to go there yet. In case you weren't paying attention, first you must
   go to Kazard, which is east of Sirius (although you might not have known
   that, since it was previously "unselectable" or because you couldn't read
   the map in the instruction booklet).


Q: Shields don't increase my defense, so what good are they?

A: They can block certain attacks. When you aren't attacking, your shield is
   raised. It comes in handy sometimes.


Q: Is it possible to get all the items?

A: Not the _item_ items, but all the equipment, yes. Assuming you didn't
   miss the articles in places that can never be returned to...


Q: Shouldn't that guy's name be "Orpheus"?

A: It's possible that they were alluding to Orpheus, but the fact remains
   that the pronunciation is significantly different. Furthermore, Orphus
   in this game has very little in common with the mythological Orpheus.
