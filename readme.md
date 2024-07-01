# Massey Ferguson Electroluminescent Driver
Based upon the Steve Pietkiewicz of LTC Electroluminescent Panel Power Supply in [Linear Technology Application Note 61](https://www.analog.com/media/en/technical-documentation/application-notes/an61fa.pdf) August 1994
Project never long term tested due to only having one Electroluminescent gauge left on the tractor which was cloudy so just decided to use 12V modern gauges.  Thought more were EL gauges, but they were just burned out 12v lamps.  Simply completed this to learn Kicad with a usedful project before moving on to more complex things.

## Features
- Adjustable Voltage and Frequency
> After searching everything on line could not find the specifications for this old of a tractor so made sure it was adjustable to fine tune brightness.
- Square wave output centered around 0
- Case with mounting points for zip ties
> Ended up mounting it to the vibration dampening mount that the voltage regulator was previously on.  Tractor has a internally regulated alternator so it was no longer needed.  It could also be attached to the bolt pattern on the existing EL driver instead.

## Known Issues
- +5V pin of the 555 timer not routed.  Fixed on board with a jumper wire
- resistor between the output of the 555 timer and the transistor needs a current limiting resistor between
- Potentiometer choices I ordered allowed for too large of a voltage swing which ended up bruning out my voltage regulator.  To fix this I used a generic boost converter I had lying around from 12v to 90v from that fit in the case as I did not want to wait on shipping of a new lienar regulator.  [Boost Converter](https://www.amazon.com/gp/product/B09P3MTC4J/ref=ppx_yo_dt_b_asin_title_o00_s01?ie=UTF8&psc=1).  I simply spliced this before the last diode in the multiiplier in order to inject the power directly.