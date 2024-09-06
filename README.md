# Triumph-Adler SE 1040 Rebuild
The Triumph-Adler (TA) SE 1040 was a typewriter setup from the early to late 1980s, consisting of an external keyboard and a daisy wheel printer plus optional internal and external storage. While the printer units are hard to come by in good shape these days, the keyboards turn up on Ebay from time to time and I managed to grab two for cheap. My initial idea was to only re-use the keycaps, which are thick, black, low-profile double-shot ABS with MX compatible mounts. But then the boards arrived and I really liked their look.

![alt text](https://github.com/DirkSonguer/keyboard-TA-SE-1040/blob/main/images/TA-SE-1040-front.jpg "TA SE 1040 Front")

I decided to try to restore or rebuild the keyboards in some way. This repo documents my findings in case others want to mod their TA SE 1040s.

# What is this thing? And why does it exist?
In the early 1980s, it was already becoming clear that these "Computer" things might be on to something. But they also represented a [disruptive innovation](https://publish.obsidian.md/dirksonguer/Types+of+Innovation): Typewriter manufacturers had no idea how to manufacture computers, let alone write software for them. Typists also needed to learn completely new skillsets to effectively do the same as before and utilize the new capabilities of PCs. In 1982, the German company Triumph-Adler (TA), a leading manufacturer of typewriters at the time, created a gap-solution to allow themselves and typists an easier transition between both worlds.

The TA SE was a family of "highly intelligent text systems". As a modular system, the devices inthe series look very similar, sharing many of their components internal and external components and capabilities. While the most members of the SE family were manufactured as all-in-one typewriters, the SE 1040 series tried something new. Instead of housing the keyboard and the printing components in one chassis, TA separated both. The keyboard was housed within its own case that also contained a display capable of showing a row of 40 characters. All printing and paper handling related components were put inside a separate daisy wheel printer that could operate by itself.

![alt text](https://github.com/DirkSonguer/keyboard-TA-SE-1040/blob/main/images/TA-SE-1040-illustration.jpg "TA SE 1041 Illustration")

Both units connected via a parallel port, using standardized interfaces. This meant that some versions of the keyboard could also be used as a stand-alone teletypewriter, while the printer could also be used by a PC. The printer unit was also sold seprately as "[TRD 170](https://archive.org/details/de-bedienungsanleitung-triumph-adler-trd-170-s-typenraddrucker)" daisy wheel printer for office computers.

The keyboard unit was controlled by a [8048/49 microcontroller](https://en.wikipedia.org/wiki/Intel_MCS-48) and featured 
8kb of memory. It offered 10 memory slots, each capable of holding up to 730 characters, or about 10 lines of text. Other models featured 16kb and doubled the number of memory slots, as well as the option to use external storage. Typists could enter and edit text into the keyboard memory before sending it to print on the printer unit. Memory slots could also be used as templates and used in form letters.

The SE 1040 came in four editions:
* SE 1040: Keyboard without internal memory expansion & no external storage
* SE 1040 MD: Keyboard with internal memory expansion & external microdisk drive 
* SE 1041: Keyboard with internal memory expansion & external 5.25 floppy disk drive
* SE 1042: Keyboard with internal memory expansion, external 5.25 floppy disk drive & teletext capabilities

Triumph-Adler also sold a separate monitor, to which many of the SE devices could be connected. The [Adler Screentyper](https://etzone.org/wp-content/uploads/2020/07/4e598-adler-screen-typer.pdf) extended the 1040's display, organizing single rows into pages. The interface was fully controlled by the keyboard, giving users "*the benefit of genuine word processing with ease of operation of modern electronic typewriters.*"

At this point it becomes clear that the TA SE series are computers - just very simple ones that run no real operating system, but a hardwired word processor, utilizing familar typewriter keys and metaphors. They allowed Triumph-Adler to slowly get a grip on producing PCs, which led to the TA Alphatronic brand of computer systems in the mid 1980s. Typists on the other hand could already enjoy the benefits of word processing without learning a new interface paradigm. THis made the SE system quite popular, hence the relatively cheap price for 1040 variants today.

However, their PC line didn't turn out so well and in 1986, Triumph-Adler was acquired by Olivetti, a competitor of TA based in Italy. After the acquisition, production and development of TA products was largely halted, and several German manufacturing facilities were closed and sold off.

More information on the TA SE 10xx series of typewriters:
* https://deskthority.net/wiki/Triumph-Adler
* https://etzone.org/2016/12/15/adler-se-series-electronic-typewriters/
* https://www.provinz.bz.it/katalog-kulturgueter/de/suche.asp?kks_priref=150008265

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

I assume this denominates generations, however neither board shows any kind of manufacturing date reference that I can see.

## Switches
The switches are [Cherry M9](https://deskthority.net/wiki/Cherry_M9). According to the Cherry catalog, these are the low profile linear variant - the main housing sits below the steel plate, with the top part clipping into the plate.

The switches in the first board are M9 blacks (see pictures). The board also has two M9 switches with clear stems. Based on their slightly wonkier soldering my guess is that these were replacements / repairs at some point.

The second board features only M9 switches with clear stems, in line with the replacement switches from the first board. 

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
Rebuilding the keyboard poses an interesting dilemma:
1. Restore the keyboard, keeping as many original parts as possible
2. Reconstruct the keyboard with modern parts, only keeping the exterior

## Thoughts on Restoration
The original keyboard was connected to a daisy wheel printer unit that provided power and accepted character and command codes. A restoration effort would mean
1. Making sure all internal components work as they should
2. Build a converter box that would provide power as well as routes the keyboard input to a modern computer interface like USB

This assumes that the keyboards are still working and that it's actually desirable to type on the original switches. Especially the last part is debatable as the M9 switches are quite... [horrible](https://www.youtube.com/watch?v=OgUFYYTNaes).

In terms of restoring the keyboard, I recently got my hands on the original technical documentations for the SE 10-series as part of the estate of Gernot Haltenorth, a previous technical writer for Triumph-Adler. There are also other amazing people working on old TA SE keyboards (as the image below shows, which I got from a very helpful fellow). So it would be theoretically possible to repair any issues with the boards, assuming you could still get the components (which you can't).

![alt text](https://github.com/DirkSonguer/keyboard-TA-SE-1040/blob/main/images/TA-SE-1040-breakout-box.jpg "TA SE 1040 Breakout Box Work")

All that makes a true restoration possible, but (at least for me) impractical.

## Thoughts on Reconstruction
Reconstruction would start with removing the original PCB. Since everything is on that PCB this equates to removing the entire interior of the keyboard. Step two would be creating a new PCB with modern hot-swap cherry MX sockets, new display and some equivalent functionality for the comfort keys & LEDs.

## Layout
The original layout of the SE 1040 is, well, weird. While the alphas are standard, everything around them is wrong (see above). Rebuilding the original layout in [KLE](http://www.keyboard-layout-editor.com/) results in something like this:

![alt text](https://github.com/DirkSonguer/keyboard-TA-SE-1040/blob/main/original-layout/triumph-adler-se-1040.png "TA SE 1040 Original Layout")

If we assume that we want to keep the original top case as-is, then we can normalize the modifiers into a regular 60% keyboard, and add an additional column of keys to the left. This however leaves a weird 0.5u gap to the left on the bottom alpha row. Alternatively the PCB could support a 2.5u left shift that sticks out a bit.

The bottom modifier row is 12u in total (8u spacebar plus four 1u keys). Assuming a standard 6.25u spacebar, that leaves 5.75u. For example three 1.25u and one 2u. A 7u spacebar doesn't maske this mess any easier. I have played around with some options below, but haven't found a setup that I am happy with.

![alt text](https://github.com/DirkSonguer/keyboard-TA-SE-1040/blob/main/new-layout/keyboard-layout.png "TA SE 1040 New Layout")

Cutting a [prototype plate](https://github.com/DirkSonguer/keyboard-TA-SE-1040/blob/main/plate/plate-2024-03-24T16_29_11.879Z.pdf) with this (attached to the top case with tape) fits pretty well into the case. However, I wonder if it's practical to have a PCB with this layout. Instead it might be more practical to create four PCB modules: One for the comfort keys (also containing the LEDs), the main keyboard (standard PCB), the numpad (also normal numpad), and the display (LED display and driver).

## Display
There are still [Vacuum Fluorescent Displays](https://en.wikipedia.org/wiki/Vacuum_fluorescent_display) (VFD) in production, as for example described in [this project](https://www.hackster.io/macsboost/particle-weather-vfd-80fa78). They are also [not that hard to program for](https://hackingmajenkoblog.wordpress.com/2017/12/23/vacuum-fluorescent-displays-on-arduino/). However looking through some Chinese part lists, I couldn't come up with one that really fits the case as-is. I could fit two smaller ones side-by-side, but then there would be a bezel in the middle.

It might just be simpler to replace it with an LCD, or even one of those OLED strips. In that case I could use a regular graphics library and either emulate the old VFD-style, or even go full ham on design.

## Software used
* KLE for creating the layout: http://www.keyboard-layout-editor.com/
* ai03 Plate Generator for the plate: https://kbplate.ai03.com/

## Helpful links
Overview of tools to build mechanical keyboards: https://github.com/BenRoe/awesome-mechanical-keyboard/blob/master/src/pages/en/tools.md
