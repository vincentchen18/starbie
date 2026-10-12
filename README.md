# Starbie

## Overview

Starbie is a tiny motion controlled desktop pet, powered by USB or battery. It is a star-shaped PCB hosting a little digital creature on an OLED Screen. It includes multiple interactive functionalities. Tilt it to navigate menus, shake it to wake it up, and watch its mood light change as you neglect it. (you probably shouldn't neglect it but this is also a functionality, not a recommendation.) Also has multiple sensors that track gyroscopic and accelerometric position, as well as tracking temperature and humidity.

This project was built for Hack Club's hardware program [Half Life](https://halflife.hackclub.com/), a 10 week YSWS to help beginners learn hardware project, and incidentally, it is ***my*** first hardware project!!! :DDD

I will also note that this is based off a tutorial from one of Half Life's organisers, and you can find the tutorial repo [here](https://github.com/SharKingStudios/Starbie). I added some additional features myself, but thank you [SharKingStudios](https://github.com/SharKingStudios/) this tutorial as it was a great starting point.

Additionally, I have also created a storage case for Starbie (although it is irregularly shaped due to how I shaped the printed circuit board)

## Schematic, PCB and Components

![Schematic render](Journal/img_5.png)

The final schematic is shown in the above picture, featuring a XIAO-ESP32-C3, Environment and MPU6050 sensor, as well as a menu button and an on/off switch as well as a battery connector. 

The desktop pet can be powered both by battery or by USB connection

![PCB render](Journal/img_10.png)


## Features

- **Wandering pet:** a 32×32 pixel creature walks across the OLED.
- **Tilt-controlled radial menu:** press the menu button, then tilt to pick an option, and press again to select the option. The interactive options are:
- --> **Nap:** Starbie just falls asleep with zzz's until you shake it to wake it up
- --> **Play:** Starbie sprints in laps with hearts
- --> **Feed:** Starbie wiggles and jumps and gains fullness
- --> **Pet:** Increases Starbie's joy
- **Stats:** Joy, Energy, and Fullness, saved to flash so they save when you turn Starbie back on
- **Shake to wake:** shaking it wakes it and gets a reaction
- **Environment sensing:** Starbie can detect the temperature (and it **will** complain if it's too hot or cold!)
- **RGB Mood Light**: this shows how starbie is feeling:
Dark blue: napping
Pink: being loved
Red: too hot!
ice blue: too cold!
amber: hungry or tired
green: happy (brighter = morer happierness)
purple: dizzy

## Hardware

A storage case for Starbie has also been included, and you can find the box and lid STEP files in [`3D Models`](3D%20Models/)

Full list in [`BOM.csv`](Starbie/BOM.csv). Gerbers in [`gerbers/`](Starbie/gerbers/).

## Firmware

Arduino IDE was used to program Starbie.

## AI Usage

AI was not used in any way for this project besides as a guide to help me learn to use KiCad

## Bill of Materials

### Grant-funded ($30 tier 1)

| Item | Purpose | Qty | Unit (USD) | Total (USD) | Link |
|---|---|---|---|---|---|
| Starbie PCB (2-layer, 97.3×140.3mm) | Custom star-shaped board | 5 | 2.12 | 10.60 | [JLCPCB](https://jlcpcb.com/quote) |
| JLCPCB New User PCB coupon | Discount | 1 | -6.00 | -6.00 | — |
| JLCPCB shipping (Global Standard Direct Line → AU) | Shipping | 1 | 8.52 | 8.52 | [JLCPCB](https://jlcpcb.com/quote) |
| Seeed Studio XIAO ESP32-C3 | Main microcontroller | 1 | 6.31 | 6.31 | [AliExpress](https://www.aliexpress.com/item/1005008791664713.html) |
| 0.96" 128×64 I2C OLED (SSD1306) | Display | 1 | 2.20 | 2.20 | [AliExpress](https://www.aliexpress.com/item/1005006262908701.html) |
| DHT11 (bare 4-pin) | Temp + humidity sensor | 1 | 1.60 | 1.60 | [AliExpress](https://www.aliexpress.com/item/1005008818897051.html) |
| MPU-6050 (GY-521) | Accelerometer/gyro for tilt + shake | 1 | 1.03 | 1.03 | [AliExpress](https://www.aliexpress.com/item/1005008604349573.html) |
| 5mm RGB LED, common cathode (pack) | Mood light | 1 | 2.17 | 2.17 | [AliExpress](https://www.aliexpress.com/item/32601543257.html) |
| Resistor kit, 1/4W 300pcs (10k + 220Ω used) | DHT11 pull-up + LED current limiting | 1 | 3.23 | 3.23 | [AliExpress](https://www.aliexpress.com/item/1005011772534173.html) |
| **Grant total** | | | | **29.66** | |

### Paid out of pocket

| Item | Purpose | Qty | Unit (USD) | Total (USD) | Link |
|---|---|---|---|---|---|
| Gateron G Pro 3.0 MX switches (pack) | MENU + STATS buttons | 1 | 4.02 | 4.02 | [AliExpress](https://www.aliexpress.com/item/1005010559544082.html) |
| AliExpress shipping + 10% GST | Shipping + tax | 1 | 6.51 | 6.51 | — |
| **Out-of-pocket total** | | | | **10.53** | |

**Project total: $40.19**