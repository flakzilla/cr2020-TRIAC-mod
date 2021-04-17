# Yamaha CR-2020 TRIAC power switch mod PCB
Cheap and convenient PCB for the famous TRIAC power switch mod. This board is meant for the Yamaha CR-2020 (and includes installation instructions targeting that device), but ought to work with anything that can support the TRIAC mod.

![Finished Board](img/board_complete_no_heatsink.jpg?raw=true "Finished Board (no heatsink)")

[Front Detail](img/board_front.jpg?raw=true)

[Rear Detail](img/board_rear.jpg?raw=true)

## Summary
This project is a dirt cheap PCB that makes it easier to install the TRIAC mod into a CR-2020. A complete BOM, example photos, and a hookup diagram are included.

The KiCAD project files are available for download from this repository ([direct link](https://github.com/flakzilla/cr2020-TRIAC-mod/tree/main/CR-2020%20TRIAC%20power%20switch%20mod)).

### What is the TRIAC mod?
The TRIAC mod is a way to extend the life of power switches with contacts that become damaged over time due to arcing. With the mod installed, a solid state TRIAC device is used to switch power electronically, and the power switch itself is rewired to activate the TRIAC at low current. Since the power switch doesn't have to pass high current in this configuration, the contacts won't arc as much during actuation, and the switch will last a lot longer.

Read up on these AK threads to learn more:
* https://www.audiokarma.org/forums/index.php?threads/yamaha-cr-2020-power-switch-failed-on.919979/
* https://www.audiokarma.org/forums/index.php?threads/is-your-unobtainium-power-switch-worth-5-and-an-hour-or-so-of-your-time.504673/

### Caution & Advice
* Do not apply the 08-80 (jumper wire) Service Bulletin if the TRIAC mod is installed.
* At least 2oz copper is required for the PCB.
* Although included in some diagrams, an RC snubber across MT1/MT2 is not required as long as the specified ("alternistor" type) TRIAC is used.
* The CR-2020 power switch has two sets of contacts: one to connect the main transformer, and another to connect the switched outlet. This implementation of the TRIAC mod doesn't protect the switched outlet contacts. If that's a concern, avoid using the switched outlet.
* It's possible to use the switched outlet's contacts in lieu of the main contacts if the main contacts are fried, just swap the red and white wires coming back from the power switch.

### Acknowledgements
The author would like to thank all of the AudioKarma users who invented, refined, and made it possible to find information about the TRIAC mod.

## How-To
### PCB
Recommend OSH Park, their service is very cheap for these small boards: https://oshpark.com/

Prepared gerber files for this board: [Gerbers, v1.0](https://github.com/flakzilla/cr2020-TRIAC-mod/blob/main/CR-2020%20TRIAC%20power%20switch%20mod/gerber%20zips/gerbers%20v1.0.zip)

Board requires **2oz copper weight**. Thicker copper is mandatory due to high current passing through the TRIAC. If using OSH Park, the 2oz-0.8mm service works great. The board is designed to just about handle 7A, the fuse current for the CR-2020.

### Parts
BOM:
* [ODS Format](https://github.com/flakzilla/cr2020-TRIAC-mod/blob/main/CR-2020%20TRIAC%20power%20switch%20mod/BOM/BOM.ods)
* [Excel Format](https://github.com/flakzilla/cr2020-TRIAC-mod/blob/main/CR-2020%20TRIAC%20power%20switch%20mod/BOM/BOM.xlsx)

Note that it's necessary to modify the heatsink to fit behind the transformer. Look at the pictures included with the KiCAD project files: [heatsink modifications](https://github.com/flakzilla/cr2020-TRIAC-mod/tree/main/CR-2020%20TRIAC%20power%20switch%20mod/reference/heatsink)

### Assembly
Install the populated board using the mounting hole for the small resistor behind the transformer. The factory mounting screw can be used to affix the standoff in place of the nut, and the factory nut is then used to affix the board to the standoff.

Wire according to the hookup diagram. You'll need an extra wire to connect MT1 to the fuse holder.
* [Hookup diagram](img/hookup_diagram.png?raw=true)

A completed installation:
* [Installed (clear view w/o heatsink)](img/installed_no_heatsink.jpg?raw=true)
* [Installed (w/ heatsink)](img/installed_heatsink.jpg?raw=true)

## License
This project is released under the terms of the Creative Commons Attribution + Noncommercial + ShareAlike (BY-NC-SA) license. https://creativecommons.org/licenses/by-nc-sa/2.0/

This project is distributed 'as-is' in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

