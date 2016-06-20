# [fit] Hardware, Hula Hoops, & Flow
## Lindsey Bieda	

🐦 @lindseybieda | 🎮 ekko#11472

---

## Who?

- Software Engineer (at Articulate)
- Beginner hula hooper
- Novice hardware tinkerer
- 🍵🍵🍵🍵

![](https://i.imgur.com/P2MwoCF.jpg)

---

## Hardware
- $$$ Barrier to entry (getting cheaper)
- Intimidating
- How do I start without electrocuting myself?

![](https://i.imgur.com/X5s0Fwj.jpg)

---

![left](https://upload.wikimedia.org/wikipedia/en/2/2a/HandyBoard_GJP.jpg)
![right](https://cdn-shop.adafruit.com/970x728/1500-06.jpg)

### Handyboard: $200
- 68HC11 8-bit microcontroller @ 2 MHz
- 32KB battery-backed SRAM

### Trinket: $7
- ATtiny85 8-bit microcontroller @ 8 MHz
- 512 byte of SRAM

---

## Hula Hooping

- $20 barrier to entry
- Hey I used to do that as a kid
- Wait that looks hard

![](http://i.imgur.com/mhJoOY4.jpg)

---

## Let's figure out an approach
### Using SCIENCE!

1. Internets!
2. Friends
3. Failure?

![left](http://i.imgur.com/bzYjIpu.jpg)

---

# Flow

![](https://static.pexels.com/photos/6832/waterfall-beauty-lets-explore-lets-get-lost.jpg)

---

## Flow

- When you are fully immersed in a task and have an energized focus
- Mihály Csíkszentmihályi (Me-High Cheek-sent-me-high)


### High Skill + High Challenge = Flow

![](http://i.imgur.com/I0EaR4W.jpg)

---

# High Challenge?

![right](http://www.eventstrategy.nl/wp-content/uploads/2012/01/flow-diagram1-1024x1024.jpg)

---

> "Enjoyment appears at the boundary between boredom and anxiety"
-- Mihály Csíkszentmihályi

---

## Why care about flow?

- Helps in improving skill
- Intellectually and emotionally stimulating
- Fun!

---

> "[Flow] makes the present instant more enjoyable, and it builds the self-confidence that allows us to develop skills..."
-- Mihály Csíkszentmihályi

---

## Recall:

- Hardware: high challenge
- Hula hooping: high challenge

---

# Let's Flow!

![](http://cdn.themis-media.com/media/global/images/library/deriv/999/999693.jpg)

---

# LED Hula Hoop steps:

1. Design
2. Solder
3. Code
4. Dance


![](https://www.wired.com/wp-content/uploads/blogs/magazine/wp-content/images/19-07/ff_feedbackloop_f.jpg)

--- 

# Chance for flow at every step!

---

# Mistakes Happen

![](http://www.teamjimmyjoe.com/wp-content/uploads/2015/02/open-sign-you-had-one-job.jpg)

---

# Things Break

![](http://i.imgur.com/gh72t99.jpg)

---

# The Hoop Will Drop
#### Curse you gravity

![](http://blogs-images.forbes.com/erikkain/files/2015/08/Gravity-Falls.png)

---

# This is okay!

---

# This is GOOD!

![](http://images-cdn.moviepilot.com/images/c_scale,h_818,w_1920/t_mp_quality/jnzn3tcvh5gp2s3g1o4t/is-palpatine-the-supreme-leader-snoke-from-star-wars-the-force-awakens-760329.jpg)

---

# Hard things are important to flow

---

# Flow is good for your brain

![left fit](http://vomzi.com/wp-content/uploads/2016/02/45-im-so-excited-gif-466.gif)

---

# Therefore, hard things are good for your brain 

---

## Failure is just a step on the way to a happy brain! 💙 

---
![inline](https://i.imgur.com/KJUyVUh.png)

---

![inline](http://i.imgur.com/GSx09fC.png)

---

```C
#include <Adafruit_NeoPixel.h>
#ifdef __AVR__
  #include <avr/power.h>
#endif

#define PIN 0

Adafruit_NeoPixel strip = Adafruit_NeoPixel(40, PIN, NEO_GRB + NEO_KHZ800);

void setup() {
  strip.setBrightness(127);
  strip.begin();
  strip.show(); // Initialize all pixels to 'off'
}

void loop() {
  uint16_t i;
  uint16_t c = 1;
  
  // go through all the pixels and change the color
  for(i=0; i<strip.numPixels(); i++){
    strip.setPixelColor(i, c, c, c);
  }
  
  c++; // increment the color
  delay(20); // sleep for a bit so we can see it
}

```
---

```c
void loop() {
  uint16_t i;
  uint16_t c = 1;
  
  for(i=0; i<strip.numPixels(); i++){
    strip.setPixelColor(i, c, c, c);
  }
  
  c++;
  delay(20);
}
```

---

# Flicker fusion threshold:

## Around 13 milliseconds

---

# Basic electronics kit (or MVHardware stuff)
- Soldering iron (hopefully with a stand)
- Solder
- Desoldering pump
- Helping hand tool

---


# Thank you 

![](http://www.gravitybong.net/files/public/1462855220_1259_FT79802_kviqmdnismrznvlxbyjm.gif)

--- 

# Some kits to practice soldering
- [Make: Color Visualizer Kit](http://www.makershed.com/products/color-visualizer-kit)
- [Solder: Time II Watch Kit](http://www.makershed.com/products/solder-time-ii-watch-kit-1)
- [LED Dice (Die) Kit ](http://www.makershed.com/products/led-dice-die-kit)
- [Adafruit MintyBoost USB Charger Kit](http://www.makershed.com/products/mintyboost-usb-charger-kit-v3-0)
- [MiniPOV 4 Kit - DIY Full-Color POV and Light Painting Kit](https://www.adafruit.com/products/1776) (my first ever)
- [Conway's Game of Life Kit](https://www.adafruit.com/products/89)

---

# References & Resources

- Flow by Mihaly Csikszentmihalyi
- Beyond Boredom and Anxiety by Mihaly Csikszentmihalyi
- [Adafruit Guide To Excellent Soldering](https://learn.adafruit.com/adafruit-guide-excellent-soldering/)
- [Adafruit NeoPixel Überguide](https://learn.adafruit.com/adafruit-neopixel-uberguide/overview)
- [Instructables: Make a Hula Hoop](http://www.instructables.com/id/Make-a-Hula-Hoop/)