




                               Langrisser II
                         English Translation Patch




 History
-----------------------------------------------------------------------------

080812 Initial release
081106 Improved ending sequence timing/animation, other improvements
091211 Minor corrections, thanks to Alexander Landgren
100626 Fixed shop points display. Thanks to someone for finally reporting it.
110527 Corrected hero name collision checker bug, thanks to Lady Abaxa
110701 Fixed Game Over window (broken by new feature), thanks to Artur Khokh




 Overview
-----------------------------------------------------------------------------

This is a translation patch for the Mega Drive game Langrisser II.
It is the sequel to Langrisser (known as Warsong in the USA) by Masaya.
As usual, it is a "dual-language" patch, meaning that it is capable
of displaying the original Japanese script in addition to the English
translation, depending on the country code of your machine.

It is loosely based on the older Hiryuu Honyaku / Warui Toransu translation.
A few improvements to their original work were made by D et al. before he
passed it along. Aside from the script and a few graphics, almost nothing
was taken from the old release. The hacking was completely redone from
scratch and is far superior. The script was almost entirely rewritten,
edited, and type-set, with quite a bit of it retranslated.




 Applying the Patch
-----------------------------------------------------------------------------

Hopefully included with this document is a patch file in the IPS format.
You can use any program that supports that file format to apply this
translation patch to your ROM file.

This patch is only compatible with the "Revision 02" version of the game.




 Playing the Game
-----------------------------------------------------------------------------

Once you've patched the ROM file, simply load it up in your favorite
Genesis / Mega Drive emulator, console copier, or flash cartridge.

The game will detect the country code of your machine (real or emulated) and
then switch to English or Japanese mode accordingly. The Japanese option
does not apply to every facet of the game, mostly just the in-game script.




 Q & A
-----------------------------------------------------------------------------

Q: This patch doesn't work! What do I do?

A: Make sure that your ROM file is not in an interleaved format. It's also
   possible that there is more than one version of the game, or that your
   copy is corrupt.

   Some emulators may also fail to run the program. Please make sure you try
   several of the most up-to-date emulators available.


Q: Why is the text in Japanese?!?

A: This is a dual-language translation patch. If it detects that it is
   running on a Japanese system, it will use the original game script.
   If you are using an emulator, make sure the country code is set to USA.


Q: What is the main character's official name?

A: Erwin and Elwin are the two most likely candidates. One can make a good
   case for both of them, but there is no way to know what Masaya intended.
   If it matters to you, D uses the former, and HH/WT the latter.

   The name entry option is fully supported, so use whatever name you prefer.


Q: Why can't I name the hero after myself?

A: If your name is Keith or Scott or something then you've encountered
   a feature of Langrisser II that prohibits any names which match the
   game's  master list of characters. A few hundred dollars in court fees
   will take care of the problem.


Q: Why can't I give the hero a humiliating name like "Villager"?

A: You can, you just have to use a different capitalization scheme.


Q: No variable-width font?

A: It's there in a few places, but D requested that a specific font be used.
   (Something about giving the game a Warsong feel.)

   This turned out to be a wise decision, as it sped up the development
   process significantly, and made type-setting much easier. It would
   have delayed this release for many months if another approach was used.


Q: Why does the ending look like an old dubbed Japanese monster movie?

A: Not only did Masaya animate the mouths and eyes of two of the characters
   in the ending, they also tried to design each mouth animation to match
   the actual words being "spoken". So the animation will necessarily last
   longer than the text printing sometimes because they are independent.
   This is an intentional feature of the Japanese version and has nothing to
   do with the translation, which uses a new set of animations to match the
   English text anyway.

   One deficiency in the English version is that not much effort was put into
   trying to pick the best animation frames to match the English wording; the
   main concern was making sure that the animation lasted approximately as
   long as an informal narration. In other words, the text was read aloud
   and the animation resequenced to end at the same time, but only some of
   the frames were modified to better reflect the actual shape the mouth
   would be making. Since most people will be reading the text rather than
   lips, this was deemed acceptable -- it is not easy to design animations
   when you are given a very limited set of frames to choose from that were
   intended for a different language.

   It's also worth mentioning that the music was scored to last just as long
   as the Japanese text, which is why the text speed is a little faster than
   would have been ideal. If you take anything away from this, it should be
   that Masaya commendably paid a great deal of attention to the details of
   a small section of the game. If they had scored the music sloppily and
   left out the animation entirely, few people would have noticed.


Q: What's with that weird "aniki" scenario?

A: It's a tribute to the Chou Aniki series of games.




 List of Changes (not exhaustive)
-----------------------------------------------------------------------------

Opening translated
Title screen replaced (slightly modified from older version to fix a glitch)
Accented characters added to font (for Lána, Krämer, Böser)
Name entry fully supported
Graphics bug fixed on route screen (hard to see in original Japanese version)
All menus completely redone
Secret scenario prefix changed from ? to X
Speed hacks (entering the shop is several seconds faster)
8x8 names expanded to two rows, very few abbreviations needed
Script is fully translated, with dual-language support
Text window is now dynamically resized
A few portrait selections were corrected
Special dialogue during ending enabled? (original Masaya bug?)
Ending and epilogues translated
No ROM expansion




 Translation Notes
-----------------------------------------------------------------------------

As mentioned above, this is a heavily rewritten edition of Hiryuu Honyaku /
Warui Toransu's script. Tomato, at great personal risk, provided reams of
high-quality epilogue translations that were not available in older versions.

Warui Toransu literally means "bad translation", and that humble name was
sadly well-chosen in this case. (Note that Hiryuu Honyaku also participated
in the original translation, not just Warui Toransu.)

Objectively speaking, the original script had serious problems with accuracy
at times. These mistakes were often clearly not the result of paraphrase,
which is more subjective and harder to criticize, but rather guesswork and
inexperience. While some of the translators knew what they were doing and
produced accurate translations, others seemed to lack even basic knowledge
of Japanese and were consistently wrong on almost every string.

However, I suspect I received an older draft and that later (i.e. published)
versions of the script were better.




 Hacking Notes
-----------------------------------------------------------------------------

The other translation did not appear to use any assembly-level hacking, which
severely restricted what they could do with the game and had some unfortunate
side-effects such as requiring the ROM to be expanded, which is anathema to
me (all my translations fit within the original file size, even with dual-
language support.) This version makes extensive use of code modifications,
with around 60 subroutine hooks and probably hundreds of in-place fixes.
This ended up being a lot more work than expected, and is probably the most
extensive hacking job I've done so far. For comparison purposes, the earlier
King Colossus and Yuu Yuu Hakusho only had around 40 subroutine hooks each.

One of the major improvements over the HH/WT version is that most of the
name/class abbreviations were eliminated by using both 8x8 rows. The
results are much cleaner looking.

The hacking was accelerated by the fact that a monospace font was used for
most of the menus and things. A nice side effect of this was that the kanji
tile pre-loading could be eliminated, which sped up certain transitions
noticeably. Variable-width font rendering can still be found in a few places,
such as the intro and ending, but it was not feasible to use it for some of
the menus due to an inability to balance the trade-offs. Therefore, it is not
used in most places simply for consistency and/or convenience.

One of the more interesting features added is the dynamic window resizing.
The window height is adjusted based on the number of lines actually needed
for a given page. This was moderately difficult to implement, but ended
up looking quite nice. The trick was getting it to work without any flicker
or other jarring effects.
