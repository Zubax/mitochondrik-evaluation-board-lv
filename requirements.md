# Requirements for MyDuck LV

## Device purpose

MyDuck LV is a device designed for the production of [Mitochondrik LV](https://zubax.com/products/mitochondrik-lv) module.
It can be considered as a specialized jig, that allows easy flashing and excessive testing of all functions of Mitochondrik LV module.
A possibility to use MyDuck LV as an evaluation board for Mitochondrik LV should also be considered.
MyDuck LV combined with Mitochondrik LV makes for a complete PMSM motor controller.

## Technical requirements

* Mitochondrik LV flashing capability.
* Mitochondrik LV mounting should be possible without adding any components to the module in any way.
* Capability to test all the functions of Mitochondrik LV.
* The mechanical key, that prevents installing Mitochondrik LV incorrectly.
* The electronic key that prevents powering the device if Mitochondrik LV is not installed or installed incorrectly.
* The ease of access to all the Mitochondrik LV external signals when the device is used as an evaluation board.

## Power stage requirements

* Supply voltage range - 13 - 51 V.
* Max continuous current/peak current - 10/20 A.
* Repairability.
* Some means for easy heat sink mounting should be considered.

## Logic part requirements

* Repairability.
* CAN interface ICs should be protected with TVS diodes.
* 5V supply line should be protected with TVS diode.

## Design requirements for using the device as a production jig

Due to the low reliability of pogo pins, Mitochondrik LV should be installed on a separate adapter PCB
which in turn should be installed on the main MyDuck LV PCB.
This allows for replacement of only the adapter PCB in case of a single pogo pin failure.
The adapter PCB (and all the parts fastened to it) should allow for easy,
reliable and repeatable positioning and fixing Mitochondrik LV in place.
Also, some means of correct pogo pins mounting (perpendicularity to the PCB surface and correct height above PCB surface are critical) should be introduced.

It should be possible to install [Babel-Babel production tool](https://zubax.com/products/mitochondrik-lv) directly to the MyDuck LV PCB
without the need for an external adapter PCB.

## Environmental conditions

* Indoor use
* Operating temperature range - 0...+40С.
* Humidity - up to 100%

Using non-AEC-Q grade components as well as deviations from the hardware development policies is allowed.
