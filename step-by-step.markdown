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

# Basic test of hardware

Riffle pre-programmed with "blink" code that blinks the LED every 1 second.
Plug the Riffle into USB power to test it. Does it blink? It works!

# Install the Arduino IDE

Download the program from arduino.cc.  Version 1.6.5 or later
If you've installed the driver correctly, then the Tools: Ports menu should tell you whether there is a device connected


# Installing the USB-Serial driver

Windows
Mac
Restart computer


# Install the necessary Arduino libraries

Download from the github repo
Drag all folders into the sketchbook / libraries folder

# Compile and load the 'Blink' code
blink

# Basic datalogging
Open the datalogger sketch
Compile and load it
Log for a while
Turn off device and check contents on card

