--------------------------------------------------------------------------------
iBolit Simple Diagnostics Cartridge
Copyright (c) 2020-2022 RBSC
Last updated: 16.07.2022
--------------------------------------------------------------------------------

UPDATE from 16.07.2022
----------------------

It's recommended to update the cartridge with an overvoltage protection. See the "iBolit_fuse.jpg" image in the Pics folder!

To install the overvoltage protection, isolate pin 24 of IC1 - cut the traces on both sides of the pin. Then purchase and
solder a 5.1V 1W rated zener diode between pins 12 and 24, the cathode should be connected to pin 24. Solder resettable fuse
0.5A between C2 and pin 24 of IC1. Solder a wire between C5 and the cut off trace to supply power to the voltmeters.

This way the PLD ICs and LEDs will be protected from the overvoltage while the 5V voltmeter will show exact voltage on the slot
connector.



About
-----

iBolit is a simple diagnostics cartridge. During the previous years we've seen numerous messages from MSX users, whose computers
suddenly stopped working after being removed from the storage or after another power cycle. Many people complained about black
screens or about total power failure. It's a known fact that RAM and other elements may go bad during storing or at power-on.
Diagnosing those problems usually starts from checking the power rails, clock signals, reset signal's state and activity on data
and address bus. It has been decided to create a simple diagnostics cartridge that could help to perform the initial check of a
computer and rule out the most common problems.

The cartridge that we named "iBolit" ( see Doctor Aybolit) was created using the GAL22V10 programmable logic chips, LED assemblies
and volt/ammeters from the PC's USB socket tester dongles. There's a cartridge slot installed on the top of iBolit cartridge's
board. There one can insert any cartridge including the one with MSX diagnostics ROM (there are a few, but it would be nice to
create a universal one). The GAL firmware is very primitive - if there's a high level on input, the LED connected to the output
will light up. The cartridge is fairly cheap to build - maximum 12-15 Euro - and is relatively easy to assemble. The daughterboard
with voltmeters is detachable.


Where to buy parts
------------------

The parts for assembling the cartridge can be purchased from these sellers on AliExpress:

 - https://www.aliexpress.com/item/32929139598.html   (buy the one with gray case and USB connectors on the left and right side)
 - https://www.aliexpress.com/item/4000078359420.html (buy 2 converters)
 - https://www.aliexpress.com/item/4001336380255.html (buy 2x5 pin headers)
 - https://www.aliexpress.com/item/32890057619.html   (buy 2x5 pin connectors)
 - https://www.aliexpress.com/item/4000970562846.html (also buy blue and yellow colors)
 - https://www.aliexpress.com/item/32800771545.html   (or use a different 5mm LED)
 - https://www.aliexpress.com/item/32918831775.html   (buy 1kOhm SMD resistor assemblies)
 - https://www.aliexpress.com/item/32948284513.html   (this LED is for the -12v voltmeter)
 - https://www.aliexpress.com/item/32375666910.html   (buy 10uF and 47uF capacitors)
 - https://www.aliexpress.com/item/4001146953252.html (buy 50-pin angled slot connector)


Assembling notes
----------------

Please read the following notes carefully:


 - It's highly recommended to install ceramic capacitors everywhere on the board. For the DC-DC converters the ceramic 10uF
   capacitors are a must

 - To adapt the voltmeters to work with iBolit, you need to first carefully open the USB tester's case with a knife and remove
   the board. Then desolder both indicator panels (mark one indicator panel to know where it came from) and desolder both USB
   connectors from the board. After that solder the indicator panels back to the board, but as low as possible. And finally
   solder two 4-pin pin headers to the board, the pins will have to be forces into the board because the distance between the
   holes is not 2.54mm

 - The voltmeter with a separate red LED is for -12v, it should be installed on the lowest position of the daughterboard. See
   the reference images

 - To install a small red LED to the -12v voltmeter (this step is optional), solder the cathode to the upper GND track and
   anode to the second pin from the top. See the reference images. The LED should be a bit above the voltmeter's board

 - Please note that LED assemblies may have incorrect key position! So please always test the LED assemblies with multimeter
   in the diode testing mode to find the correct polarity. The cathode should be on the right, like marked on the board

 - The pins of both DC-DC converters should be carefully bent at 90 degree angle and the converters have to be installed
   face-down. See the reference images

 - The GAL chips need to be programmed with the firmware before use. A widespread TL866 programmer will do just fine. Use
   the .JED firmware file from the "Firmware" folder and the "GAL22V10D" chip type when programming

 - Instead of one blue and two red LED assemblies you might want to install one red and two blue LED assemblies. Make your
   own choice. It's recommended to install the yellow LED assembly at the rightmost position. If you are installing the
   green LED assembly, you need to select a different value for the resistor assembly, for example 330 Ohm instead of 1kOhm

 - Before inserting the diagnostics board into the MSX slot it's highly recommend to make sure that +5v on the slot is within
   acceptable range (not more than 6-7v!), otherwise the diagnostics board may be damaged. The device doesn't have the
   over-voltage protection on the +5v rail

 - The daughterboard with voltmeters is detachable. When it is detached, no power will be supplied to the upper cartridge slot.
   If you need to use the cartridge slot without the attached daughterboard, you need to put 5 jumpers horizontally on 5 pairs
   of pins of the connector


IMPORTANT!
----------

The RBSC provides all the files and information for free, without any liability (see the disclaimer.txt file). The provided information,
software or hardware must not be used for commercial purposes unless permitted by the RBSC. Producing a small amount of bare boards for
personal projects and selling the rest of the batch is allowed without the permission of RBSC.

When the sources of the tools are used to create alternative projects, please always mention the original source and the copyright!


Contact information
-------------------

The members of RBSC group Tnt23, Wierzbowsky, Pencioner, Ptero, GreyWolf, SuperMax and DJS3000 can be contacted via the group's e-mail
address:

info@rbsc.su

The group's coordinator could be reached via this e-mail address:

admin@rbsc.su

The group's website can be found here:

https://rbsc.su/
https://rbsc.su/ru

The RBSC's hardware repository can be found here:

https://github.com/rbsc

The RBSC's 3D model repository can be found here:

https://www.thingiverse.com/groups/rbsc/things

-= ! MSX FOREVER ! =-
