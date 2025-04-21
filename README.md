# Molise Firmware

Please do not hesitate to support me. Pay me a 🍺 or a ☕: [https://paypal.me/dtouton](https://paypal.me/dtouton)

My Youtube channel: [Dtcreation 3D](https://www.youtube.com/channel/UCQOsiY8l6Of56zkFhtDT0Sw)

My Instagram : [Dtcreation 3D](https://www.instagram.com/dtcreation3d/)

My Twitter : [Dtcreation 3D](https://twitter.com/Dtcreation3)

Join our facebook group: [Molise Firmware](https://www.facebook.com/groups/molisefirmware)

The sources for the TFT screen are [available on this repository](https://github.com/Dtcreation/Firmware-Molise-TFT)

Super fang for BLtouch [Thingiverse](https://www.thingiverse.com/thing:4589399)

Super fang for TouchMi [Thingiverse](https://www.thingiverse.com/thing:4713319)

### What is Molise firmware

Molise is modified firmware for brand printers [Artillery](https://artillery3d.com/). The firmware also supports Sidewinder X1 and X2, Genius and Genius Pro and la Hornet.

Firmware is split in 2

- For the motherboard: Marlin Molise
- For TFT screen: Based on Bigtreetech firmware. [Sources available here](https://github.com/Dtcreation/Firmware-Molise-TFT)

### Current version

Latest version of Molise __4.x__ based on [Marlin LTS-2.1.2](https://github.com/MarlinFirmware/Marlin/tree/lts-2.1.2)

### About Molise Firmware

Here is a listing of what the Firmware currently offers:

Firmware currently supports the following hardware:

- TMC 2100, 2208 or 2209 and LV8729 drivers and UART mode
- Motherboard SKR 1.3, 1.4, 1.4 Turbo and MKS SGen L v1 and v2, MKS Gen L v1 and v2.1
- Extrude BMG, Hemera and Matrix
- BlTouch (with or without Waggster Mod)
- TouchMi with or without LED on X1

The Firmware makes the following changes to Marlin (compared to the stock version)
- Support of BlTouch and TouchMi
- Auto Bed Leveling with Stock Sensor [more information on the 3dprintbeginner website](https://3dprintbeginner.com/sidewinder-x1-auto-bed-leveling-stock-sensor/)
- Graphical LCD: Marlin mode for Bigtreetech and clone screens
- Sensorless Homing: Allows positioning of an axis without the need for a physical limit switch
- The M600: allows you to change color during printing (Compatible with SD card, USB key and Ocotprint)
- Mesh Bed Leveling: MBL - Allows you to manually palpate several points of your plate as a BLTouch would do it automatically
- Automatic alignment of Z steppers (Z_STEPPER_AUTO_ALIGN)
- Solution to the Octoprint communication problem by changing the connection of the TFT screen on the MKS Gen L (option)
- Removal of the runout filament sensor on the motherboard for compatibility with Octoprint and SD reader on the motherboard (Option) (for the original motherboard, plug it on D2 pin X+ connector)

The code in the `Configuration.h` file has been split into 7 sections to make the code more readable. So, for people who want to compile code from source, the job will be easier. For more explanation on the code compilation, please refer to the [dedicated wiki](https://github.com/Dtcreation/Firmware-Molise-Artillery/wiki)

Molise 4.x firmware is provided to you free of charge in an "as is" state. We cannot be held responsible for any damage it may do to your 3D printer if it occurs. Please proceed with caution.

To make your task easier, the molise firmware is supplied to you "pre-compiled" for the following 6 cases:

- X1 Stock
- X1 Stock + BLTouch (Waggster Mod)
- X1 Stock + TouchMi
- Genius Stock
- Genius Stock + BLTouch (Waggster Mod)
- Genius Stock + TouchMi
- X2 Stock
- Genius Pro Stock
- Hornet Stock

The Molise Firmware is supplied with a second firmware, this is the firmware of the TFT screen. This TFT Firmware is based on the Official Firmware of Bigtreetech with the support among others of the following touch functions:

- M600
- Babystepping
- ABL
- MBL
- Z Offset
- Autotune PID
- Assisted filament loading-unloading
- Assisted E-step calibration
- UART management
- Various configurations

And all preconfigured in French and English

If you like it or would like to contribute to other improvements to this firmware, please consider the possibility of donating to:

https://paypal.me/dtouton

Thank you !


### Installation and configuration

In order to help you in installing and configuring the Firmware, please take a look at the [Wiki](https://github.com/Dtcreation/Firmware-Molise-Artillery/wiki)

#### Create a Wiki with the following data

MARLIN FW UPDATE PROCEDURES:

On the Sidewinder X1 and Genius printers, the USB port on the motherboard used to connect the printer to a PC (e.g. Octoprint) is wired to a serial bus. This bus is also shared by the TFT and the motherboard. Sharing the serial bus does not allow easy flashing of Marlin firmware due to collisions in the bus.

Three possible solutions have normally been adopted to allow Marlin firmware updates with a prerequisite, disconnecting the black and red cable from the TFT screen (definitely, this cable is mainly used to block the flash):

1) physical disconnection of the TFT serial cable so that the serial bus is no longer shared with the TFT. This solution requires removing the cover under the chassis and possibly losing all warranty.

2) Turn on the printer from the main power button (on the back of the printer)
from the TFT, press the "Menu-> Parameters-> Connection-> Disconnect" button. A black background with text asking to touch the screen to reconnect the TFT is prompted. DO NOT press the screen to keep the TFT disconnected from the serial bus.
from the PC, open the application you usually use to flash the Marlin firmware.
connect a USB cable from the PC to the USB port on the motherboard and connect the application to the printer
follow the instructions provided by your application to flash the Marlin firmware.
After the Marlin firmware is flashed, disconnect the application from the printer and restart the printer.

3) deport the TFT connection to the EXP1 port, you can then flash without any worries

![MKS_GEN_LnewTFTwiring](https://user-images.githubusercontent.com/60579620/107208792-598fb080-6a02-11eb-8e8a-aaaefea56d4c.jpg)

### Changelog

#### 4.2 First Released

- Upgrade to Marlin 2.1.2.5


# Thanks

Molise 4.x firmware is provided to you by David TOUTON, [the awesome 3D printing community on Facebook](https://www.facebook.com/groups/molisefirmware), and of course, we can't forget the team Marlin who spent countless days, nights and years building Marlin to where it is today.
