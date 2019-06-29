# gps-reference
GPS-Referenced Programmable Precision Signal Generator

**Current state:** Alpha
**Next steps:** Procure the board, the components, assemble & test.

This is the do-it-yourself version of the u-Blox-based GPS-Referenced Programmable Precision Signal Generator.

This design is largely inspired by [ZL2PD design](https://www.zl2pd.com/GPS_Freq_Ref.html) and features a few other stuff, like break-out headers for I2C, Serial, USB, External Battery and antenna selector.

The [schematics](/Schematics) are in Autodesk Eagle CAD format.

There are two signal outputs; one DC-coupled, suitable for logic level output and an AC-coupled output.

There is a [Gerber](https://github.com/rfrht/gps-reference/raw/master/Design/gps-gerbers.zip) for ordering a PCB from your favourite PCB shop, as well [Digi-Key](/Design/gps-bom.csv) Bill of Materials, which currently costs around $27 (including the u-blox M8 IC).

## Board pictures:
Top:
![Board front](https://github.com/rfrht/gps-reference/raw/master/Design/gps-top.png)

Bottom:
![Board back](https://github.com/rfrht/gps-reference/raw/master/Design/gps-bottom.png)
