# Samurai Shodown III – Zankuro Musoken - English Patch for Sega Saturn)
English patch for **Samurai Spirits: Zankurou Musouken** (Sega Saturn, Japan).

The Japanese Saturn disc of Samurai Shodown III was converted from SNK's Neo Geo arcade version. 
The arcade original could run in Japanese or English, and the Saturn port kept a surprising amount of that English material: 
fighter names, menus, story texts, the loading screen, even the code that switches between the two languages. 
It simply never switches: the game always starts in Japanese.

I admit the language barrier in this game isn't a big deal, but was the ideal scenario to test myself into hacking roms on real purpose.

I started this patch some time ago the "long way" (with very little knowledge, using Crystal Tile 2, Hex Ed...) but after some stopped time I decided to help myself with Claude Code and learn from it for future projects.

## Requirements

- A dump of the Japanese disc in **BIN/CUE** format with one file per track (Redump style).
- **Delta Patcher** ([download](https://www.romhacking.net/utilities/704/)), **xdelta3-gui** ([download](https://github.com/Moodkiller/xdelta3-gui-2.0)) or any other xdelta3 front-end.
- To play: the **1 MB RAM cartridge** (or a 4-in-1 cartridge), on a real Saturn or in an emulator.
- **ImgBurn** ([download](https://www.imgburn.com/index.php?act=download)) to burn the patched disc (or your favourite tool).

Only **Track 01** is patched. The audio tracks and the `.cue` file stay as they are.

### Check your Track 01 properties

Original:

- Size: 57504048 bytes
- CRC32: 5DDFD8B3
- MD5: 10ef62790e424328f00d37bfe36d0ce7
- SHA-1: 8b19487e66d3999709578a526d9f200154ab5583

Patched:

- Size: 57504048 bytes
- CRC32: E415D2A2
- SHA-1: 1c8f774d6cc8b588a6676f288942ecbaaf654d14

If the original checksum does not match, the patch will not apply to your dump. Anyway if you find your version doesn't have the given checksum, contact me and I'll check on it and adapt it.

## How to apply

### GUI style (recommended)
With an xdelta3 front-end (such as Delta Patcher or xdelta3-gui): choose Track 01 as the original/source file, the `.xdelta` file as the patch, and apply.

### CMD style
Use the following command:

xdelta3 -d -s "Samurai Spirits - Zankurou Musouken (Japan) (Track 01).bin" "Samurai Shodown III (English) - Track 01.xdelta" "patched.bin"
   
## After patching
1. Replace the original Track 01 with the patched file, **keeping the original file name**, so the `.cue` still finds it.
2. Burn the `.cue` file using the lowest speed available. I strongly recommend using ImgBurn on Windows (IMHO ImgBurn is the best to me since it's the only one I found, empirically, that works properly with MODE1/2352 CUEs).

## Credits

- Myself (alexbl9x)
- Claude Opus 5.5
