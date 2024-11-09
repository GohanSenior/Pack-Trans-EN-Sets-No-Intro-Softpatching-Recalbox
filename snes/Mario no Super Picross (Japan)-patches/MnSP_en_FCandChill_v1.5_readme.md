[//]: <> (This readme is in the markdown format. Please preview in a markdown parser.)

# Mario's Super Picross: English Translation

## About
Mario's Super Picross is a Super Famicom game released in 1995 September 14th. It uses the engine (and even the same assets) of other Picross games that Jupiter flooded the market with at the time. Despite Nintendo's heavy marketing of the first Mario Picross Game Boy game outside of Japan, sales weren't great, therefore, future Mario Picross titles weren't released outside of Japan back in the day. Fast forward the Wii era, the game was released in Europe for the Virtual Console. In 2020, Mario's Super Picross was then released worldwide on Nintendo Switch Online. The catch: the game was still in Japanese! [The most Nintendo did was offer a translated tutorial on their YouTube channel.](https://www.youtube.com/watch?v=WOrZ07PVo5I) I'm only aware of a couple of changes to the re-releases which were applied on the fly with Lua patching. Firstly, three puzzles were changed probably due to copyright reasons. Additionally, the Virtual Console release stripped the audio data out of the rom due to Sony owning the patents to the SPC700 BRR format and its decoding. Nintendo, not wanting to pay up, opted on sound hacks instead. By the time the game came out on the Switch, the patent had expired.

## Development
There was previous talk in the community about how the game already had VWF despite being in Japanese. This would be one less thing to hack in. You occasionally had people begging for the game to be translated on places like Discord.

In mid 2021, I picked up the project because I wanted to translate one of the few Mario games that were still in Japanese. Also, I figured it would be easy, considering VWF was already in the game. However, the pointers were mostly all hardcoded (aside from the puzzle names). I had to locate all the pointers for all of the graphics and dialogue which were scattered about everywhere. Additionally, I cracked the compression format so I could insert custom graphics. The puzzle names were also embedded in other puzzle data like the puzzle animations. I had to adjust my script inserter to properly extract the puzzle names. Hacking the game wasn't hard, just tedious and would scare any novice hacker.

One thing you may notice when playing through this game is just how many Japanese culture references there are in it. You didn't know pig incense burners were a thing? Unfamiliar with Toyama no Kin-san? Well, now you know! Some stuff like "Teru Teru Bouzu" will have a brief parenthetical explanation on what it is (a ghost doll). Some Mario names have comments, but these were in the original game. I don't love having romaji in translations, but it's unavoidable without changing the puzzles. Fortunately, it's not too bad in this translation. You'll even learn about Japanese culture along the way!

I've read the seven reviews on the romhacking.net site (which by the way, is pretty insane to have on the first week of release), and I appreciate the feedback and the fact people really enjoy the translation! A couple of people commented on the katakana puzzles at the very beginning. Replacing the puzzles was something I considered. After realizing the puzzles spell "Mario's Picross" and the fact that there's plenty of other Japanese culture puzzles, I left the puzzles alone. Sometime in the future, I'll release my translation tools, which can assist in a hacker changing the puzzles as they see fit.

I realize that a lot of people have played this game on Nintendo Switch Online. If you would like to resume where you left off in your NSO play session, one option is to just play through the game again. Another option is to use the following cheat code to plow through the game:

```
C05E7B:EA
C05E7C:EA
```

With this code, after starting a puzzle, you'll instantly win. One side effect is that the completion time will be 00:00 so everyone will know you cheated!

The game's anniversary was last month at the time of this writing, which I unfortunately missed for this translation ~~([Nintendo apparently forgot about it too because they posted about the game only two days after the fan translation's initial release. Coincidence? Probably.](https://twitter.com/NintendoAmerica/status/1446535873764466690))~~. Oh well. Eventually, I want to release the translation's source code. However, considering this is a hot Nintendo item, I'm waiting a bit. Additionally, it probably won't include graphic data or script data because of Nintendo being Nintendo.

## Changes
* All graphics and text were translated (duh)
* The puzzle names in the original Japanese version used the VWF routine but had a hardcoded width. This logic was adjusted and the text centering logic was rewritten.
* The logo was expanded to cover more width. One side effect is that the tiles in the background are partially covered up. 
* The the logo on the menu screen was improved by expanding the palettes to better match the ones on the title screen.
* The font was slightly adjusted.
* Menus were expanded to fit more English characters.
* Text speed was increased for the milestone text (the Mario tutorial text was already at a decent speed)

## Support the Creators
If you like this game, consider supporting Nintendo by subscribing to Nintendo Switch Online or buying games from [Jupiter's Picross e series.](https://en.wikipedia.org/wiki/Picross_e)

## Changelog
* 2021 November 15th: 1.5
	* There's now a Nintendo Switch Online translation patch. Now you can enjoy puzzles that don't follow the difficulty curve... English!
	* An issue regarding the music selection menu was resolved. Later in the game, the amount of songs expands from 3 to 4. When adjusting the menu sprites, I didn't realize this, so the graphics didn't display the extra option.
	* Adjusted the logo graphics and tutorial graphic... again. I don't usually like improving games, but the the logo on the menu screen was improved by expanding the palettes to better match the ones on the title screen.
	* The SNES header adjusted by updating the version number and region. I was considering disabling the game's save file sanity check to modify the header's game code, but it would mess with save file cross compatibility between the original version and this fan translation.
	* Fixed a bug where the font was getting cut off after you solve a puzzle. This is because I extended some of the characters (`p` and `q` for example) in the font by a pixel. After corrupting the VRAM, it appeared the game was changing the tileset after a scanline. After discussing with people, some people thought the game was running on either Mode 5 or 6 and is switching modes mid-scanline. It didn't look like it was. As far as I could tell it was running on Mode 1. Some people thought it was writing to either BG12NBA or BG34NBA registers. As far as I could tell it was not. Some people thought it had something to do with IRQs. Again, as far as I could tell it was not. So what *was* the game doing and why? I honestly had no idea. After banging my head for hours setting breakpoints at registers, two generous people (oziphanto and blizzz) stepped up to the plate, downloaded the hack, and got their hands dirty. Turns out that because the BGMode was being modified by indirect DMA transfers, I wasn't seeing it changed via standard breakpoints. This can be observed by inspecting DMAs in the event viewer in MESEN-S. Once located, each value indicated in the event viewer can be searched in the memory viewer. What we find in the memory viewer would be data that would later be read by a DMA. From there, a breakpoint can be set to see how this data is being written. The logic to write to this area has been adjusted to display two extra scanlines of the font, just to be safe. For what it's worth, nobody but me noticed this. It was a great learning opportunity, so again, big thanks to oziphanto and blizzz.
* 2021 October 10th: 1.4
	* A handful of puzzle names were adjusted to fix the title casing, make the puzzle names more accurate to the picture, and use terminology more commonly used in English vernacular.
	* Start quote graphic in font adjusted.
	* There's some lines from Mario and Wario that I thought were unused / didn't know how to trigger. If you skip some puzzles, they give a message encouraging you to go back and complete them. The lines were cleaned up given this context.
	* You have "a 30 minutes" to complete each puzzle typo was fixed.
* 2021 October 8th: 1.3
	* Minor tweak to the text centering for puzzle names after a puzzle is completed.
* 2021 October 7th: 1.2
	* Fixed an issue where Wario's EX-K puzzle's name was not showing up. The text centering code was adjusted to allow for longer names.
	* Fixed an issue where the "の (No)" puzzle's picture was disappearing and some other puzzle animations weren't playing.
* 2021 October 6th: 1.1
	* Cleaned up the tutorial menu graphic.
* 2021 October 6th: 1.0
	* Initial release

## Credits
* FCandChill: Hacking, puzzle translations, graphics, script revision
* kumori#8931: Text translation 
* Senn: Kanji identification
* LuigiBlood#9296: Title screen feedback
* furrykef#4595: Onspot translation
* blizzz & oziphanto: Puzzle name bug fix
* togemet2: Was there
* Kajitani-Eizan#9804: Feedback
* kandowontu#2047: Feedback/beta tester
* blameitontherobot#7777: Original title screen gfx

## Bug Reporters
* supersonicjc
	* Wario's EX-K puzzle issue.
* svenge
	* Puzzle picture disappearing issue.
* Eldrethor
	* You have "a 30 minutes" to complete each puzzle typo.
* VVV18
	* Music menu selection issue