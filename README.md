# Asus [XG-C100F](https://www.asus.com/networking-iot-servers/wired-solutions/all-series/xg-c100f/) SFP+ Network Adapter

Based on the Aquantia AQC10x Chipset Now owned Marvell </br>
works nice, has nice [Linux public drivers](https://www.marvell.com/support/downloads.html) but creates a lot of Heat. </br>
Asus also made a sister card with RJ45 Only [XG-C100C](https://www.asus.com/networking-iot-servers/wired-solutions/all-series/xg-c100c/) No SFP+ cage. </br>

i had many problems in the past with RJ45 connectors, the plastic tab breaks too easy, </br>
some brands of connectors, save cost on manufacture: the pastic is "the same size", </br>
but the copper blades that cut the cables and touch the RJ45 connector are smaller. </br>

i wanted to try Fiber optic because i had good times with ADAT Optical Light Pipe. </br>

### The Problem:

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
at teh factory its a very long bar cut like 3.5"x2.0"bread slices for each card. </br>
Bracket is 0.725" but Heastsink is a few milimeters shorter = could be taller / bigger </br>
there is room for improvement. </br>

PCB has 2 coils taller vs. the AQC10x IC, something else, capacitors & other IC's </br>
The idea is to make direct contact: Heatsink-to->IC with thermal paste </br>
Heatsink cannot be lowered without causing a short, </br>
unless its drilled in those exact places to make room for the coils & other componets. </br>

Other option is to lower 1mm the standoffs, and use a thinner thermal pad that touces all components of the PCB. </br>

### Alternatives:

AQC IC is very nice... was also used in Sonnet 10G Solo card, </br>
the Original 10G Solo had a smaller but taller heatsink only for the Aquantia IC. </br>
much easy & better thermal sollution, but Sonnet discontinued the 10G Solo v1. </br>
The New Sonnet 10G Solo v2 is Not the same, had different Intel IC </br>

### The 2nd Problem: 
Newer High.End Gamer boards have faster PCIe.v5 but less PCIe lanes available, </br>
and "older cards" are not updated for New faster PCIe. </br>
ASUS XG-C100F/C is PCIe.v3.x4 </br>
Sonnet 10G Solo is PCIe.v3.x4 </br>
Newer versions should be: </br>
PCIe.v4.x2 </br>
PCIe.v5.x1 </br>

intel 12,13,14 LGA1700 has 20 lanes, AM5 has 24 PCIe lanes. </br>
Older boards used special PCIe bifurcation IC's like Nvidia NF200 to have more PCIe lanes. </br>
modern boards can also be upgraded to have more PCIe lanes with PCIe expansion chassis. </br>

most modern boards today: </br>
Z790, Z890, X680e, B650 boards have PCIe.x1 that is near useless for today technology. </br>
some boards have PCIe.v4.x4 but is designed for Thunderbolt 4 / USB4 PCIe cards. </br>
Those cards are a "Must have" If you like to Boot different Linux distros from USB4 at 40Gbps </bt>
or move PCIe cards using TB3 eGPU extenal chasis to other machines. </br>

some boards also have USB3.2 2x2 20Gbps, but requires a optional "Not included bracket" </br>
Out of the Box, USB3.2 2x2 does Not work, if your case does Not have the weird connector. </br>

