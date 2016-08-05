#Welcome!

This is a set of code and instructions for getting started with the [Riffle](test) datalogger.  Using the code in this repository, you should be able to blink the onboard LED, set the onboard Real Time Clock (RTC), and log sensor readings to the onboard microSD card.   

- If you already have experience using Arduino-compatible boards, check out the [Quick Start](https://github.com/dwblair/Riffle-Getting-Started#quick-start) section below to get up and running quickly. In general, the Riffle behaves like an Arduino UNO in the Arduino IDE (you should select "Arduino UNO" as the "Board" in the IDE), but you'll need to install a **special driver** (see [Software prep](test), below) in order to program the device over USB if you're using Mac or Windows.  

- If you would prefer more detailed instructions for setting up your Riffle, please check out the [Step-by-Step Instructions](test).

# Quick Start

## Hardware prep

- Insert a microSD card and a coin cell into the Riffle.

- Insert a lithium ion battery into the 'Lith/USB' JST connector (JST connector labels are on the back side of the board).

- Make sure that the switch on the Riffle is switched to the side labeled 'Lith/USB' (label is next to switch).

## Software prep

- Make sure that the Arduino IDE (version 1.6.10 or higher) is installed.  If it
 isn't, get it [here](https://www.arduino.cc/en/Main/Software).

- **Installing the USB-Serial Driver**. On Mac or Windows, the Riffle requires a special driver in order to be programmed via the Arduino IDE, due to the onbaord CH340 USB-Serial chip.  For Windows, you can use the driver [here]( http://raysfiles.com/drivers/ch341ser.exe).  For Mac, follow instructions [here]( http://www.instructables.com/id/Arduino-Nano-CH340/). Linux systems should generally not require additional drivers.

- Copy all of the folders in 'arduino_libraries' into the 'libraries' folder inside the 'sketchbook' folder associated with the Arduino IDE install.  These libraries are necessary for running the 'temp_logger.ino' and 'set_rtc.ino' sketches in this repo.  

## Blinking the onboard LED 

- Compile and load the 'blink.ino' sketch onto the Riffle, selecting 'Arduino UNO' as the 'Board' version in the Arduino IDE.
- This code is very similar to the standard Arduino IDE 'blink' test, except that for the Riffle, the pin connected to the onboard LED is pin 9, rather than the typical pin 13 on the UNO. This is reflected in the blink.ino sketch.

## Setting the Real Time Clock

- Using the Arduino IDE, compile and load the the 'set_rtc.ino' code onto the Riffle, using 'Arduino UNO' as the 'Board' version in the Arduino IDE. 

- Follow the prompts to set the year, month, day, hour, and second for the on-board RTC.  Once successful, the RTC will maintain the time as long as the coin cell is inserted.

## Logging values to the microSD card

(Note: for this sketch, you'll need to set the Real Time Clock (see above) in order to get sensible timestamps.  If you don't, the time stamps will still increment, but the initial time will default to Jan 1, 1970.)

- Using the Arduino IDE, compile the 'temp_logger.ino' code above, and load it onto the Riffle board, using 'Arduino UNO' as the 'Board' version in the Arduino IDE.

- The Riffle should start logging temperature values to the microSD card. These temperature values come from hardware inside the RTC. 


