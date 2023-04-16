# Triumph Adler SE 1040 Rebuild
The Triumph Adler SE 1040 was a typewriter setup from the mid to late 1980s, consisting of an external keyboard & control unit and a daisy wheel printer unit.

While the printer unit is hard to come by in good shape these days, the keyboards turn up on Ebay from time to time and I managed to grab two for cheap. My initial idea was to re-use the keycaps, which are nice and thick, black, low profile double-shot ABS with MX compatible mount. But when the boards arrived I thought I might try and rebuild them in some way, either by trying some form of conversion (re-using some of the components), or completely replacing the interior with modern tech.

This repo documents my findings in case others want to mod their TA SE 1040s.

More information on the TA SE 10xx series of typewriters:
* https://etzone.org/2016/12/15/adler-se-series-electronic-typewriters/
* https://www.wikiwand.com/de/Triumph-Adler#Elektronische_B%C3%BCroschreibmaschinen_mit_Kugelkopf (German)
* https://deskthority.net/wiki/Triumph-Adler

# Keyboard documentation

![alt text](https://github.com/DirkSonguer/keyboard-TA-SE-1040/blob/main/images/TA-SE-1040-front.jpg "TA SE 1040 Front")

![alt text](https://github.com/DirkSonguer/keyboard-TA-SE-1040/blob/main/images/TA-SE-1040-back.jpg "TA SE 1040 Back")

## PCBs
The two boards seem to be two different editions. While not different from the outside, the PCBs (and switches, see below) do differ.
* The first board is labelled "Assembly Group EDCA01" ("Baugruppe" in German)
* The second board is labelled "Assembly Group EDCA03"

I assume this denominates generations, however neither board shows any kind of manufacturing date reference.

## Layout
Both the SE 1040's have a German ISO-DE layout with some additional modifyer keys to control typewriter functionalities like font settings and cursor control. It's similar to a 60% plus numpad plus 6 XT-style F-keys.

Notably, on the first board the top left key on the "numpad" function cluster is a blank & doesn't have a switch underneath. The second board has a working switch there, with an "E-mail" icon on the respective keycap.

In total, the keyboard has 84 keys (83 + 1 blank).

![alt text](https://github.com/DirkSonguer/keyboard-TA-SE-1040/blob/main/original-layout/triumph-adler-se-1040.png "TA SE 1040 Layout")

## Switches
The switches are [Cherry M9](https://deskthority.net/wiki/Cherry_M9). According to the Cherry catalog, these are the low profile linear variant - the main housing sits below the steel plate, with the top part clipping into the plate.

The switches in the first board are M9 blacks (see pictures). The board also has two M9 clear switches. Based on their slightly wonkier soldering my guess is that these were replacements / repairs at some point.

The second board features only M9 clears, in line with the replacement switches from the first board. 

![alt text](https://github.com/DirkSonguer/keyboard-TA-SE-1040/blob/main/images/TA-SE-1040-switches.jpg "TA SE 1040 Switches")

## Keycaps
The keyboard has black, low profile keycaps. They are 2mm thick and 8mm at their highest point, with a width of 18mm (1u). The alphas have concave indents and are slightly angled, although every row features the same angle. The modifyers and relegendables have flat surfaces.

![alt text](https://github.com/DirkSonguer/keyboard-TA-SE-1040/blob/main/images/TA-SE-1040-keycaps.jpg "TA SE 1040 Keycaps")

## Display
The display is a 40x1 character [Vacuum Fluorescent Display](https://en.wikipedia.org/wiki/Vacuum_fluorescent_display) (VFD), each charater with a 5x12 dot matrix, driven by 12 Texas Instruments UCN4810A VFD display driver chips.

![alt text](https://github.com/DirkSonguer/keyboard-TA-SE-1040/blob/main/images/TA-SE-1040-display.jpg "TA SE 1040 Display")

## LEDs
On the left is a column of function keys with corresponding LEDs: Typing mode, text alignment, font weight, line weight, font size and line height. The keys would swith through the options with the LEDs highlighting the currently selected one.

In total, there are 22 LEDs in 6 groups. Each group is a separate module soldered to the PCB.

# Rebuild
Rebuilding the keyboard poses an interesting dilemma:
1. Try to get the keyboard running again with as many original parts as possible
2. Reconstruct the keyboard with modern parts, only keeping the exterior original



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
