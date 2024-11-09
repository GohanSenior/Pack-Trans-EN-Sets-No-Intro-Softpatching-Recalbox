




                                  Pulseman
                         English Translation Patch




 History
-----------------------------------------------------------------------------

070226 Initial release




 Overview
-----------------------------------------------------------------------------

This is a translation patch for the Mega Drive game "Pulseman". As usual,
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
   the patching process.

   Another possibility is that you are using a PAL Mega Drive. This game was
   designed for NTSC systems and has known problems on PAL machines.


Q: Why is the text in Japanese?!?

A: This is a dual-language translation patch. If it detects that it is
   running on a Japanese system, it will use the original game script.
   If you are using an emulator, make sure the country code is set to USA.




 List of Changes (not exhaustive)
-----------------------------------------------------------------------------

Inserted uncompressed, pre-rendered data to replace the game's text sprites
Modified internal sprite structures to add text sprites and change parameters
Modified ending state machine so Lisa's mouth stops moving when she is silent
Slowed down the opening slightly to make the text easier to read
Minor changes to, and re-timing of, the credits
Rearranged the options screen slightly, as a consequence of the previous
An extra entry is now available for the map option
Disabled the console type check




 Hacking Notes
-----------------------------------------------------------------------------

This game appeared deceptively simple, with only 22 strings to translate.
However, it ended up requiring quite a bit of work; many a weekend was spent
on this translation.

One unusual aspect of this game was the fact that all of the Japanese text
was stored as tile data and displayed using sprites. This slowed down the
process considerably, as the translations needed to be rendered and converted
before they could be tested in-game. Since my method involved taking screen
shots of a modified version of a previous translation, which utilized a nice
variable-width font, it got quite irritating when changes needed to be made.
The whole pipeline had about a half-dozen steps, but ultimately it was less
of a hassle than it would have been to write a program for such a specific
task. On the plus side, storing the text as graphics data allowed me to
manually adjust the kerning to improve the appearance slightly, as well as
to squeeze in a few more precious pixels. Which leads to the next topic:
lack of room.

Since Japanese is a compact language, the authors of this game were able to
get away with only displaying two lines of 16 characters, sometimes less for
many of the strings. (Even so, the Japanese seems a bit terse at times.)
This presented a problem, however, as even with a variable-width font there
still wasn't enough room to display the translations without cutting them
down significantly. To fix this, the game's internal data structures had
to be replaced in order to add more sprites for most of the strings.

Another interesting problem was the decision about what to do with the text
that accompanies the English voice-overs. The Japanese subtitles don't match
the English dubbing, but are fairly close and don't change the basic meaning
of what is being said. Since it would have been distracting to have the
subtitles differ from the spoken dialogue, I was left with two choices.

The first (and most appealing) option was to remove the text during the
spoken parts. This would have saved me a lot of time, as the relevant
strings had some of the least standardized implementations as far as the rest
of this game goes. I was also intimidated by the fact that important tile
data was stored immediately after the text portion in the ending sequence,
which would require scattering the tile data elsewhere in the already packed
VRAM.

However, I decided that the second option, transcribing the English dialogue,
was preferable as long as there was enough room to display it all.
I reasoned that not everyone can understand spoken English perfectly,
especially when the sound quality is low, and some people may not be able to
hear the audio at all, for a variety of conceivable reasons. It turned out
that it was possible to display every spoken word, except one, so this option
was implemented. The one word that wouldn't fit was a leading "however",
so leaving it out wasn't a big deal.

As usual, the obsessive drive toward "perfection" prompted some additional
hacking, the results of which are partially described elsewhere in this
document. Including the usual drudgery of documentation, play testing,
and so on, this project ended up taking a lot longer than one might expect
from the seemingly small amount of text that was translated.


Although this is the first English patch, it is not the first translation
of the game, as there was already a French version by the Terminus group.
I have not examined it in detail, but it appears to overwrite the graphics
data directly, unlike my patch which modifies the code to load the tile data
into VRAM when necessary. This means that they were able to recompress the
data in a format that is compatible with the game's decompression algorithm,
which is quite impressive. It does not appear to modify the code at all.
