# ldBd
Simple Load Board for Power Supply Testing

This is a very simple PCB design to act as a power supply load board.  
Yes, there are fancy load boards available out there with digital readouts, fans, etc.
This goes opposite that - it is ***trivially simple***.
This is a simple 2 sided PCB 100mm X 100mm with 50 and 25 watt power resistors that can
be connected various ways using banana plug jumpers.
(See notes on the back of the PCB for some options)

It's a bit of a squeeze getting everything to fit, but staying at 100mmX100mm keeps board manufacturing inexpensive.
You can have 5 bare PCB's fabricated for you in China for just a few dollars plus shipping.
(For example I paid $2.00 + shipping for 5 bare boards from https://jlcpcb.com)

The files needed for PCB manufacturing are in the 'gerbers/'
directory.  The design was done in KiCad version 7, and the files with extensions "kicad_*" can be used to
modify it further, if you wish.

![A View of the Raw Board](doc/ldBd.jpg)

The power resistors are connected to the board mounting holes via short soldered jumpers and M3 bolts/nuts.
The whole top and bottom surfaces are mostly big copper pours, so resistor heat is spread across the entire board.

I haven't generated an official BOM, but the parts list is fairly simple:

- R1 is a 4 ohm, 50 watt power resistor
- R2 is a 2 ohm, 50 watt power resistor
- R3 is a 1 ohm, 50 watt power resistor
- R4 is a 0.5 ohm, 25 watt power resistor
- J1-17 (17 items) are banana jacks. I used black on one side and red on the other, but .. whatever you want.
- If you want the current sense option, J18 is a 1X2 0.1" pin header, and R5 is a 0.002 ohm 1206 sized surface mount resistor. Both are easy to hand solder.
- You will also need some M3 bolts&nuts - or similar - to hold the resistors down.
- and of course you need to make or buy banana plug jumpers.

Talking about parts; I am US based. The load resistors are available at reasonable prices from most any electronics
distributor - Digikey, Mouser, Newark, etc.  However, the only place I could find banana jacks
and plugs at a reasonable price (I don't consider > $1 each to be reasonable) was from China.
The jacks&plugs I used were from AliExpress - and YES as you can see if you look closely at the next picture - 
*the same supplier gave me 2 different styles*!

I 3d printed a simple base for the board.  The stl file for that is in the case/ directory. Use M3 bolts to fasten the board down.
Since the board CAN get quite warm, PETG or an alternate material with a higher glass transition temperature than PLA is recommended.

And here's ***my*** finished product!

![Finished ldBd](/doc/ldBd-all.jpg)

Usage is simple - you need to know `e = i * r` and how to calculate effective parallel and series resistances.
(Again, see the notes on the back of the board for some ideas ![back](doc/ldBd-back.pdf) )
Also - ***Use common sense***. Do not exceed the resistor ratings! I have found dissipating even 20 watts continuously
for 5-10 minutes on this board can make it get very warm. Use a fan if needed to increase heat transfer.

This work is licensed under the Creative Commons Attribution 4.0 International License. To view a copy of the license, visit https://creativecommons.org/licenses/by/4.0/
