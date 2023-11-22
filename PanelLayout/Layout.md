## Panel Layout for PCB

The panel dimensions provided in the section "Original Design" below are based on my own module build, since I am not following the standard HP (1HP eq. 5.08mm) size. An alternative by building an HP-standard size panel can be found in the section "HP Standard Design" further below.

### Original Design
Coordinates given in the table fit to the layout of components given in the PCBc in folder GerberFiles.

Panel size: 95mm x 128.5mm

The numbers in the table are refering to the numbers in the picture below.
Coordinates origin is the lower left corner of the panel.


| No. | X-coord. [mm] | Y-coord. [mm] | Comment |
| --- | --- | --- | --- |
| 1 | 6 | 105 | Range Button |
| 2 | 13 | 105 | Range LED |
| 3 | 30 | 105 | Frequency Pot |
| 4 | 65 | 105 | Shape Pot |
| 5 | 82 | 105 | Output Mode LED |
| 6 | 89 | 105 | Output Mode Button |
| 7 | 47.5 | 102 | Ramp Mode LED |
| 8 | 47.5 | 95 | Ramp Mode Button |
| 9 | 20 | 77 | Slope Pot |
| 10 | 47.5 | 77 | Smoothness Pot |
| 11 | 75 | 77 | Shift/Level Pot |
| 12 | 12.5| 50 | Slope CV Pot |
| 13 | 30 | 50 | Frequency CV Pot |
| 14 | 47.5 | 50 | Smoothness CV Pot |
| 15 | 65 | 50 | Shape CV Pot |
| 16 | 82.5 | 50 | Shift/Level CV Pot |
| 17 | 10 | 30 | Slope CV Jack |
| 18 | 25 | 30 | Freqency CV Jack |
| 19 | 40 | 30 | 1Volt/Oct CV JACK |
| 20 | 55 | 30 | Smoothness CV Jack |
| 21 | 70 | 30 | Shape CV Jack |
| 22 | 85 | 30 | Shift/Level CV Jack |
| 23 | 22 | 40 | Output1 LED |
| 24 | 22 | 55 | Output2 LED |
| 25 | 22 | 70 | Output3 LED |
| 26 | 22 | 85 | Output4 LED |
| 27 | 15 | 10 | Trigger Jack |
| 28 | 15 | 25 | Clock Jack |
| 29 | 15 | 40 | Output1 Jack |
| 30 | 15 | 55 | Output2 Jack |
| 31 | 15 | 70 | Output3 Jack |
| 32 | 15 | 85 | Output4 Jack |

<img height="1000" src="https://github.com/TOILmodular/TidesV2/assets/97026614/c56b4e37-4cdc-4eb5-beba-1c4686d6eb5e">

### HP Standard Design
For building the panel with a size following the HP standard, you can use the panel Gerber file provided in the folder "GerberFiles".
I ordered my own panel via such gerber file built out of PCB material.

Here are a few parameters of the panel.
| Parameter | Value |
| --- | --- |
| Width | 18HP |
| Pot hole diameter | 8mm |
| Jack hole diameter | 6.1mm |
| Tact switch hole diameter | 5.1 mm |
| Mounting hole diameter | 3.2mm|
| LED hole diameter | 3.1mm|
