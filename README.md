# AutoShield
Inspired by Prusa and 3DVerkstan, the AutoShield is designed to print faster and support automated bed removal for continuous printing.

Maybe we're biased, but we also think it's the prettiest.

See it in action: https://youtu.be/gVObd0i1pr8
Find it at Prusa: https://www.prusaprinters.org/prints/28435-autoshield-automatic-bed-removal-face-shield

The band is designed for the Prusa MK3S printers and PrusaSlicer's draft profile, vase mode, with 0.8mm external perimeters. We're using 0.4mm nozzles, but 0.6 or 0.8mm would work great as well with the appropriate gcode changes.

Use automatic bed removal with CAUTION. The extruder is not designed to be used as a battering ram, but that's exactly what we're doing! Be prepared to stop the print and for the extruder fan or fan mount to break over time. Some combinations of print beds, filaments, and z-heights may need tweaking of the printer and/or gcode. This is working on our printers, but YMMV!

To perform the automated bed removal, we edited the start and end gcode to print the purge line on the Y axis and to cool the bed prior to pushing the band off. To reduce cooling time, the extruder moves to the center of the band and turns on the part cooling fan to accelerate cool down.

For continuous printing, we duplicated the gcode for one part and manually adjusted the placement of the purge line in the X direction.

To reduce print time further, we added instructions to change the print speed multiplier to 150% when vase mode starts and to start reducing the bed temperature at 12mm z-height.


