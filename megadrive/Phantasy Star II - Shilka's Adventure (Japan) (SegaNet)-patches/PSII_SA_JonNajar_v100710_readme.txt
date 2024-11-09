




                    Phantasy Star II: Shilka's Adventure
                         English Translation Patch




 History
-----------------------------------------------------------------------------

070712 Initial release
070808 A script correction, thanks to Bernd
080628 Minor translation fix & changed a name (thanks to Ruben van Ophuizen)
100710 Script rewritten, code updated, minor graphics fix, a few bugs fixed




 Overview
-----------------------------------------------------------------------------

This is a translation patch for the Mega Drive Sega Net game entitled
"Phantasy Star II: Shilka's Adventure". It sports a variable-width font
engine with kerning and, as usual, it is a "dual-language" patch, meaning
that it supports both Japanese and English, depending on the country code
of your machine.




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
then switch to English or Japanese mode accordingly.




 Q & A
-----------------------------------------------------------------------------

Q: This patch doesn't work! What do I do?

A: Make sure that your ROM file is not in an interleaved format. It's also
   possible that there is more than one version of the game, or that your
   copy is corrupt.

   Some emulators may also fail to run the program. Please make sure you try
   several of the most up-to-date emulators available.


Q: It doesn't work with my copier / flash cartridge! Why not?

   This was tested on a real Genesis so you shouldn't have any problems in
   that respect. The most likely reason is that something went wrong during
   the patching process. See the previous question and try it in an emulator
   to see if that works.

   Another possibility is that you are using a PAL Mega Drive. This game was
   designed for NTSC systems and I didn't make any changes in that respect.
   It should still run (probably at the wrong speed), but you never know...


Q: Why is the text in Japanese?!?

A: This is a dual-language translation patch. If it detects that it is
   running on a Japanese system, it will use the original game script.
   If you are using an emulator, make sure the country code is set to USA.




 Translation/Transliteration Notes
-----------------------------------------------------------------------------

The surnames are simply omitted, since there is no way to tell for sure how
to properly transliterate/translate them.

The katakana renditions are available at various places online, for the
curious, but don't trust their transliterations. For example, "Kinds" is
commonly misspelled as "Kainz", even though the latter is the most logical
transliteration. So you can see why it's impossible to tell for sure.

ERIOSA-RU was rendered as Eli Ossale. Ossale Kohta is a pseudonym for famed
Sega developer Kotaro Hayashida, and he writes the first part in katakana
as OSA-RU. It is not clear whether this was intended to be one word or two,
and the first part of the name could be written several different ways.

(Thanks to Ruben van Ophuizen for pointing out the connection.)

Astute readers may have noticed that some of the monetary values in the text
have changed from older versions. The literal values were divided by 100 in
order to keep the currency system roughly consistent with the other games.

Meseta (the Phantasy Star currency) more closely match a dollar system
whereas the author of Shilka's Adventure seemed to be treating them like
the Japanese Yen (which is roughly equivalent to a cent, exchange rates
not withstanding), hence the decision to adjust the values to keep the
numbers more in line with the other games.




 Hacking Notes
-----------------------------------------------------------------------------

Nothing interesting (fortunately). The usual techniques were employed and old
code was modified and reused. The variable-width font engine was upgraded to
handle groups and triplets (possibly a new invention in kerning technology).

Other than that, there's not much to say here, except a very special thanks
to a very special guest.
