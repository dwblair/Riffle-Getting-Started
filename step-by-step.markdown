# Riffle Hardware Overview 

Battery port options.  Voltage range.  Lithium Ion battery charger port.  General battery charger port.
MicroUSB -- for powering board, programming board, charging lithium ion battery if it's plugged in.
Power LED indicates plugged in to USB power / charging
Blinking LED.  
MicroSD card slot
Inputs / outputs on end of board
Pins on bottom of board
Coin cell battery CR1220 (for RTC)

# Basic test of hardware: Blinky
Riffle pre-programmed with "blink" code that blinks the LED every 1 second.
Plug the Riffle into USB power to test it. Does it blink? It works!

# Programming the Riffle 

Here we'll  1) Install a USB-Serial driver, 2) Install the Arduino IDE, 3) Install necessary Arduino Libraries 4) Load a driver

## Installing the USB-Serial chip (Ch340) driver

Windows
Mac
Restart computer

## Install the Arduino IDE

Download the program from arduino.cc.  Version 1.6.5 or later
If you've installed the driver correctly, then the Tools: Ports menu should tell you whether there is a device connected

## Install the necessary libraries

Download from the github repo
Drag all folders into the sketchbook / libraries folder

## Compile and Load the Blink code
blink

## Basic datalogging
Open the datalogger sketch
Compile and load it
Log for a while
Turn off device and check contents on card

-----

Notice to folks:
Going to be using github 
Version-control documents
Please file questions / suggestions as github 'issues'


