# Manufacturing instructions

## Evaluation board 
To manufacture the device as an evaluation board, only the JIG PCB should be assembled.
No special instruction needed, assembly variant "STANDALONE" from the JIG project should be used to generate BOM and PnP files.
As the mitochondrik footprint is populated using PLS2 male connectors,
the module installed to the PCB should be equipped with appropriate mating connectors.

## Production tool
To use the device as a production tool, two PCB should be manufactured.
The JIG PCB should be manufactured using "JIG" assembly variant to generate BOM and PnP files.
Besides that, the adapter PCB should also be manufactured. A fully assembled adapter PCB can be seen in the picture below.

![](../figures/adapter_assembly.png)

Beside 4 PBS11 connectors, the PCB also contains 44 pogo pins and a 3D printed holder for Mitochondrik module.
The pogo pins should be installed perpendicular to the surface of the PCB and at a correct height.
As it may be tricky to do it repeatable by hand it is recommended to use a special 3d printed tool. It can be seen in the picture below.

![](../figures/pogo_tool.png)

The tool should be placed UNDER the PCB and aligned with all the holes on the PCB. It can be temporarily fixed in place using M3 screws.
After that, the pins can be pushed into the tool through the PCB from the top. The pins should be pushed until the lower tip of the pin is flush with the lower surface of the tool (this guarantee the correct height of a pin in relation to the top surface of the PCB).
After that, the pins can be soldered from the top side of the PCB.
The tool is single-use and cannot be removed from the device after the pins are mounted.
After the pogo pins are installed the 3d printed holder should be secured in place using 4 8-12 mm length M3 screws and 4 M3 nuts.

Adapter blow scheme can be seen below.

![](../figures/adapter_blow_scheme.svg)