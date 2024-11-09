[//]: <> (This readme is in the markdown format. Please preview in a markdown parser.)

# Tensai Bakabon (Sega Master System): English Translation
Source code: [https://github.com/romh-acking/tensai-bakabon-sms-en](https://github.com/romh-acking/tensai-bakabon-sms-en)

## About
I was approached by a friend, cccmar, about the potentially working with him and TheMajinZenki on translating this game in late December. Both had their eyes on it for awhile, as it's essentially the only remaining notable untranslated game on the system (I wouldn't really call Brazilian shovelware games notable). The game's quirky atmosphere intrigued me, so I accepted the offer.

Tensai Bakabon is apparently a highly requested game to be translated... well, as highly requested as you can get for a niche console. [The first translation attempt for this game started in 2008](https://www.smspower.org/forums/11498-TensaiBakabonTranslation), but was quietly cancelled. Despite this, their notes on the SMS Power forum made starting the project more approachable. So I'm thankful for the thread existing.

My main concern was being able to dump all the text properly. Not because it was difficult but because the easiest method was tedious. Pointers are stored in (what I assume to be) a scripting language. I discovered where to set an execution breakpoint that allows for pointer locations to be extracted easily (it's `0x101D`, in case you're curious). cccmar surprisingly stepped up to the plate and located the large majority of them, which I am very thankful for. With that done, the project started going places.

This is my first experience making Z80 assembly language patches. It's also my time implementing a variable width font hacks. Coding in Z80 assembly is quite unintuitive coming from 6502 assembly, but over time, I came to understand how to manuever the language. Let us know if you spot lines we missed. The dialogue decompression buffer was relocated in RAM to be above important registers. This isn't a problem, unless the data loaded in is very huge. So if you encounter a non-repointed pointer, a lot of invalid data will probably be read, which will overwrite important registers and crash the game.

Testing the game was kind of a pain as it required cccmar and I to discover every possible way to trigger lines, some of which are very obscure. There's text that pops up when your inventory is full, when you don't have enough money, etc. that had to be accounted for.

This game is rather text heavy and this project is the only translation project for this system to leverage VWF hacks. You could say this ends the Sega Master System fan translation timeline with a bang.

Included with this patch is a translated manual. It's quite a lovely manual, and has some information that's easy to miss while playing the game, so make sure to have a look at it.

This game doesn't seem to be based on any specific episode, but all the characters appear in the second series at some point, Ganso Tensai Bakabon.

## Patching Instructions
The patch is a [Beat patch](https://www.romhacking.net/utilities/893/). Either use the Beat patcher or patch your rom here:

[https://www.romhacking.net/patch/](https://www.romhacking.net/patch/)

No IPS patches will be provided.

## Translation Notes / Changes
* Variable Width Font was added
	* Please excuse the flickering sometimes. The VWF routine isn't the most efficient and publicly accessible VWF code out there isn't very readable. The code probably uses more clock cycles than it really should and the code takes up `0x200` bytes.
* The text speed was doubled. Similarly to what was done in the Metal Slader Glory translation, the sound effect when writing dialogue is skipped for every other character to eliminate obnoxious beeping as a result of the aforementioned hack.
* Namecards where hacked to support multiple lines.
* Underground level data was modified to translate the tiles that spelled "Bakabon".
* The character いね　むりのすけ (Ine Murinosuke) was localized to "Lazy Jones". The character was never officially localized in the anime, but it's supposed to be a pun about the character ~~sleeping~~ being hardworking. The localized name is a pun on "Lazy Bones" and is also a reference to the Commodore 64 game of the same name where you play as a hotel worker who slacks off. This is fitting as the Bakabon character presumably works at the building you find him at.
* "うらないのに　しょうばいなのか？" was translated as "Four tunas? Is that good business?"
	* The original is a pun on "uranai" which is both "fortune teller" and "won't sell", so literally "Is it really a business if you won't sell?".
* "ハジメてだなんて。" as translated as "Sorry, I don't think I know any Jimmy Round."
	* The pun here is that "Hajime" is the name of the missing son, but "hajimete" means "first time", so the stupid Bakadai student is saying "How could you forget me? This isn't our first meeting".
* The included translated manual features a two-paged advertisement for video game jigsaw puzzles (Which is a weird thing to advertise. Why not advertise other games, Sega???). The puzzle images are arcade game screenshots overlayed by Japanese text, rendering the original images unusable for the translation. Admittedly, playing through these games to get the exact moments was deemed to be more trouble than it's worth. As a result, (less exciting) replacement screenshots were obtained from the internet.

## Changelog
* 2023 August 26th: 1.2
	* Checksum correction, thanks to colonsimulator for reporting this. Certain BIOSes complain when the checksum is off.
* 2022 May 15th: 1.1
	* Credits corrections, thanks to Maxim for the corrections.
* 2022 May 5th: 1.0
	* Initial release

## Credits

### Main Team
* FCandChill
	* Project lead
	* ASM hacking
	* Graphics
	* Manual Editing
	* Utilities
	* Proofreader
* cccmar
	* For going above and beyond playtesting
	* Spot translations
	* Hacking
* TheMajinZenki
	* Translator
### Support
* Prof9
	* armipsz80 troubleshooting
* Pinobatch
	* Font feedback
* All the lovely people at SMS Power
	* Documentation (game specific and general)
	* Feedback
* Sega Retro
	* Manual scans
* Calindro
	* For making Emulicious that features an amazing debugger.
* Klarth
	* For making TileShop
* Maxim
	* Credits corrections
* colonsimulator
	* Checksum error report

### Beta Testers
* cccmar
* Révo
	* Real hardware tester
	* Not that guy from the Super Mario 64 decompilation project.
* togemet2