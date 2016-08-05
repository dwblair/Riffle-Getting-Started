#Welcome!

This is a set of code and instructions for getting started with the [Riffle](test) datalogger.  Using the code in this repository, you should be able to blink the onboard LED, set the onboard Real Time Clock (RTC), and log sensor readings to the onboard microSD card.   

- If you already have experience using Arduino-compatible boards, check out the [Quick Start](https://github.com/dwblair/Riffle-Getting-Started#quick-start) section below to get up and running quickly.

- If you would prefer a more detailed description, check out the [Step-by-Step Instructions](test).

# Quick Start

## Hardware prep

- Insert a microSD card and a coin cell into the appropriate locations on the Riffle.

- Insert a lithium ion battery into the appropriate JST connector on the Riffle (labeled 'Lith/USB' on the back of the board).

- Make sure that the switch on the Riffle is switched to the side labeled 'Lith/USB'.

## Software prep

- Make sure that the Arduino IDE (version 1.6.10 or higher) is installed.  If it
 isn't, get it [here](https://www.arduino.cc/en/Main/Software).

- On Mac or Windows, the Riffle requires a special driver in order to be programmed via the Arduino IDE.  For Windows, you can use the driver [here]( http://raysfiles.com/drivers/ch341ser.exe).  For Mac, follow instructions [here]( http://www.instructables.com/id/Arduino-Nano-CH340/).

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


