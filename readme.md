Thermocouple Interface | 3.3V
=============================

This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/3.0/">Creative Commons Attribution-ShareAlike 3.0 Unported License</a>.

<a rel="license" href="http://creativecommons.org/licenses/by-sa/3.0/"><img alt="Creative Commons License" style="border-width:0" src="http://i.creativecommons.org/l/by-sa/3.0/88x31.png" /></a>
	
Designed By:

*	Ryan McLaughlin <ryan@ryanjmclaughlin.com>


Summary
-------

The single thermocouple interface was made out of the need to interface a micro controller to a thermocouple. One of the popular chips to perform a thermocouple to digital conversion is the MAX6675 (now MAX31855). While this is a great little chip it is a small surface mount part and therefore difficult to solder. The thermocouple interface board not only helps with having the chip broken out to a simple 0.1" header, but also provides a mini-thermocouple connector to easily interface to a thermocouple. Thermocouples are not designed to be soldered and this provides a good solid connection, while also using the proper metals in the connector required for a thermocouple connection.

**CAUTION: The MAX31855 is for 3.3V only! If connecting to a 5V system, you must use a level shifter!!**

Tutorial
--------

It is simple to get everything up and running.

1.	Install a header or solder jumper wires to the pin connections
2.	Connect a K-Type [Thermocouple](http://en.wikipedia.org/wiki/Thermocouple Thermocouple) to the PCB Thermocouple Connector use a Thermocouple Wire Connector if necessary
3.	Wire the necessary connections to an Arduino or other micro controller, the bare minimum connections are +V, GND, SCK, SO, CS  **CAUTION: The MAX31855 is for 3.3V only! If connecting to a 5V system, you must use a level shifter!!**
4.	If using an Arduino, load one of the samples from the MAX6675 Arduino Library and you should see temperature information in the serial console. With other micro controllers you can access the chip using a standard SPI interface. See MAX31855 data sheet for more details.


Board Specs
-----------

*	Dimensions: 1.25" x 1.50"
*	Chip: MAX31855
*	Voltage: 3.3V
*	Header: 1x6 0.1" Pitch
*	Fixturing: Four Corner Holes (1.20"x0.95" Spacing)


Versions
--------

###Version 1.3

* Initial release under Eagle 6.1 on Github
* PCB Production dates: 09-2011, 01-2012

This revision changed from the MAX6675 to the new MAX31855 chip.  It has more accuracy and a better temperature range.  The footprint and fixturing holes have remained the same, but the board layout modified to make a better connection between the thermocouple connector and the MAX31855.  They were move closer together and larger traces between the chip and connector.  This should allow for better CJC, and more accuracy.  The board comes fully assembled along with a male and female header, and a 4050 level shifter chip. <small>Licensed under OSHW</small>

####Board Specs
*	Dimensions: 1.25" x 1.50"
*	Chip: MAX31855
*	Voltage: 3.3V
*	Header: 1x6 0.1" Pitch
*	Fixturing: Four Corner Holes (1.20"x0.95" Spacing)


###Version 1.2

This version of the board did not make many changes from V1.1.  The changes were mainly related to the manufacturing.  The PCB dimensions were better specified in the gerber files sent to fab resulting in better board routing.  The previous version was router slightly smaller than specified.  The solder mask was also updated to correct for some errors and spacing.

####Board Specs
*	Dimensions: 1.25" x 1.50"
*	Chip: MAX6675
*	Header: 1x6 0.1" Pitch
*	Fixturing: Four Corner Holes (1.20"x0.95" Spacing)


###Version 1.1

The next version made some major changes based on some feedback of the original version.  The additions included:

*	The recommended 0.1µF filtering cap for the MAX6675
*	Additional fixturing holes in each corner of the board to allow for flexible and rigid mounting
*	A power indicator LED
*	A status indicator LED that is driven by a separate pin, which is useful for displaying a status of the thermocouple from your program

####Board Specs
*	Dimensions: 1.25" x 1.50"
*	Chip: MAX6675
*	Header: 1x6 0.1" Pitch
*	Fixturing: Four Corner Holes (1.20"x0.95" Spacing)


###Version 1.0

The original version of this board was built as a simple breakout interface for the MAX6675.  The first attempt to do this was using a [http://www.sparkfun.com/commerce/product_info.php?products_id=494 SOIC to DIP adapter board].  While this worked, it did not provide a reliable connection for a thermocouple.  The solution was to use a [[PCB Thermocouple Connector]].

####Board Specs
*	Dimensions: 2.00" x 0.75"
*	Chip: MAX6675
*	Header: 1x5 0.1" Pitch
*	Fixturing: Single Hole


Purchase
--------

[store.ryanjmclaughlin.com](http://store.ryanjmclaughlin.com). 


TODO
----

*	Do not route LED through level shifter
