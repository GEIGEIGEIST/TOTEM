# TOTEM BUILD GUIDE

## PART LIST

### REQUIRED PARTS

| Part name        | Count | Remarks | 
| :--------------  | :---: | :------ |
| TOTEM PCB        | 01 | You can find the files for it [here](/PCB/) |
| Seeed Studio XIAO| 02 | You can choose between the [nRF52840 BLE version (wireless)](https://www.seeedstudio.com/Seeed-XIAO-BLE-nRF52840-p-5201.html) or the [RP2040 version (wired)](https://www.seeedstudio.com/XIAO-RP2040-v1-0-p-5026.html) |
| Choc key switch  | 38 | Kailh Choc low profile key switches |
| diodes 1N4148W   | 38 | These are surface mount diodes in SOD123 package |
| 1u Choc keycaps  | 38 | You can use the black or white keycaps from Kailh, but I recommend MBK, LDSA or CFX keycaps |
| reset button     | 02 | Alps SKHLLCA010 |
| USB-C cable      | 01 | For connecting the keyboard to your PC |
| power switch     | 02 | MSK12C02 (only required for the Bluetooth build) |
| Lipo battery     | 02 | There is space for a 15 x 22 x 7.5 mm battery (only required for the Bluetooth build) |
| TRRS jack        | 02 | MJ-4PP-9 or PJ320A (only required for the wired build)|
| TRRS cable       | 01 | Alternatively, you can use a TRS cable for [half-duplex](https://github.com/qmk/qmk_firmware/blob/master/docs/serial_driver.md#usart-half-duplex) (only required for the wired build)|


### OPTIONAL PARTS

| Part name              | Count | Remarks | 
| :--------------------- | :---: | :------ |
| switch socket          | 38 | Switch sockets for Kailh choc switches |


### 3DP CASE PARTS

| Part name              | Count | Remarks | 
| :--------------------- | :---: | :------ |
| 3D printed case        | 02 | Find the case files [here](/case) |
| 6mm M2 standoffs       | 08 | 6mm round standoffs for screwing the top and bottom of the case together |
| 6mm M2 countersunk screws | 16 ||
| 8.5mm rubber feet | 8 | they can also be smaller |

### TENTING CASE PARTS
| Part name              | Count | Remarks | 
| :--------------------- | :---: | :------ |
| Additional 8.5mm rubber feet | 2 | Optional, they can also be smaller |
| Tenting feet | 4 | Example source [here](https://aliexpress.com/item/1005005605228469.html) |
| Anti-Slip adhesive sheet | 1 | Optional, example source [here](https://aliexpress.com/item/1005005377684110.html) |


## INTRODUCTION

Here is an overview of where and on which side each component needs to be soldered (click on the image to see a larger version).

![TOTEM solder guide](/docs/images/TOTEM_solderguide.png)


***

## BREAK OFF HALVES

The PCB comes in one piece. You need to break it into two halves.

![TOTEM PCB](/docs/images/buildguide/pcb_top.jpg)

After breaking them apart, you're left with some sprue marks, which you can remove with a file if you like, but you don't need to.

> **Warning**
> You should wear a mask while doing this since the FR4 dust is considered to be toxic.

![PCB sprue marks](/docs/images/buildguide/side_01.jpg)

I paint the edges black using a sharpie, so they fit better with the top and bottom, but that's optional too.

![PCB edges](/docs/images/buildguide/side_02.jpg)


***

## DIODES

The diodes need to be soldered on the top of the PCB. Pay attention to their orientation:  They have a small line on one side, which should be on the side the arrow on the PCB is facing to.

<p align="center">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="/docs/images/buildguide/diodes_dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="/docs/images/buildguide/diodes_bright.svg">
  <img alt="diode orientation" src="/docs/images/buildguide/diodes_dark.svg">
</picture>
</p>

Apply a small amount of solder on one pad.

![Solder on one pad](/docs/images/buildguide/diode_01.jpg)


Then use tweezers to place the diode on the pads and reheat the solder to secure the diode.

![Solder diode](/docs/images/buildguide/diode_02.jpg)


Now you can solder the second pad.

***
 
## SWITCH SOCKETS (optional)

Here you can apply the same technique as used for the diodes: Apply some solder on one of the pads first.

![switch sockets pad](/docs/images/buildguide/hotswap_01.jpg)

Then place the switch socket in the silk screen markings. The orientation matters here too. Especially if you plan on using the case.

<p align="center">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="/docs/images/buildguide/socket_dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="/docs/images/buildguide/socket_bright.svg">
  <img alt="hotswap socket orientation" src="/docs/images/buildguide/socket_dark.svg">
</picture>
</p>


![hotswap socket right and wrong orientation](/docs/images/buildguide/hotswap_02.jpg)


Then reheat the solder. 
Apply some pressure with a pair of tweezers to make sure the socket is fully seated.\
Now solder the second pad.

![switch socket soldered](/docs/images/buildguide/hotswap_03.jpg)

***

## POWER SWITCHES (only required for Bluetooth build)

Apply a tiny bit of solder on the bigger, outer pads on top of the PCB. 

![power switch pads](/docs/images/buildguide/power_01.jpg)

The power switch has some tiny knobs on its bottom, which fit into the PCB holes. Hold it in place with tweezers and then reheat the solder on the pad. After this, you can solder the other pad and the three pins.

![power switch](/docs/images/buildguide/power_02.jpg)


***

## RESET SWITCHES

Insert the switch into the top of the PCB. 

![reset switch](/docs/images/buildguide/reset_01.jpg)

I placed the footprint a bit more towards the edge, than it's meant to be, to integrate it better into the case. Therefore the tiny stabilizer on the bottom of the switch doesn't touch the PCB anymore. Make sure it is aligned with the PCB vertically, so it's oriented correctly.

![reset switch orientation](/docs/images/buildguide/reset_02.jpg)

Then solder the four pins on the bottom to the PCB

![reset switch solder](/docs/images/buildguide/reset_03.jpg)


***

## TRRS JACKS (optional)

> **Warning**
> You don't need the TRRS jacks for running the TOTEM with ZMK. Actually, you can damage your board when connecting it through TRRS, while also connected to a battery.

Install the TRRS jack on the bottom side of the PCB. The place where you should insert it is marked with a white line.

![TRRS jack](/docs/images/buildguide/trrs_01.jpg)

You may want to use some masking tape to hold it in place since you need to solder it on the bottom.

![TRRS jack taped](/docs/images/buildguide/trrs_02.jpg)

Then solder the pins on the bottom to the PCB.

![TRRS jack soldered](/docs/images/buildguide/trrs_03.jpg)


***

## MICROCONTROLLER

> **Warning**
> First flash the microcontroller to make sure it works, before soldering it in. Especially since you can't use sockets.

Place the microcontroller in its place. 

> **Note**
> If you're struggling with keeping it in place you can use the headers, which came with it, and some double-sided tape. But make sure it sits flat on the PCB. Otherwise, the case won't fit.

Apply some flux and try to hold the iron at an angle where you touch the pads of the microcontroller and the PCB while adding solder.

![soldering MCU](/docs/images/buildguide/MCU_01.jpg)

The pads on the back are a bit fiddly to solder, so you should add a lot of flux to the pads on the microcontroller first. Then apply the same technique as on the front: Try to touch the pads on the microcontroller and the PCB before adding solder. 

![soldering MCU back](/docs/images/buildguide/MCU_02.jpg)



***

## BATTERY (optional)

> **Warning**
> You don't need the battery for running the TOTEM with QMK. Actually, you can damage your board when connecting it through TRRS, while also connected to a battery.

You probably need to shorten the cables and tin them, since the length needs to be pretty short, to fit. I've also plasti dipped mine.

![shorten battery cables](/docs/images/buildguide/battery_01.jpg)

> **Warning**
> Before attaching the battery in any way to the PCB set the power switch to off (right on both sides).

You can see which cable needs to go in which eye by the silkscreen below the eyes. Red is + / Black is -.

![battery face](/docs/images/buildguide/batt_face.jpg)

Attach the wires of the battery to the pads and solder them in.

![Ouch](/docs/images/buildguide/it_stings.jpg)


***

## CLEANING

You can use an old toothbrush and some isopropanol to clean it from residues. 


***

## FIRMWARE

If you have not already flashed the firmware to the microcontroller you should do it now.\
[Here](https://github.com/GEIGEIGEIST/zmk-config-totem) you can find the ZMK firmware for the TOTEM.\
[Here](https://github.com/GEIGEIGEIST/qmk-config-totem) you can find the QMK firmware for the TOTEM.\

Probably a good idea to also install switches to make sure all of them work, before inserting the board into the case.

![PCB with switches](/docs/images/buildguide/pcb_switches.jpg)


***

## CASE

> **Note**
> I'm using the transparent version of the case, so it's easier to see where everything goes, but it's identical to the black/white case.

First, install the standoffs from below into the top of the case.

![Top case with standoffs](/docs/images/buildguide/case_top_standoffs.jpg)


Next screw them in from above.

![Top case with screws](/docs/images/buildguide/case_top_screws.jpg)


Now insert the board into the top and connect them using the switches.

![Top case with switches](/docs/images/buildguide/switches.jpg)


The bottom has some insets for using rubber feet. 

![bottom case insets](/docs/images/buildguide/case_bottom_bump.jpg)


You can then attach the bottom to the case and screw it in. 

![bottom case screws](/docs/images/buildguide/case_bottom_screws.jpg)



***

## FINAL BUILD

This is what the final keyboard will probably look like. 

![final build](/docs/images/buildguide/final.jpg)


