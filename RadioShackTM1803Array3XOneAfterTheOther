//Jeff Thompson - 3/15/2014
//Arduino 1.05-r2 required
// ArrayOfLedArrays.  In this example, we're going to set up three Radio Shack TM1803 strips on three
// different pins, each strip getting its own CRGB array to be played with, only this time they're going
// to be all parts of an array of arrays.
// Uncomment/edit one of the following lines for your leds arrangement.
// FastLED.addLeds<TM1803, DATA_PIN, RGB>(leds, NUM_LEDS);
// FastLED.addLeds<TM1804, DATA_PIN, RGB>(leds, NUM_LEDS);
// FastLED.addLeds<TM1809, DATA_PIN, RGB>(leds, NUM_LEDS);
// FastLED.addLeds<WS2811, DATA_PIN, RGB>(leds, NUM_LEDS);
// FastLED.addLeds<WS2812, DATA_PIN, RGB>(leds, NUM_LEDS);
// FastLED.addLeds<WS2812B, DATA_PIN, RGB>(leds, NUM_LEDS);
// FastLED.addLeds<NEOPIXEL, DATA_PIN>(leds, NUM_LEDS);
// FastLED.addLeds<UCS1903, DATA_PIN, RGB>(leds, NUM_LEDS);
// FastLED.addLeds<UCS1903B, DATA_PIN, RGB>(leds, NUM_LEDS);
// FastLED.addLeds<GW6205, DATA_PIN, RGB>(leds, NUM_LEDS);
// FastLED.addLeds<GW6205_400, DATA_PIN, RGB>(leds, NUM_LEDS);
// FastLED.addLeds<WS2801, RGB>(leds, NUM_LEDS);
// FastLED.addLeds<SM16716, RGB>(leds, NUM_LEDS);
// FastLED.addLeds<LPD8806, RGB>(leds, NUM_LEDS);
// FastLED.addLeds<WS2801, DATA_PIN, CLOCK_PIN, RGB>(leds, NUM_LEDS);
// FastLED.addLeds<SM16716, DATA_PIN, CLOCK_PIN, RGB>(leds, NUM_LEDS);
// FastLED.addLeds<LPD8806, DATA_PIN, CLOCK_PIN, RGB>(leds, NUM_LEDS);

#include "FastLED.h"

#define NUM_STRIPS 3
#define NUM_LEDS_PER_STRIP 10
CRGB leds[NUM_STRIPS][NUM_LEDS_PER_STRIP];
void setup() {
  // 10 leds on pin 6
  FastLED.addLeds<TM1803, 6>(leds[0], NUM_LEDS_PER_STRIP);
  FastLED.addLeds<TM1803, 7>(leds[1], NUM_LEDS_PER_STRIP);
  FastLED.addLeds<TM1803, 8>(leds[2], NUM_LEDS_PER_STRIP);
}

void loop() {
  // outer loop goes over each strip, one at a time
  for(int x = 0; x < NUM_STRIPS; x++) {
  // inner loop goes over each led in the current strip, one at a time
    for(int i = 0; i < NUM_LEDS_PER_STRIP; i++) {
      leds[x][i] = CRGB::Red;
      FastLED.show();
      leds[x][i] = CRGB::Black;
      delay(100);
    }
  }
}
