FastLED NeoPixels
Scripts for Adafruit(NEOPIXEL) & RadioShack leds(TM1803).
If RadioShack leds are pale cyan & pink use Arduino 1.05-r2

Uncomment/edit one of the following lines for your leds arrangement.

FastLED.addLeds<TM1803, DATA_PIN, RGB>(leds, NUM_LEDS);
FastLED.addLeds<NEOPIXEL, DATA_PIN>(leds, NUM_LEDS);
