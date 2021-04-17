Raspberry Pi I²C Level-Shifter
==============================

A PiHAT for converting the Raspberry Pi I²C Signals from 3.3V levels to 5V levels, which is usefull if you want to interface with I²C-components that use 5V voltage levels. The project aims to save time in wiring up an external level-shifter and just plug a shield on top of the gpio pins of the Raspberry Pi.

## Schematics, Layout

<img src="img/schematic.png" alt="schematic" height="350">
<br>

<img src="img/layout.png" alt="layout" height="350">
<br>

## Application

This is how the module is supposed to be used:

On Raspberry Pi 3B+:
<img src="img/rpi/RPi_3B+.jpg" alt="3b+" height="300">
<br>

On Raspberry Pi Compute Module 4 IO Board:
<img src="img/rpi/RPi_CM4IO.jpg" alt="cm4" height="300">
<br>

## Testing

I tested the pcb, however and hand-soldered everything (which I can definitely not recommend). Everything is soldered exactly like in the schematic, even though I placed some parts differently.

Here is how my prototype looks like:

<img src="img/pcb/pcb.jpg" alt="pcb" height="400">
<br>

<br>
And here are my oscilloscope measurements on level shifting a rectangular pulse with the following frequencies:

40kHz:
<img src="img/oscilloscope/40kHz.bmp" alt="osci_40kHz" height="300">
<br>

200kHz:
<img src="img/oscilloscope/200kHz.bmp" alt="osci_200kHz" height="300">
<br>

500kHz (from here on it doesn't seem to be able to reach the full 5V):
<img src="img/oscilloscope/500kHz.bmp" alt="osci_500kHz" height="300">
<br>

And here a screenshot of the included LT-Spice simulation:
<img src="img/simulation.png" alt="simulation" height="350">
<br>

## Dependencies

2N7002 MOSFET library (lbr/transistors_gaui.lbr):
* http://eagle.autodesk.com/eagle/download/1129

## License

The project is licensed under the MIT-License. For further information see `LICENSE.md`.
