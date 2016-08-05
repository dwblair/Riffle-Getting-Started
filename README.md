This repository contains basic code for getting started with the Riffle datalogger version 0.1.8.  For those familiar with the Arduino, the [Quick Start](https://github.com/dwblair/Riffle-Getting-Started#quick-start) section is probably sufficient documentation for getting to the point of logging temperature values onto a microSD card using the Riffle.

For those unfamiliar with the Arduino, consult the [wiki] for more detailed step-by-step instructions, with pictures.

# Quick Start

## Hardware prep

- Insert a microSD card and a coin cell into the appropriate locations on the Riffle.

- Insert a lithium ion battery into the appropriate JST connector on the Riffle (labeled 'Lith/USB' on the back of the board).

- Make sure that the switch on the Riffle is switched to the side labeled 'Lith/USB'.

## Software prep

- Make sure that the Arduino IDE (version 1.6.10 or higher) is installed.  If it
 isn't, get it [here](https://www.arduino.cc/en/Main/Software).

- Copy all of the folders in 'arduino_libraries' into the 'libraries' folder inside the 'sketchbook' folder associated with the Arduino IDE install.  These libraries are necessary for running the 'temp_logger.ino' and 'set_rtc.ino' sketches in this repo.  

## Blinking the onboard LED 

- Complie and load the 'blink.ino' sketch onto the Riffle.
- The code is very similar to the standard Arduino IDE 'blink' test, except that for the Riffle, the pin connected to the onboard LED is pin 9, rather than the typical pin 13 on the UNO. This is reflected in the code.

## Setting the Real Time Clock

- Using the Arduino IDE, ompile and load the the 'set_rtc.ino' code onto the Riffle.

- Follow the prompts to set the year, month, day, hour, and second for the on-board RTC.  Once successful, the RTC will maintain the time as long as the coin cell is inserted.

## Logging values to the microSD card

(Note: for this sketch, you'll need to set the Real Time Clock (see above) in order to get sensible timestamps.  If you don't, the time stamps will still increment, but the initial time will default to Jan 1, 1970.)

- Using the Arduino IDE, compile the 'temp_logger.ino' code above, and load it onto the Riffle board.

- The Riffle should start logging temperature values to the microSD card. These temperature values come from hardware inside the RTC. 


