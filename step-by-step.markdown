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

<img src="pics/blink.gif">

If there is no blink, check your USB power source.  If your power source seems to be okay, there may be a problem with the Riffle hardware, or it may have been programmed improperly.

# Install the Arduino IDE

- Download the Arduino IDE (version 1.6.5 or later) for your operating system (Mac, Windows, Linux) from [the arduino website](http://arduino.cc), and install it.

# Install the USB-Serial driver

The Riffle communicates with a laptop or computer via a USB-Serial chip (called the 'CH340') that requires that a special driver be installed on your computer (if you're using Mac or Windows -- no special driver required for Linux).  

### Mac

Follow the instructions [here](http://www.instructables.com/id/Arduino-Nano-CH340/) for downloading and installing the CH340 driver for Mac.  

Notes from people who've done this:

- Once you've downloaded the ch34xinstaller.pkg file, you'll need to unzip it -- this may happen automatically.  
- If following the Instructables linked above and downloading the driver from the linked source there, and you are running OS X Yosemite, try downloading the driver without the additional step of opening a terminal and typing in the special code, as it has worked without that step (at least for one person).

Here are some screenshots of the process:

<img src="pics/mac_install_1.png">

### Windows

### Linux

# Riffle programming basics: blink


# Basic datalogging


### Install the necessary Arduino libraries

Download from the github repo
Drag all folders into the sketchbook / libraries folder
Open the datalogger sketch
Compile and load it
Log for a while
Turn off device and check contents on card

