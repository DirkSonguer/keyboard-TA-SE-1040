# Triumph Adler SE 1040 Rebuild
The Triumph Adler (TA) SE 1040 was a typewriter setup from the early to late 1980s, consisting of an external keyboard and a daisy wheel printer plus optional internal and external storage.

![alt text](https://github.com/DirkSonguer/keyboard-TA-SE-1040/blob/main/images/TA-SE-1040-illustration.jpg "TA SE 1041 Illustration")

The SE 1040 came in 3 editions:
* SE 1040: Keyboard without internal memory expansion & no external storage
* SE 1041: Keyboard with internal memory expansion & external 5.25 floppy disk drive
* SE 1040 MD: Keyboard with internal memory expansion & external microdisk drive 

All three would attach to the same daisy wheel printer. While the printer unit is hard to come by in good shape these days, the keyboards turn up on Ebay from time to time and I managed to grab two for cheap. My initial idea was to only re-use the keycaps, which are thick, black, low-profile double-shot ABS with MX compatible mounts. But then the boards arrived and I really liked their look.

I decided to try to restore or rebuild the keyboards in some way. This repo documents my findings in case others want to mod their TA SE 1040s.

More information on the TA SE 10xx series of typewriters:
* https://etzone.org/2016/12/15/adler-se-series-electronic-typewriters/
* https://www.wikiwand.com/de/Triumph-Adler#Elektronische_B%C3%BCroschreibmaschinen_mit_Kugelkopf (German)
* https://deskthority.net/wiki/Triumph-Adler

# Keyboard documentation

![alt text](https://github.com/DirkSonguer/keyboard-TA-SE-1040/blob/main/images/TA-SE-1040-front.jpg "TA SE 1040 Front")

![alt text](https://github.com/DirkSonguer/keyboard-TA-SE-1040/blob/main/images/TA-SE-1040-back.jpg "TA SE 1040 Back")

Both the SE 1040's have a German ISO-DE layout with additional modifyer keys to control typewriter functionalities. The main keys are similar to a 60% plus 6 XT-style function keys (left) plus a numpad (right).

In total, the keyboard has 84 keys.

![alt text](https://github.com/DirkSonguer/keyboard-TA-SE-1040/blob/main/images/TA-SE-1040-keyboard-illustration.jpg "TA SE 1040 Keyboard Illustration")

![alt text](https://github.com/DirkSonguer/keyboard-TA-SE-1040/blob/main/original-layout/triumph-adler-se-1040.png "TA SE 1040 Layout")

## Main Keys
At first glance the main keys look look similar to a 60% keyboard, however with some oddities:
* 8u space bar
* The enter key is a "Big Ass Enter", however 1u by 2u
* ctrl & alt are other function keys with 1u
* Left shift is 2.5u
* Right shift is 1,5u
* Backspace is 1.5u
* There are 3 additional keys to the left

Since the board uses M9 switches, the key sizes and distances are the same as with a modern board.

## Comfort Keys & LEDs
TA calls the left function row "comfort keys". These are a column of six function keys with corresponding LEDs.

From top to bottom:
* Operating mode
* Font alignment
* Printing mode
* Typing pressure
* Character spacing
* Line spacing

![alt text](https://github.com/DirkSonguer/keyboard-TA-SE-1040/blob/main/images/TA-SE-1040-comfort-keys.jpg "TA SE 1040 Comfort Keys")

Pressing the comfort keys would switch through the available options. An LED next to the key would highlight the currently selected option.

In total, there are 22 LEDs in 6 groups. Each group is a separate module soldered to the PCB.

## Additional Keys
TA calls the numpad cluster "additional keys". It does not contain any number keys, but typewriter controls. The symbols are thus not usually found on computer keyboards. However there are some familiar ones like "START", "END", "LINE UP" and "LINE DOWN".

## PCBs
The two boards seem to be two different editions. While not different from the outside, the PCBs (and switches, see below) do differ.
* The first board is labelled "Assembly Group EDCA01" ("Baugruppe" in German)
* The second board is labelled "Assembly Group EDCA03"

I assume this denominates generations, however neither board shows any kind of manufacturing date reference.

## Switches
The switches are [Cherry M9](https://deskthority.net/wiki/Cherry_M9). According to the Cherry catalog, these are the low profile linear variant - the main housing sits below the steel plate, with the top part clipping into the plate.

The switches in the first board are M9 blacks (see pictures). The board also has two M9 clear switches. Based on their slightly wonkier soldering my guess is that these were replacements / repairs at some point.

The second board features only M9 clears, in line with the replacement switches from the first board. 

![alt text](https://github.com/DirkSonguer/keyboard-TA-SE-1040/blob/main/images/TA-SE-1040-switches.jpg "TA SE 1040 Switches")

## Keycaps
The keyboard has black, low profile keycaps, made out of double-shot ABS. The lettering is middle-centered and quite large.

![alt text](https://github.com/DirkSonguer/keyboard-TA-SE-1040/blob/main/images/TA-SE-1040-keycaps.jpg "TA SE 1040 Keycaps")

The alphas are uniform and have concave indents, however they are slightly angled. 1u is 17.7mm x 17.7mm. They are 7.4mm at their highest point (front-facing) and 6.3mm at their lowest (back-facing), making the angle about 4°.

The modifyers and relegendables have flat surfaces without indents and have the same angle.

![alt text](https://github.com/DirkSonguer/keyboard-TA-SE-1040/blob/main/images/TA-SE-1040-keycaps-details.jpg "TA SE 1040 Keycap Details")

## Display
The display is a 40x1 character [Vacuum Fluorescent Display](https://en.wikipedia.org/wiki/Vacuum_fluorescent_display) (VFD), each charater with a 5x12 dot matrix, driven by 12 Texas Instruments UCN4810A VFD display driver chips.

![alt text](https://github.com/DirkSonguer/keyboard-TA-SE-1040/blob/main/images/TA-SE-1040-display-illustration.jpg "TA SE 1040 Display Illustration")

![alt text](https://github.com/DirkSonguer/keyboard-TA-SE-1040/blob/main/images/TA-SE-1040-display.jpg "TA SE 1040 Display")

# Rebuild
Rebuilding the keyboard poses an interesting dilemma: Either try some form of restoration (repair and re-use the original components) or by replacing the interior with modern tech
1. Restorate the keyboard with as many original parts as possible
2. Reconstruct the keyboard with modern parts, only keeping the exterior

## Thoughts on restoration
The original keyboard was connected to a daisy wheel printer unit that provided power and likely more functionality. Little documentation exists how the 104x units actually worked, so it would need to be a complete reverse engineering effort.

The end state would be building a converter unit that would provide power as well as routes the input to a modern computer interface like USB.

This assumes that the keyboards are still working, the reverse engineering goes well and it's actually desirable to type on the original switches. Especially the last part is debatable.

## Thoughts on reconstruction

## Layout

## Display

https://www.hackster.io/macsboost/particle-weather-vfd-80fa78

https://www.youtube.com/watch?v=JM_Iqasw9K4

https://hackingmajenkoblog.wordpress.com/2017/12/23/vacuum-fluorescent-displays-on-arduino/

## Software used
* KLE for creating the layout: http://www.keyboard-layout-editor.com/
* ai03 Plate Generator for the plate: https://kbplate.ai03.com/

## Helpful links
Overview of tools to build mechanical keyboards: https://github.com/BenRoe/awesome-mechanical-keyboard/blob/master/src/pages/en/tools.md
