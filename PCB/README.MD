# TOTEM PCB FILES

## MANUFACTURING

There are two versions available. Both fit the same [case](/case/README.MD), but require different microcontrollers.

### Version 0.3 (Standard)
Recommended for the standard **Seeed XIAO nRF52840** or **XIAO RP2040**.
- Download: [totem_0-3_gerbers.zip](/PCB/totem_0-3/totem_0-3_gerbers.zip/)

### Version 0.4 (Plus)
Tailored for the **Seeed XIAO nRF52840 Plus** and **XIAO RP2350**.
This version is **easier to solder** since there is a larger cutout. Also, the **battery pins are farther away** from the keyboard matrix pins, which should avoid shorts.
- Download: [totem_0-4-plus_gerbers.zip](/PCB/totem_0-4-plus/totem_0-4-plus_gerbers.zip)

---

If you want to get the PCB made you need to download the ZIP for your version and upload it to the website of the manufacture.
I can recommend [JLCPCB](https://jlcpcb.com/), [Seeed Fusion](https://www.seeedstudio.com/fusion_pcb.html) or [PCBway](https://www.pcbway.com/).
If you want the silkscreen in yellow [AllPCB](https://www.allpcb.com/online_pcb_quote_new.html) is a pretty affordable choice.

- download the ZIP file for your version
- upload the ZIP file to the website of the manufacturer.
- sometimes the Gerber preview from JLCPCB can't display the PCB, even when the files are fine. In this case use these dimensions: 258.7mm * 94.35mm
- PCB Thickness 1.6mm
- 2 layers
- PCB Qty as much as you like. One PCB is a full keyboard.
- PCB Color Black (or any other color you like)
- No impedance control
- Surface Finish HASL(with lead) if you want the easiest soldering experience or LeadFree HASL.
- Remove Order Number Yes

![TOTEM PCB](/docs/images/TOTEM_pcb.png)

***

## CHECK PINOUT OR TRACES

If you only want to check the traces or see what is connected to which pin you can take a look at these graphics.
You can also take a look at the PDFs:
- **0.3:** [schematics](TOTEM_0-3_schematics.pdf) and [PCB](TOTEM_0-3_PCB.pdf)
- **0.4:** [schematics](TOTEM_0-3_schematics.pdf) and [PCB](TOTEM_0-4-plus-PCB.pdf)

![TOTEM pinout](/docs/images/TOTEM_pinout.png)

***

![TOTEM traces](/docs/images/TOTEM_traces.svg)

***

## TAKE A DEEPER LOOK OR MODIFY 

You can download the project if you need to take a deeper look or modify something. You need the Open Source software [KiCad](https://www.kicad.org/) to open it.
