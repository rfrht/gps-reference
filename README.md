# GPS-Referenced Programmable Precision Signal Generator

**Current state:** Project Stage. [Issues](https://github.com/rfrht/gps-reference/issues)

**Next steps:** Procure, build, assemble, test.

## Overview

This is the do-it-yourself version of the u-Blox-based **GPS-Referenced Programmable Precision Signal Generator**.

In this version/revision, there's a Si5351-C clock generator driven by the GPS signal, hoping to be able to get more and cleaner signals using the GPS as a reference. See the [schematic](/gps-schematics.pdf).

The I²C bus is shared between the U-Blox and the Si5351C device. The clock signal level is TTL 3.3V.

The board was inspired by [ZL2PD design](https://www.zl2pd.com/GPS_Freq_Ref.html) and features a few other stuff, like break-out headers for I2C, Serial, USB, External Battery and antenna selector.

RA3APW [did some some extensive research (Russian content)](http://www.ra3apw.ru/proekty/ublox-neo-7m/) and found that there are a few frequencies where there is some very good precision for the general hobbyist, yielding precision between 0.1 PPM to 1 PPB. This is not a [GPS-Disciplined Oscillator](https://en.wikipedia.org/wiki/GPS_disciplined_oscillator) but a high precision [Numerically Controlled Oscillator](https://en.wikipedia.org/wiki/Numerically_controlled_oscillator) instead.

Bear in mind that the RA3APW tested U-Blox M-7 hardware, while in this project we will be using the newer generation [NEO-M8Q-01A Automotive grade](https://www.u-blox.com/en/product/neo-m8q-01a-module), which sports a [TCXO](https://en.wikipedia.org/wiki/Crystal_oscillator#Temperature), (hopefully) increasing precision.

## Frequencies

The tested high reliability frequencies are, namely:

| Frequency | Frequency |
| --- | --- |
| [300 kHz](https://rf3.org:8443/q/gps/gps-ref-300-khz.png) | [500 kHz](https://rf3.org:8443/q/gps/gps-ref-500-khz.png) |
| [1 MHz](https://rf3.org:8443/q/gps/gps-ref-1-mhz.png) | [1.2 MHz](https://rf3.org:8443/q/gps/gps-ref-1-2-mhz.png) |
| [1.5 MHz](https://rf3.org:8443/q/gps/gps-ref-1-5-mhz.png) | [1.6 MHz](https://rf3.org:8443/q/gps/gps-ref-1-6-mhz.png) |
| [2 MHz](https://rf3.org:8443/q/gps/gps-ref-2-mhz.png) | [2.4 MHz](https://rf3.org:8443/q/gps/gps-ref-2-4-mhz.png) |
| [3 MHz](https://rf3.org:8443/q/gps/gps-ref-3-mhz.png) | [4 MHz](https://rf3.org:8443/q/gps/gps-ref-4-mhz.png) |
| [4.8 MHz](https://rf3.org:8443/q/gps/gps-ref-4-8-mhz.png) | [6 MHz](https://rf3.org:8443/q/gps/gps-ref-6-mhz.png) |
| [8 MHz](https://rf3.org:8443/q/gps/gps-ref-8-mhz.png) | [12 MHz](https://rf3.org:8443/q/gps/gps-ref-12-mhz.png) |
| [24 MHz](https://rf3.org:8443/q/gps/gps-ref-24-mhz.png) | --- |

There are certainly others. It seem to follow some mathematical order, but I failed to figure out the proper sequence.

### Good frequency waveform
This is a 1 MHz waveform:

![1 MHz GPS-Referenced signal](https://rf3.org:8443/q/gps/gps-ref-1-mhz.png)

### Non-optimal frequencies
Check this 16 MHz signal, there are harmonics along the main waveform:

![16 MHz unsuitable waveform](https://rf3.org:8443/q/gps/gps-ref-16-mhz.png)

This is how the problem manifests in low frequencies. Check the falling edge of a 360 kHz:

![360 kHz signal](https://rf3.org:8443/q/gps/gps-ref-360-khz.png)

## Configuration
Use the [U-Blox U-Center](https://www.u-blox.com/en/product/u-center) tool to configure your board. Open the Config page, in `TP5 (Timepulse 5)` menu and configure as per the below screenshot:

![U-Blox Signal Generator configuration](https://rf3.org:8443/q/gps/gps-ref-ublox-config.png)

*U-Blox Configuration page - Click to enlarge*

## Artefacts

The [schematics](/Schematics) are in Autodesk Eagle CAD format.

There is a [Gerber](https://github.com/rfrht/gps-reference/raw/master/Design/gps-gerbers.zip) for ordering a PCB from your favourite PCB shop (Hint: $2 in jlcpcb.com for 5 units), as well a Digi-Key friendly [Bill of Materials](/Design/gps-bom.csv), which currently costs around $27 (including the GPS module).

## Board pictures:
Board:

![Board front](https://rf3.org:8443/q/gps/gps-referenced-oscillator.jpg)

Cabled (with external wire antenna):
![Cabled GPS Referenced Board](https://rf3.org:8443/q/gps/gps-referenced-cabled.jpg)

## TODO:
Check [Issues](https://github.com/rfrht/gps-reference/issues)
