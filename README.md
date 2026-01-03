# Alpenmeister M v1 Controller
also known as Meisterbox M

![Picture of leverless controller.](https://github.com/AlpenmeisterCustoms/AlpenmeisterM-v1/blob/main/pictures/meisterboxM_front.png)
![Picture of leverless controller.](https://github.com/AlpenmeisterCustoms/AlpenmeisterM-v1/blob/main/pictures/meisterboxM_tilt.png)
![Picture of different controller faceplates.](https://github.com/AlpenmeisterCustoms/AlpenmeisterM-v1/blob/main/pictures/meisterboxM_faceplates.png)
[![Youtube Video](https://github.com/user-attachments/assets/df346f7e-8029-429a-80a5-c51b9253bf50)](https://youtu.be/GesAZIjat_Y)


Alpenmeister M v1 Controller is licensed under [Creative Commons Attribution-NonCommercial 4.0 International](https://creativecommons.org/licenses/by-nc/4.0/)  
Free to build and modify for personal use. If you want to sell this design, please contact me.

The goal here was to build a controller that is as thin and small as possible, yet using buttons that are typically used on arcade machines. The other main goal was to provide a framework to experiment and use different custom layouts, that suit ones individual needs best. Just move around the keyboard switches, put on a different cove and you are ready to go. Use different profiles to easily save and switch between them.

It comes with an acrylic cover so you can put in your favorite artwork. It has a second USB-C port for passthrough authenticator dongles like the Brook Wingman FGC or others to use this controller on different consoles. (more infos on compatibility here) Switches are Kailh choc v2. Button caps are made by Duelpad. The layout is the Meisterlayout with two thumb buttons, two pinky buttons and a center button. It's designed as ergonomic and flexible as possible.

## Case Files

The repository contains five STLs in the `stls_to_print` folder which you'll need to print to make the Meisterbox M:

* 1x `stls_to_print/Meisterbox M v1.3 bottom.stl`: the bottom of the shell
* 1x `stls_to_print/Meisterbox M v1.3 mid.stl`: the mid layer of the shell
* 1x `stls_to_print/Meisterbox M v1.3 top.stl`: the top layer of the shell

You might need to orient the items on your print bed. You should be able to print this on a standard printer's bed of about 250mmx250mmx250mm printer. This build has been tested in PLA and PETG. Our recommendation is using PETG if you can, since that would make sure your controller won't warp when exposed to heat or become brittle because of sun exposure. If you use this controller to travel, those might be some conditions it might get exposed to.

You will also find files for the acrylic cover `optional/Meisterbox M v1.3 acrylic.step` and a cutout file for the optional artwork `optional/Meisterbox M v1.3 Acrylic.dxf`. Optional faceplate ideas are also found in `optional/`.  

## PCB Files

You can find the files necessary to order the PCB in `pcb/`. Ordering the PCBs will need some caution. If you want to order the boards please closely follow the instructions.

### How to Order the PCBs
1. Go to JLCPCB.com
2. Click on "Order now"
3. Click on "Add gerber file" and choose "MeisterboxMv1.3.zip"
4. Use the default options (see reference at the end of these instructions), except those mentioned here:
    - PCB Color: choose your color, we would recommend black
    - Surface Finish: HASL, we would recommend LeadFree
    - Confirm Production file: Yes
5. Use the switch next to "PCB Assembly"  
6. Use the default options for PCB Assembly, except those mentioned here:  

    - **Confirm Parts Placement: Yes  
       THIS IS IMPORTANT, JLCPCB will make a production file to match the files we provide, please check if all components are where they should be**
    - PCBA Qty: Choose the same amount as PCB Qty
    - Advanced Options: don't touch and leave as defaults

7. Click "Next"
8. Click "Next"
9. Click "Add BOM" File and choose "MeisterboxMv1.3_bom.csv", then click "Add CPL File" and choose "MeisterboxMv1.3_cpl.csv". Then click "Process BOM & CPL"
10. You will then be presented with the components that are used on the board, they should be in stock and selected (hotswap sockets don't seem to be in stock anymore unfortunately; also if you don't want to pay the higher price for "standard assembly", don't check the LEDs to get populated). Only then click "Next". Do not proceed if some other components are missing and you don't know what they do.
11. You might then see a prompt saying "The system detects components that may be offset from the PCB, does it try to automatically align it?" (sic). Click "Cancel".
13. You'll be in your cart. Select the PCB we just configured and then go through the "Secure Checkout"

Please bear in mind: Do this at your own risk. It is your own responsibility to do the ordering process. We are not responsible for any mistakes in this instruction, as the actual ordering process might change at any time.
<details><summary>Click to see default options for reference</summary>

    PCB: 
    - Base Material: FR-4
    - Layers: 2
    - Dimensions: do not touch
    - PCB Qty: 5 is minimum
    - Product Type: Industrial/Consumer electronics
    - Different Design: 1
    - Delivery Format: Single PCB
    - PCB Thickness: 1.6mm
    - Silkscreen: White
    - Outer Copper Weight: 1oz
    - Via Covering: Tented
    - Min via hole size/diameter 0.3mm
    - Board Outline Tolerance: +/-0.2mm
    - Mark on PCB: Remove Mark
    - Electrical Test: Flying Probe Fully Test
    - Gold Fingers. No
    - Castellated Holes: No
    - Edge Plating: No
    PCB Assembly:
    - PCBA Type: Economic
    - Assembly Side: Top Side
    - Tooling holes: Added by JLCPCB
    - Parts Selection: By Customer
</details>


## Additional Hardware

You'll need some other hardware to assemble the whole controller:
* 14x Choc V2 switches
* 14x Choc hotswap sockets (since they seem to be permanently out of stock on JLC)
* 14x Duelpad 24mm and 30mm equivalent buttons
* 4x 4mm M3 heat inserts 
* 4x 8mm M3 flat top screws
* 1x 2mm acrylic top plate
* 1x USB-C cable (right-angled one with a slim connector is highly recommended)

## Assembly

1. Flash firmware onto board. Follow [these instructions](https://gp2040-ce.info/installation/). Use [this firmware](https://github.com/AlpenmeisterCustoms/GP2040-CE/actions/runs/19237635402/artifacts/4521340374).
2. Solder hotswap sockets to board.
3. Insert heat inserts into case.
5. Put PCB into bottom case part.
6. Stack mid and top layer on top of it.
7. Put acrylic plate on top of that.
8. Screw it together.
9. Insert switches and keycaps.
10. Enjoy.

## Licensing

Alpenmeister M v1 Controller is licensed under [Creative Commons Attribution-NonCommercial 4.0 International](https://creativecommons.org/licenses/by-nc/4.0/)  
Free to build and modify for personal use. If you want to sell this design, please contact me.  

## Contact

You can find me (@alpen.meister) on the [Open Stick Community Discord](https://discord.gg/JqK6K5tu).
Or on [Alpenmeister.com](https://alpenmeister.com/en/)
