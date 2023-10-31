# Tides v2018 - Tidal Modulator Eurorack Module
A clone of the Mutable Instruments Tides version 2018 module.

(TBD module pictures)

## Module Build and PCBs
In the folder GerberFiles, I added two different versions for the control board, an "original" and a "Thonk" version.
Reason is that for my own module, I am using specific potentiometers - 16K4 series from Supertech Electronics - and 3.5mm jack sockets - MJ-355 from Marushin - available at my local electronics shop.

(TBD orig PCB picture)

However, since most DIY projects for Eurorack modules out there are using potentiometers from ALPHA and so-called THONKICONN jacks, as they are provided by Thonk in the UK, I also created another control board PCB version, called "Thonk", with footprints for those components.

(TBD Thonk PCB picture)

The main board PCB is the same for both versions

(TBD main PCB picture)

I created the Gerber files with the online tool EasyEDA and ordered it at JLCPCB.

## Panel Layout
I added the information about hole coordinates for the front panel in the folder PanelLayout, referring to the component layout in the Gerber files. The layout is the same for all PCB versions.

In addition, there is a Gerber file for the panel, following the HP standard. My own modules do not follow that width standard, as I am only using sliding nuts in my racks.

You can use the panel Gerber file to have the panel built out of PCB material.

## Additional Information about specific Components
The module build requires the soldering of SMD components. Besides the STM32F373 microcontroller, there is the DAC8164 chip and several other components, like op amps, voltage regulators, ceramic capacitors, ferrite beads, and a diode array.

Here is a list of SMD parts in my design.
- STM32F373CCT6 (microcontroller)
- DAC8164 (digital-analog0converter, 16-TSSOP package)
- TLV4172 (quad op amp, 8-SOIC, TL072 also works fine)
- LM1117-3.3 (voltage regulator, SOT-223 package)
- LM4040B10 (voltage regulator, SOT-23-3 package)
- BAT54ST (diode array, SOT-523 package)
- 0.1uF capacitors (1608 package)
- BLM18R (ferrite bead, 1608 package)

Concerning the resistor size, I am usually using small-size resistors, about half the length of the usual size, so they need less space on the PCB. If you want to use my Gerber files, you have to consider that fact. You might still use normal size resistors and put them in a standing position on the boards. Should also work fine.

## Firmware
I shared the .hex files for the STM32F373 chip (bootloader and main) in the folder Firmware.

## Programming
The main PCB contains connection points for both connector types for programming STM32 chips, JTAG and UART. Those can be used for standard pins with 2.54mm distance. Depending on the available connector, you only need one of those two connection point groups. However, I only tested the UART connection. The JTAG connection points do not match the standard JTAG adapter connectors. You need to check the lables on the adapter and on the PCB, and connect them, accordingly.

Besides that, there are two connection points for putting the chip into boot mode, which is needed for loading the bootloader file. Just solder a 1x2 pin with standard 2.54mm distance to connection points labeled "BOOT". For activating the boot mode, place a jumper onto the pins. As soon as the bootloder is uploaded, remove the jumper while keeping the board powered on to put the chip into operation mode, so the main code can be uploaded.

(TBD progamming connectors pictures)

## Calibration
The calibration procedure is the same, as the one for the original module from Mutable Instruments.

1. Disconnect all CV inputs.
2. Connect the note CV output of a well-calibrated keyboard interface or MIDI-CV converter to the V/OCT input. Leave all the other CV inputs unpatched.
3. Press the Range and Output Mode buttons simultaneously. The first LED will slowly blink.
4. Send a voltage of 1V to the V/OCT input.
5. Press any button. The second LED will blink.
6. Send a voltage of 3V to the V/OCT input.
7. Press any button.
