# GPS-Referenced Programmable Precision Signal Generator

**Current state:** Alpha

**Next steps:** Procure the board, the components, assemble & test.

This is the do-it-yourself version of the u-Blox-based GPS-Referenced Programmable Precision Signal Generator. While this is **not** a [GPS-Disciplined Oscillator](https://en.wikipedia.org/wiki/GPS_disciplined_oscillator) but a [Numerically Controlled Oscillator](https://en.wikipedia.org/wiki/Numerically_controlled_oscillator) instead.

This is not all sad news - RA3APW [did some some extensive research (Russian content)](http://www.ra3apw.ru/proekty/ublox-neo-7m/) and found that there are a few frequencies where there is some very good precision for the general hobbyist, yielding precision between 0.1 PPM to 1 PPB.

The great frequencies are, namely:

| Frequency |
| --- |
|24.000 MHz |
|16.000 MHz |
|12.000 MHz |
|8.000 MHz |
|6.000 MHz |
|4.000 MHz |
|3.000 MHz |
|2.000 MHz | 

Bear in mind that the RA3APW tested U-Blox M-7 hardware, while in this project we will be using the new [NEO-M8Q-01A Automotive grade](https://www.u-blox.com/en/product/neo-m8q-01a-module) version which sports a TCXO, (hopefully) increasing precision.

This board design is largely inspired by [ZL2PD design](https://www.zl2pd.com/GPS_Freq_Ref.html) and features a few other stuff, like break-out headers for I2C, Serial, USB, External Battery and antenna selector.

The [schematics](/Schematics) are in Autodesk Eagle CAD format.

There are two signal outputs; one DC-coupled, suitable for logic level output and an AC-coupled output.

There is a [Gerber](https://github.com/rfrht/gps-reference/raw/master/Design/gps-gerbers.zip) for ordering a PCB from your favourite PCB shop, as well [Digi-Key](/Design/gps-bom.csv) Bill of Materials, which currently costs around $27 (including the u-blox M8 IC).

## Board pictures:
Top:

![Board front](https://github.com/rfrht/gps-reference/raw/master/Design/gps-top.png)

Bottom:

![Board back](https://github.com/rfrht/gps-reference/raw/master/Design/gps-bottom.png)

## TODO:
The current design does not contains provisions for Active antennas, this is slated to appear in Revision B.
