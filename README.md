# Triumph Adler SE 1040 Rebuild
The Triumph Adler SE 1040 was a typewriter setup from the mid to late 1980s, consisting of an external keyboard & control unit and a daisy wheel printer unit.

While the printer unit is hard to come by in good shape these days, the keyboards turn up on Ebay from time to time and I managed to grab two for cheap. My initial idea was to re-use the keycaps, which are nice and thick, black, low profile double-shot ABS with MX compatible mount. But when the boards arrived I thought I might try and rebuild them in some way, either by trying some form of conversion (re-using some of the components), or completely replacing the interior with modern tech.

This repo documents my findings in case others want to mod their TA SE 1040s.

More information on the TA SE 10xx series of typewriters:
* https://etzone.org/2016/12/15/adler-se-series-electronic-typewriters/
* https://www.wikiwand.com/de/Triumph-Adler#Elektronische_B%C3%BCroschreibmaschinen_mit_Kugelkopf (German)
* https://deskthority.net/wiki/Triumph-Adler

# Keyboard documentation

![alt text](https://github.com/DirkSonguer/keyboard-TA-SE-1040/blob/master/images/TA-SE-1040-front.jpg "TA SE 1040 Front")

![alt text](https://github.com/DirkSonguer/keyboard-TA-SE-1040/blob/master/images/TA-SE-1040-back.jpg "TA SE 1040 Back")

## Switches
The switches seem to be [Cherry M9](https://deskthority.net/wiki/Cherry_M9) with black stems. According to the Cherry catalog, these are the low profile variant and in this board sit below the steel plate with only the top and stem above.

Both boards however also had switches with clear stems. Based on their slightly wonkier soldering my guess is that the clear ones were replacements / repairs at some point.

![alt text](https://github.com/DirkSonguer/keyboard-TA-SE-1040/blob/master/images/TA-SE-1040-switches.jpg "TA SE 1040 Switches")

## Keycaps

![alt text](https://github.com/DirkSonguer/keyboard-TA-SE-1040/blob/master/images/TA-SE-1040-keycaps.jpg "TA SE 1040 Keycaps")

## Display
The display is a 40x1 character [Vacuum Fluorescent Display](https://en.wikipedia.org/wiki/Vacuum_fluorescent_display) (VFD), each charater with a 5x12 dot matrix, driven by 12 Texas Instruments UCN4810A VFD display driver chips.

![alt text](https://github.com/DirkSonguer/keyboard-TA-SE-1040/blob/master/images/TA-SE-1040-display.jpg "TA SE 1040 Display")

# Rebuild


## Display

https://www.hackster.io/macsboost/particle-weather-vfd-80fa78

https://www.youtube.com/watch?v=JM_Iqasw9K4

https://hackingmajenkoblog.wordpress.com/2017/12/23/vacuum-fluorescent-displays-on-arduino/



## Software used
* KLE for creating the layout: http://www.keyboard-layout-editor.com/
* ai03 Plate Generator for the plate: https://kbplate.ai03.com/

## Helpful links
Overview of tools to build mechanical keyboards: https://github.com/BenRoe/awesome-mechanical-keyboard/blob/master/src/pages/en/tools.md
