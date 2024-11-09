




                                 Gleylancer
                         English Translation Patch




 History
-----------------------------------------------------------------------------

061023 Initial release
070809 Second release (no changes, patch version is still 061023)




 Overview
-----------------------------------------------------------------------------

This is a translation patch for the Mega Drive game "Gleylancer". It is yet
another "dual-language" patch, meaning that it supports both Japanese and
English, depending on the country code of your machine (real or emulated).
It uses a true variable-width font and remixed music. (For an explanation of
why the latter was necessary, read the hacking notes later on in this file.)




 Applying the Patch
-----------------------------------------------------------------------------

Hopefully included with this document is a patch file in the IPS format.
You can use any program that supports this file format to apply this
translation patch to your ROM file.




 Playing the Game
-----------------------------------------------------------------------------

Once you've patched the ROM file, simply load it up in your favorite
Genesis / Mega Drive emulator, console copier, or flash cartridge.

The game will detect the country code of your machine (real or emulated) and
then switch to English or Japanese mode accordingly.




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

   Another possibility is that you are using a PAL Mega Drive; this game was
   designed for NTSC systems and I didn't make any changes in that respect.
   It should still run (probably at the wrong speed), but you never know...


Q: Why is the text in Japanese?!?

A: This is a dual-language translation patch; if it detects that it is
   running on a Japanese system, it will use the original game script.
   If you are using an emulator, make sure the country code is set to USA.


Q: Why aren't the credits translated?

A: There are two versions of the credits: one in English and one in Japanese,
   depending on which ending you got (this is how the original game works).
   The Japanese credits were not changed, out of respect for the authors of
   this fine game.




 List of Changes (not exhaustive)
-----------------------------------------------------------------------------

Corrected a minor error in the original Japanese script
Centered Japanese credits properly
Variable-width font support added
Modified the palettes to increase the number of colors for the font
Remixed the opening music theme slightly
Re-timed all the text




 Transliteration Notes
-----------------------------------------------------------------------------

All the character names (with one exception) were transliterated the same way
that they were written in the manual (in English).


KEN*KYABUROKKU  Ken Cabrock
RU-SHIA         Lucia Cabrock
RU-SU           Rues
TE+IMU          Teim *
EDE+I           Eddy

OBERON          Oberon
TE+ITANIA       Titania
EARIERU         Ariel
KO-MORAN        Cormoran **
KA-N*GARUVA     Carn Galva ***


* This was spelled "Tim" in the manual, but that just doesn't work as a
female name, so I spelled it "Teim", which is also how this same name (for a
female) is rendered in the English translation of Phantasy Star II, thus
providing of a helpful precedent.

** This is probably intended to refer to the cormorant bird. However,
"cormoran" is a legitimate alternative, so I decided to spell it that way
because it better represents what was actually written.

*** This is pretty obscure, even in English. It's the name of a place
in Cornwall. There is a legend about a giant associated with it.
A book was written about the subject in Japanese.

You may also be interested in knowing that Oberon, Titania, and Ariel are
all Shakespearean fairy names and that Titania is Oberon's wife.




 Hacking Notes
-----------------------------------------------------------------------------

Remixed music in the opening was a necessity because the story is divided
into five distinct sections and the music is synchronized to each of them.
While this is a great feature, it has the unfortunate consequence of forcing
all the text in each scene to be printed within a certain period of time.
It was impossible to fit the English translation into the allotted time
periods, and even the original Japanese script seems a bit rushed in places.
I changed the timings to make the English text readable and then remixed
the music to provide a few more precious seconds of time with which to
display the text.

Even with the extra time, it took lots of tinkering to make sure everything
was properly synchronized and could still be read comfortably. The intro
still goes at a pretty fast pace in places, but hopefully most people will
be able to read it. Unfortunately, there are limits to what I could do with
the music; it could not be extended indefinitely.

The "remix" should be indistinguishable from the original, unless you are
very familiar with the tune or are systematically comparing them. It mostly
involved repeating a few musical phrases here and there. Very little
creativity was involved, although I did consider expanding the PSG tracks
at one point.

The whole remix process took an entire three-day weekend as I had to reverse
engineer the music subsystem and write some special tools. Analyzing the
music data also took up a lot of time. On the plus side, however, I was able
to discover and fix an error in the original score. The mistake was evident
based on the timing analysis and by comparing the notes with those played on
another track. The mistiming wasn't too obvious in the original anyway, but
it was fixed in my version.

Be warned that none of the emulators I tested during development had
perfect timing. The opening music would get out of synch by a second
or two, as compared to a real Genesis / Mega Drive.

Some similar sound issues were involved with the ending / credits, which are
spaced in such a way that the last musical phrase occurs as the credits
stop rolling. The music was not changed, in this case, but getting the
translated "bad" ending synchronized was quite a hassle.

This was only intended to be a little side project while working on Battle
Mania Daiginjou, but perfecting it ended up being a fairly complicated task.
