# RGBW_controller
![Image alt](https://github.com/AntaresLab/RGBW_controller/raw/master/Output/3D_Prints/RGBW_controller_top.png)

![Image alt](https://github.com/AntaresLab/RGBW_controller/raw/master/Output/3D_Prints/RGBW_controller_bottom.png)
***
This PCB designed for the LED strips controlling.

It allows to control 4 channnels of LED strips or another similar-controlled loads.

Channels can be paralleled in various combinations within one PCBA to increase the load capacity. In this case you need to ensure compatibility of such connection with your firmware of controlling MCU.

When using the components, specified in the schematic, you can get up to 2A from every channel in normal conditions without strong heating. Operating voltage of this PCBA is 9...15VDC. You will can increase maximal voltage and currents, if use suitable semiconductor devices.

This PCBA is protected against reverse Power polarity and overvoltage.

**Please, use a fuse that matches the total consumption of your loads.**

All output channels are connected to the outputs of the microcontroller timer. Thus, a hardware PWM signal can be generated at all outputs.

Trere is also a power-off detector installed on this PCB. If MCU PE5 pin input is low, power is ok. If you are not satisfied with the threshold of operation of the power-off detector, change the value of the zener diode VD3. If you are not satisfied with the delay in triggering the power-off detector, change the C3 capacitor rating.

Output drivers are connected to PC4 (R), PC3 (G), PC2 (B), PC1 (W) MCU pins.

MCU programms via the SWIM interface (X2).

There is a STM8S105K4 MCU used in this board.

PCB dimensions are 33x54mm. Maximal height of the components above the PCB is 10mm on top side and 2mm (excluding the top side components pins) on bottom side.

Mounting holes are designed for M3 screws. The distances between them are 25x46mm. Distance between the center of the mounting hole and the nearest edge of the board is 4mm.

***
I will be glad to any contribution to the development of my projects.

If you will find any mistakes or inaccuracies in my projects, please notify me about that.

I will be glad, if you modify, impove or port my projects to another CADs. Please notify me if you do this, and I will mention here about that.

If you have a successful experience of using this board with components other than listed in BOM-list, or with the exceeding the declared parameters, please notify me so that I can reflect it here.

If you develop any firmware for this board, please notify me of it, and I will post here a link to your project.

If you develop another version of this board, please notify me of it to document your branch or post a link to your branch here.

***
All schematics and board design files here are Copyright (c) 2018 AntaresLab aka Sergey Starovoitov serega.starovoitov@mail.ru.

Provided under the GNU GPL v3.

***
## Known firmware for this RGBW controller

* [RGB strip-based mood lamp](https://github.com/AntaresLab/Mood_lamp)
