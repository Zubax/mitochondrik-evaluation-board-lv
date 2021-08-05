# Manufacturing instructions

## Evaluation board

To manufacture the device as an evaluation board, only the Jig PCB should be assembled.
No special instruction is needed; the assembly variant "STANDALONE" from the Jig project
should be used to generate BOM and PnP files.
As the mitochondrik footprint is populated using PLS2 male connectors,
the module installed on the PCB should be equipped with appropriate mating connectors.

The blow scheme for this usage scenario can be seen below.

<p align="center">
<img src="../figures/standalone_blow_scheme.svg" alt="" width="800"/>
</p>

## Production tool

To use the device as a production tool, two PCBs should be manufactured.
The Jig PCB should be manufactured using the "JIG" assembly variant to generate BOM and PnP files.

The blow scheme for this usage scenario can be seen below.

<p align="center">
<img src="../figures/jig_blow_scheme.svg" alt="" width="800"/>
</p>

Besides that, the adapter PCB should also be manufactured.
A fully assembled adapter PCB can be seen in the picture below.

<p align="center">
<img src="../figures/adapter_assembly.png" alt="" width="500"/>
</p>


Besides the 4x PBS11 connectors, the PCB also contains 44 pogo pins and a 3D-printed holder for the Mitochondrik module.
The pogo pins should be installed perpendicular to the surface of the PCB at the correct height.
As it may be tricky to do it by hand, it is recommended to use a special 3D-printed tool.
It can be seen in the picture below.

<p align="center">
<img src="../figures/pogo_tool.png" alt="" width="500"/>
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
<img src="../figures/adapter_blow_scheme.svg" alt="" width="800"/>
</p>
