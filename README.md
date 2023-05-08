# Mitochondrik Evaluation Board LV

Mitochondrik Evaluation Board LV is a basic reference design and an evaluation board for the Zubax Mitochnodrik LV motor control module.
When combined with Mitochondrik LV, it makes a complete PMSM motor controller suitable for bench testing and evaluation of the
Telega motor control technology.
The device is also a specialized jig (fixture) that allows easy flashing and testing of all functions of Mitochondrik LV during manufacturing.

<p align="center">
<img src="docs/figures/1.png" alt="" width="800"/>
</p>

## Features

All external signals of Mitochondrik LV are accessible via the pin headers.
Mitochondrik Evaluation Board LV provides dedicated wire connectors for 2 Cyphal/CAN interfaces,
a Dronecode debug port, and one Aux connector for GPIO and RCPWM.
The motor phase wires and the DC link input are connected via M3 screw terminals.

<p align="center">
<img src="docs/figures/2.png" alt="" width="450"/>
</p>

A switch has been implemented which prevents powering the device if Mitochondrik LV is not installed or installed incorrectly.
Thanks to this feature, it is not required to remove the power supply every time before insertion of Mitochondrik LV.
The Mitochondrik presence pin is low when Mitochondrik is inserted.
Then, CAN_VDD should be set high, which turns on Q9, which then turns on Q11, allowing VDC to power the device.
The CAN_VDD is connected to the GPIO PA4 of Zubax Babel, which would turn on the power supply during testing.
The power supply switch is arranged in logic OR configuration, which means it's enable pin is attached to both of Babels
and either one of them can turn it on.
Check out the hardware schematic below:

<p align="center">
<img src="docs/figures/3.png" alt="" width="800"/>
</p>

A mechanical key is introduced to prevent incorrect insertion of Mitochondrik LV.

<p align="center">
<img src="docs/figures/4.png" alt="" width="800"/>
</p>

Headers are available to install the [Babel-Babel production tool](https://github.com/Zubax/Babel-Babel)
directly to the Mitochondrik Evaluation Board LV PCB without the need for an external adapter PCB.

| Stacked Babel-Babel | Babel-Babel headers |
| ------------------- | ------------------- |
| ![](docs/figures/5.png)  | ![](docs/figures/6.png)  |

## Specifications

* Supply voltage range: 13--51 V.
* Max continuous current/peak phase current amplitude: 10/20 A.
* Designed strictly for indoor use.

## Telega configuration

In order to use the Mitochondrik Evaluation Board LV, the installed Mitochondrik LV has to be informed
of the parameters of the board.
To achieve this, upload the following configuration:

```yaml
# Mitochondrik Evaluation Board LV has transistors with R_DSon = 4 mohms, and 3 mohm shunts on phases A and B.
# Refer to the Mitochondrik-LV datasheet for the explanation of how the parameter values have been found.
vsi.bridge_resistance:    [0.004, 0.007, 0.004, 0.007, 0.004, 0.004]                            # [ohm]
vsi.phase_current_gain:   [33.333333333333, 33.333333333333, 8.333333333333, 8.333333333333]    # [ampere/volt]
vsi.phase_current_stderr: [0.2, 0.2, 0.1, 0.1]                                                  # [ampere]
vsi.thermistor_v2k:       [223.15, 100.0, 0.0]                                                  # for MCP9700

sys.debug: false            # Turn off the in-circuit debug interfaces to enhance EMI immunity.
sys.golden: sys. vsi.       # Retain these parameter groups across a factory reset.
```

Refer to the Telega Reference Manual for details.

## Manufacturing instructions

For details on the manufacturing process of the device, check the
instructions at [manufacturing document](/docs/manufacturing.md).

## Release notes

Newest entries at the top.

### Mitochondrik Evaluation Board LV v1.2 (2023)

* P-Channel mosfet for safety insertion changed from SQJ459EP-T1_GE3 to RQ3L070ATTB due to availability issue
* Alternative part added for FDMS86368-F085

### Mitochondrik Evaluation Board LV v1.1 (2023)

* Bug fix for CANVDD not connected to protection circuit
* Added CANVDD supply for consumer version
* Added connecto to adapter for ribbon to connect top part of adapter to the bottom part

### Mitochondrik Evaluation Board LV v1.0 (2021)

* The original version.

### License

This project is licensed under the terms of [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/).
