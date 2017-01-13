ATmega32U4asISP
==========

A workaround for [arduino/Arduino#1182](https://github.com/arduino/Arduino/issues/1182): `avrdude: stk500_getsync() attempt 1 of 10: not in sync: resp=0x03` type errors when using ATmega32U4 based boards(Leonardo, Micro, Pro Micro, etc.) as an ISP with the ArduinoISP sketch on Windows. The workaround for this was discovered by Peter VanHoyweghen and explained at https://petervanhoyweghen.wordpress.com/2012/09/16/arduinoisp-on-the-leonardo/ but some modifications are required for this to work with recent versions of the [Arduino](http://arduino.cc) IDE.

This workaround adds an **Arduino as ISP(ATmega32U4)** option to the **Tools > Programmer** menu.

The ArduinoISP sketch included with Arduino IDE 1.6.6 or greater is required.


<a id="installation"></a>
#### Installation
There are two options for installing ATmega32U4asISP:
##### Boards Manager
This installation method requires Arduino IDE version 1.6.4 or greater.
- Open the Arduino IDE.
- Open the **File > Preferences** menu item.
- Enter the following URL in **Additional Boards Manager URLs**: https://per1234.github.io/ATmega32U4asISP/package_per1234_ATmega32U4asISP_index.json.
- Open the **Tools > Board > Boards Manager...** menu item.
- Wait for the platform indexes to finish downloading.
- Scroll down until you see the **ATmega32U4asISP** entry and click on it.
- If you are using Arduino IDE 1.6.6 then you may need to close **Boards Manager** and then reopen it before the **ATmega32U4asISP** entry will appear.
- Click **Install**.
- After installation is complete close the Boards Manager window.
- If using Arduino IDE previous to v1.6.6 you may need to restart the IDE to make the **ATmega32U4asISP** programmer appear in the **Tools > Programmer** menu.

##### Manual Installation
- Download the ATmega32U4asISP files here: https://github.com/per1234/ATmega32U4asISP/archive/master.zip.
- Extract the .zip file.
- Copy the extracted folder inside your {sketchbook}\hardware folder. To determine the location of the sketchbook folder check **File > Preferences > Sketchbook location**.
- If the Arduino IDE is running then restart it.


<a id="usage"></a>
#### Usage
- **File > Examples > 11.ArduinoISP > ArduinoISP**
- Connect your ATmega32U4 based board that will be used as the programmer to the target board as explained in the comments of ArduinoISP.
- Plug in the USB cable of the programmer board.
- **Tools > Board** > select the programmer board
- **Tools > Port** > select the port of the programmer board
- **Sketch > Upload**
- **Tools > Programmer > Arduino as ISP(ATmega32U4)**
- **Tools > Board** > select target board
- **Tools > Burn Bootloader** or **Sketch > Upload Using Programmer**


#### Contributing
Pull requests or issue reports are welcome! Please see the [contribution rules](https://github.com/per1234/ATmega32U4asISP/blob/master/CONTRIBUTING.md) for instructions.
