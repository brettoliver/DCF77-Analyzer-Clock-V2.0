 DCF77 Analyzer/Clock v2.0
 Differences between Eric's Clock and my clock

Although based on Eric's clock I have made a few changes to the hardware. Please mix and match whatever option suits your needs but make sure you change the code to suit.

I use two custom made Arduino UNOs on the Vero board rather than a Uno and a Mega.

I use cheap 7 segment displays and dot matrix modules from China throughout and have changed the code to match. See the section on display errors as they work really well once these mods are carried out.

I use 2x  JQ6500 modules rather than the Adafruit sound board. As one of my boards is software controlled there are some software changes and another library to load.

As I have a Arduino Uno instead of a Arduino Mega I do not have all the spare pins to drive the decoder LEDs so I use a 3rd dot matrix module instead.

I have modified Udo Klein's Super Filter by adding extra status LED's. The brightness of these LEDs are PWM controlled by the DCF77 decoder Uno via 2 transistors not the Super Filter Uno.

There is also an LED test function added to the Super Filter to match the DCF77 decoder test funtion.

I only use 3mm LEDs and have chosen matched brightness LEDs to try and keep the brightness uniform.

I have added 4 seperate intensity levels in software so the Ring/Status LEDs, the large 7 segment displays, the small 7 segment displays and the Super Filter LEDs all have custom brightness levels depending on the readings from the single LDR.

I don't have a temperature or week number display on my clock and have modified the code to suit. 

I have added extra monitor LEDs to my Super Filter so on my clock there is only an option for Synthesized and Non Synthesized output. This is not switchable.

The DCF77 Sound on my clock has been modified to accentuate the difference between the incoming 0s and 1s. When the clock detects a 1 it just plays a slightly longer sound than 200mS.

See details here Web site: http://www.brettoliver.org.uk/DCF77_Analyzer_Clock_Mk2/Arduino_DCF77_Analyzer_MK2.htm

![alt tag](https://raw.githubusercontent.com/brettoliver/DCF77-Analyzer-Clock-V2.0/master/DCF77_Animation_1000.gif)
