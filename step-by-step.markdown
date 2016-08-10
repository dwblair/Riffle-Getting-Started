# Overview

This repo will cover:

- A quick [overview of the Riffle hardware](./step-by-step.markdown#riffle-hardware): switches, indicator lights, and battery ports 
- A basic ['Blink' test of the hardware](./step-by-step.markdown#basice-test-of-hardware): (does the on-board LED blink?)

As well as the required steps for setting yourself up to program a Riffle: 

- Installing the Arduino IDE on a desktop or laptop computer
- Installing a required driver for communicating between your computer and the Riffle
- A simple 'blink' test of programming capability

Finally, we cover the steps necesary for programming a Riffle to do basic datalogging:

- Downloading Riffle datalogging software from github
- Installing the required Arduino IDE libraries
- Compiling the code and loading the code onto the Riffle

# Riffle Hardware 

Battery port options.  Voltage range.  Lithium Ion battery charger port.  General battery charger port.
MicroUSB -- for powering board, programming board, charging lithium ion battery if it's plugged in.
Power LED indicates plugged in to USB power / charging
Blinking LED.  
MicroSD card slot
Inputs / outputs on end of board
Pins on bottom of board
Coin cell battery CR1220 (for RTC)

# Basic test of hardware

Riffle pre-programmed with "blink" code that blinks the LED every 1 second.
Plug the Riffle into USB power to test it. Does it blink? It works!

# Install the Arduino IDE

Download the program from arduino.cc.  Version 1.6.5 or later
If you've installed the driver correctly, then the Tools: Ports menu should tell you whether there is a device connected


# Installing the USB-Serial chip (Ch340) driver

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
