# Impedance Probe Tool Intermediary Board

## Overview

This repository contains the intermediary board between the Teensy LC and Digilent Pmod-IA (Impedance Analyzer) boards used in the impedance analyzer probe tool, which is one of the instruments developed for operation by the MIT Bioinstrumentation Lab rover. The Autodesk Eagle layout and schematics can be found in the `Impedance Analyzer` directory. 

The two probes are connected to a Digilent Pmod-IA board, part of Digilent's line of small input-output interface boards. This Digilent Board is then connect to the custom-made intermediary board with the necessary electrical components to communicate with a Teensy LC over I2C protocol lines. All of these boards are packaged into a container built with a 3D printer and laser cutter.

The Teensy simply receives commands from the TOSLink transceiver and operates the Digilent Pmod-IA by sending the appropriate bit commands over the I2C lines. The high level commands simply determine the reference resistor. For instance, measuring a resistance range of 100 Ohm to 10 kOhm requires the use of a certain reference resistor, so the proper settings are adjusted on the Pmod-IA. However, on a lower level, the voltage range, number of samples, frequency sweep, and gain amplifier are all programmable from the control box without having to change the firmware on the Teensy.

## Contributors

#### Primary Contributors
Ryan Poon from the [MIT Bioinstrumentation Lab](https://bioinstrumentation.mit.edu/) is the primary contributor of this project.

#### Other Contributors
Professor Ian Hunter served as the main advisor.