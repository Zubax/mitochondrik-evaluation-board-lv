# Manufacturing instructions

## Evaluation board
MyDuck-LV can be used as an evaluation board for Mitochondrik LV. In this scenario, Mitochondrik LV is soldered 
directly to the PCB, turning MyDuck LV into a debug-friendly evaluation board or a PMSM motor controller.
<p align="center">
<img src="figures/Myduck-LV-standalone.png" alt="" width="600"/>
</p>

To manufacture the device as an evaluation board, only the main PCB should be assembled.
No special instruction is needed, the main PCB should be used to generate BOM and PnP files.
As the mitochondrik footprint is populated using PLS2 male connectors,
the module installed on the PCB should be equipped with appropriate mating connectors.

The blow scheme for this usage scenario can be seen below.

<p align="center">
<img src="figures/standalone_blow_scheme.svg" alt="" width="800"/>
</p>

## Production tool

MyDuck-LV can serve as a tool for production flashing and testing of Mitochondrik LV (line checkout fixture).
In this scenario, Mitochondrik LV is mounted on an intermediate PCB using pogo pins.
This PCB is then installed into MyDuck LV.
Mitochondrik LV can be aligned in place using 3D-printed parts (red parts in the picture below).
It can then be fixed using a strip of aluminum (as suggested in the model) or with a generic toggle clamp.
MyDuck LV is designed to accept the [Babel-Babel debugging tool](https://github.com/Zubax/Babel-Babel) directly.

<p align="center">
<img src="figures/Myduck-LV-jig.png" alt="" width="600"/>
</p>

To use the device as a production tool, two PCBs should be manufactured.
The main PCB should be manufactured using the "JIG" assembly variant to generate BOM and PnP files.

The blow scheme for this usage scenario can be seen below.

<p align="center">
<img src="figures/jig_blow_scheme.svg" alt="" width="800"/>
</p>

Besides that, the adapter PCB should also be manufactured.
A fully assembled adapter PCB can be seen in the picture below.

<p align="center">
<img src="figures/adapter_assembly.png" alt="" width="500"/>
</p>

Besides the 4x PBS11 connectors, the PCB also contains 44 pogo pins and a 3D-printed holder for the Mitochondrik module.
The pogo pins should be installed perpendicular to the surface of the PCB at the correct height.
As it may be tricky to do it by hand, it is recommended to use a special 3D-printed tool.
It can be seen in the picture below.

<p align="center">
<img src="figures/pogo_tool.png" alt="" width="500"/>
</p>

The tool should be placed UNDER the PCB and aligned with all the holes on the PCB.
It can be temporarily fixed in place using M3 screws.
After that, the pins can be pushed into the tool through the PCB from the top.
The pins should be pushed until the lower tip of the pin is flush with the lower surface of the tool
(this guarantees the correct height of the pin relative to the top surface of the PCB).
After that, the pins can be soldered from the top side of the PCB.
The tool is single-use and cannot be removed from the device after the pins are mounted.
After the pogo pins are installed, the 3D-printed holder should be secured in place using 4x 8-12 mm M3 screws
and 4x M3 nuts.

The adapter blow scheme can be seen below.

<p align="center">
<img src="figures/adapter_blow_scheme.svg" alt="" width="800"/>
</p>

## BOM for final assembly of MyDuck-LV as production tool

| Name                     | Quantity |
| ------------------------ | -------- |
| Adapter assembly         | 1 |
| MyDuck-LV PCB            | 1 |       
| Babel-Babel              | 1 |      

BOM required for the manufacturing of Adapter assembly.

| Name                     | Quantity |
| ------------------------ | -------- |
| Adapter PCB              | 1 |
| PBS11 female connectors  | 4 |
| Pogo pins                | 44 |
| Pogo pins soldering rail | 1 |  
| M3 x 12mm screw          | 4 |   
| M3 nut                   | 4 |
| Mitochondrik holder      | 1 |
| Aluminium/Plastic lock   | 1 |
