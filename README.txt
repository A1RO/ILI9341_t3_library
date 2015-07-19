The source of this library has been modified to work with the multi-font library Adafruit_mfGFX by pkourany - you will need to also download and include the Adafruit_mfGFX library and include in your sketch:

http://github.com/pkourany/Adafruit_mfGFX_Library

Discussion regarding multi-font support:

http://forum.pjrc.com/threads/27510-ILI9341_t3-Library-Fonts

In addition to the Adafruit_GFX and mfGFX functions there is now a gradient fill function which fills the screen with a specified two colour gradient. Use the function as follows:

tftInstance.fillGrad(24_bit_RGB_colour_1, 24_bit_RGB_colour_2)            // fills screen with two colour vertical gradient
tftInstance.fillGrad(24_bit_RGB_colour_1, 24_bit_RGB_colour_2, fillOrientationFlag)  // fills screen with two colour gradient
                                                                                     // false = vertical, true = horizontal

*note that the colours are converted from 24bitRGB to 16bit (565) format for this display. 24bit colours are used as an input because these are easier to experiment with on a graphics editer first before putting values into your code. Colours should be declared as HEX values 0x000000 -> 0xFFFFFF where MSB = Red, bytes 3 & 4 = Green, LSB = Blue.

------------------------------------------

Discussion regarding this optimized version:

http://forum.pjrc.com/threads/26305-Highly-optimized-ILI9341-%28320x240-TFT-color-display%29-library

------------------------------------------

This is a library for the Adafruit ILI9341 display products

This library works with the Adafruit 2.8" Touch Shield V2 (SPI)
  ----> http://www.adafruit.com/products/1651
 
Check out the links above for our tutorials and wiring diagrams.
These displays use SPI to communicate, 4 or 5 pins are required
to interface (RST is optional).

Adafruit invests time and resources providing this open source code,
please support Adafruit and open-source hardware by purchasing
products from Adafruit!

Written by Limor Fried/Ladyada for Adafruit Industries.
MIT license, all text above must be included in any redistribution

To download. click the DOWNLOADS button in the top right corner, rename the uncompressed folder Adafruit_ILI9341. Check that the Adafruit_ILI9341 folder contains Adafruit_ILI9341.cpp and Adafruit_ILI9341.

Place the Adafruit_ILI9341 library folder your arduinosketchfolder/libraries/ folder. You may need to create the libraries subfolder if its your first library. Restart the IDE

Also requires the Adafruit_GFX library for Arduino.
