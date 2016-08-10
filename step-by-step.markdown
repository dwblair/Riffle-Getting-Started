# Overview

This repo will cover:

- A quick [overview of the Riffle hardware](./step-by-step.markdown#riffle-hardware): switches, indicator lights, and battery ports 
- A basic ['Blink' test of the hardware](./step-by-step.markdown#basic-test-of-hardware): (does the on-board LED blink?)

As well as the required steps for setting yourself up to program a Riffle: 

- [Installing the Arduino IDE](./step-by-step.markdown#installing-the-arduino-ide) on a desktop or laptop computer
- [Installing a required driver](./step-by-step.markdown#installing-the-usb-serial-driver) for communicating between your computer and the Riffle
- A simple 'blink' test of programming capability

Finally, we cover the steps necesary for programming a Riffle to do basic datalogging:

- Downloading Riffle datalogging software from github
- Installing the required Arduino IDE libraries
- Compiling the code and loading the code onto the Riffle

# Riffle Hardware 

### Power sources

The Riffle can use power sources with voltages between 3.7 Volts and 6 Volts. 

- It can be powered via the microUSB port on the end of the Riffe. 
- It can be powered via either of the two JST ports on the end of the Riffle.  One of these ports is labeled "USB/Lith", and should only be used with a 3.7 V Lithium Ion battery.  The other is labeled "Gen", for 'general', and can be used with any voltage source (any battery chemistry) between 3.7 and 6 Volts.  

### Power switch

The power switch on the Riffle can be in two positions: 

- "USB / Lith", which draws power from the USB port and/or the "USB/Lith" JST battery port;
- "Gen", which draws power from the "Gen" battery port.

Since the Riffle is only connected to one of these two power sources at a time, the switch acts as an 'on/off' switch.

### LEDs

There is an LED at the end of the board to indicated that the Riffle is plugged into USB power.

There is also an LED in the middle of the board.  It is connected to pin #9, and can be used as an indicator LED.


### MicroSD card slot

A slot for a microSD card is at the end of the board, for data storage

### Coin cell battery slot

A coin cell battery (of type CR1220) is at the center of the board.  This coin cell is used to power the on-board real-time clock (RTC).

# Basic test of hardware: blink

The Riffle comes pre-programmed with "blink" code that blinks the indicator LED every 1 second.

- Plug the Riffle into USB power, via the microUSB port.
- Make sure that the onboard switch is set to "USB/Lith".
- You should see the Riffle blinking every 1 second or so.

<img src="pics/blink.gif" width=200>

If there is no blink, check your USB power source.  If your power source seems to be okay, there may be a problem with the Riffle hardware, or it may have been programmed improperly.

# Install the Arduino IDE

- Download the Arduino IDE (version 1.6.5 or later) for your operating system (Mac, Windows, Linux) from [the arduino website](http://arduino.cc), and install it.

# Install the USB-Serial driver

The Riffle communicates with a laptop or computer via a USB-Serial chip (called the 'CH340') that requires that a special driver be installed on your computer (if you're using Mac or Windows -- no special driver required for Linux).  

### Mac

Follow the instructions [here](http://www.instructables.com/id/Arduino-Nano-CH340/) for downloading and installing the CH340 driver for Mac. The instructions link to a download to the Mac driver; we have also placed a copy of the latest driver [here](usb-serial-drivers/CH341SER_MAC.ZIP).  

Notes from people who've done this:

- Once you've downloaded the ch34xinstaller.pkg file, you'll need to unzip it -- this may happen automatically.  
- If following the Instructables linked above and downloading the driver from the linked source there, and you are running OS X Yosemite, try downloading the driver without the additional step of opening a terminal and typing in the special code, as it has worked without that step (at least for one person).

Here are some screenshots of the process:

<img src="pics/mac_install_1.png"><img src="pics/mac_install_2.png"><img src="pics/mac_install_3.png"><img src="pics/mac_install_4.png">

### Windows

Download and install the driver [here](usb-serial-drivers/ch341ser.exe), following the prompts.

### Linux

No driver needed for Linux.

# Riffle programming basics

- Connect the Riffle to a USB port via the microUSB connector on your board.
- Make sure that the Riffle switch is set to "USB/Lith".
- Open the Arduino IDE.
- Board selection:  From the 'Tools' menu, select 'Board: Arduino/Genuino Uno'
- Port selection: in the 'Tools' menu, you must select the 'port' that the Riffle is connected to.  The precise name of this port will change depending on the operating system.  Here is a snapshot of a properly selected port on a Mac:  <img src="pics/tools_port.png">.  

(**Note about the usb-serial driver**:  if you are unable to locate a Riffle in the "Ports" menu, the USB-Serial driver may not have installed properly. Some people have found that restarting the computer helps.)

- Select "File: Examples: 01 Basics: Blink"

<img src="pics/arduino_blink.png">

- Edit every instance of '13' to '9' in the code.  (The standard Arduino UNO has its indicator LED connected to pin 13; on the Riffle it is connected to pin 9). 
 
<img src="pics/blink_edit.png">

- Change the 'delay' rate to 500 milliseconds (or something significantly different from 1000 milliseconds, which is the blinking rate that the Riffle comes pre-programmed to display).

<img src="pics/blink_rate.png">

- Compile and load the code using the 'right arrow' button:

<img src="pics/compile_load.png">

- After the code has uploaded, you should see that the blink rate on the Riffle has changed to the blink rate you have programmed it to.

# Basic datalogging

### Install the necessary Arduino libraries

Download from the github repo
Drag all folders into the sketchbook / libraries folder
Open the datalogger sketch
Compile and load it
Log for a while
Turn off device and check contents on card

