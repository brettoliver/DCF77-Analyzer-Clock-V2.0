 DCF77 Analyzer/Clock v2.0


 This sketch is free software; you can redistribute it and/or
 modify it under the terms of the GNU Lesser General Public
 License as published by the Free Software Foundation; either
 version 2.1 of the License, or (at your option) any later version.
 
 This sketch is distributed in the hope that it will be useful,
 but WITHOUT ANY WARRANTY; without even the implied warranty of
 MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU
 Lesser General Public License for more details.
 
 You should have received a copy of the GNU Lesser General Public
 License along with this library; if not, write to the Free Software
 Foundation, Inc., 51 Franklin St, Fifth Floor, Boston, MA  02110-1301  USA


 Differences between Eric's Clock and my clock

Although based on Eric's clock I have made a few changes to the hardware. Please mix and match whatever option suits your needs but make sure you change the code to suit.

I use two custom made Arduino UNOs on the Vero board rather than a Uno and a Mega.

I use cheap 7 segment displays and dot matrix modules from China throughout and have changed the code to match. See the section on display errors as they work really well once these mods are carried out.

I use 2x  JQ6500 modules rather than the Adafruit sound board. As one of my boards is software controlled there are some software changes and another library to load.

As I have a Arduino Uno instead of a Arduino Mega I do not have all the spare pins to drive the decoder LEDs so I use a 3rd dot matrix module instead.

I have modified Udo Klein's Super Filter by adding extra status LED's. The brightness of these LEDs are PWM controlled by the DCF77 decoder Uno via 2 transistors not the Super Filter Uno.

There is also an LED test function added to the Super Filter to match the DCF77 decoder test funtion.

I only use 3mm LEDs and have chosen matched brightness LEDs to try and keep the brightness uniform.

I have added 4 seperate intensity levels in software so the Ring/Status LEDs, the large 7 segment displays, the small 7 segment displays and the Super Filter LEDs 

all have custom brightness levels depending on the readings from the single LDR.

I don't have a temperature or week number display on my clock and have modified the code to suit. 

I have added extra monitor LEDs to my Super Filter so on my clock there is only an option for Synthesized and Non Synthesized output. This is not switchable.

The DCF77 Sound on my clock has been modified to accentuate the difference between the incoming 0s and 1s. When the clock detects a 1 it just plays a slightly longer sound than 200mS.

                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            

 

 


 */

