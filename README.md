# Asus XG-C100F SFP+ Network Adapter

Based on the Aquantia AQC10X Chipset Now owned Marvell </br>
works nice, has nice [Linux public drivers](https://www.marvell.com/support/downloads.html) but creates a lot of Heat. </br>
There is a sister card with RJ45 Only XG-C100C No SFP+ cage. </br>

The Card Overheats if case fans are less than 1500rpm </br>
When cards Overheats too much, it shuts down "self-protect" and freeze the PC </br>

This is about understanding why Overheats, what will happen on the future, and how to solve it. </br>

### The Future is Clear: 
High temperature = Shorter Life = Fail. </br>

### ¿Why Overheats? 
The Heatsink looks Big & Nice, Anodized Red. </br>
PCB is also Nice Red. </br>
Eye Candy. </br>

The problem is that the Heatsink is too far apart from the AQC IC, </br>
milimeters are kilometers at that scale. </br>
has a thermal pad "low thermal transfer" >2mm or more, </br>
that barely makes contact / pressure with the heatsink "even low thermal transfer". </br>
and still the heatsink overheats like crazy. </br>

That AQC IC is on Fire, the Red color is Not a coincidence. </br>

Heatsink distance is Fixed, has round standoffs, does Not have springs like other heatsinks. </br>
The reason is because Heatsink is Extruded aluminum, for easy manufacture... </br>
is over all the PCB, exept the SFP+ cage, </br>
at teh factory its a very long bar cut like 3.5" bread slices for each card. </br>

But PCB has 2 coils taller vs. the AQC10x IC, something else & capacitors </br>
that means: </br>
Heatsink cannot be lowered without causing a short, to make direct contact with thermal paste </br>
unless its drilled in those exact places to make room for the coils. </br>

Other option is to lower 1mm the standoffs, and use a thinner thermal pad that touces all components of the PCB. </br>

### Alternatives:

AQC IC is very nice... was also used in Sonnet 10G Solo card, </br>
the Original 10G Solo had a smaller but taller heatsink only for the Aquantia IC. </br>
much easy & better thermal sollution, but Sonnet discontinued the 10G Solo v1. </br>
The New Sonnet 10G Solo v2 is Not the same, had different Intel IC </br>

The ASUS is PCIe.v3.x4 </br>

### The Problem: 
Newer Gamer boards have less PCIe lanes available, </br>
intel 12,13,14 LGA1700 has 20 lanes, AM5 has 24 PCIe lanes. </br>

most Z790m Z890, X680, B650 boards have PCIe.x1 that is near useless for today technology. </br>
some boards have PCIe.x4 but is designed for Thunderbolt 4 / USB4 PCIe cards. </br>
Those cards are a "Must have" If you like to Boot different Linux distros from USB4 at 40Gbps </bt>
some boards also have USB3.2 2x2 20Gbps, but requires a optional "Not included bracket" </br>
Out of the Box, USB3.2 2x2 does Not work, if your case does Not have the weird connector. </br>

