# Asus [XG-C100F](https://www.asus.com/networking-iot-servers/wired-solutions/all-series/xg-c100f/) SFP+ Network Adapter

Based on the Aquantia AQC10x Chipset Now owned by Marvell </br>
works nice, has nice [Linux public drivers](https://www.marvell.com/support/downloads.html) but creates a lot of Heat. </br>
Asus also made a sister card with RJ45 [XG-C100C](https://www.asus.com/networking-iot-servers/wired-solutions/all-series/xg-c100c/) No SFP+ cage. </br>

i had many problems in the past with RJ45 connectors, the plastic tab breaks too easy, </br>
some brands of connectors, save cost on manufacture: the pastic is "the same size", </br>
but the copper blades inside that cut the cables and touch the RJ45 connector are smaller. </br>

wanted to try Fiber optic because i had good memories with ADAT Optical Light Pipe. </br>

### The Problem:

The Card Overheats if case fans are less than 1500rpm </br>
When cards Overheats too much, too long, it shuts down "self-protect" and freeze the PC </br>

This is Review about understanding why Overheats, what will happen, and how to solve it. </br>

### The Future is Clear: 
High temperature = Shorter Life = Fail. </br>

### ¿Why Overheats? 
The Heatsink looks Big & Nice, Anodized Red. </br>
PCB is also Nice Red. </br>
Eye Candy. </br>

The problem is that the Heatsink is too far apart from the AQC IC, </br>
millimeters are kilometers at that scale. </br>
has a thermal pad "low thermal transfer" >2mm or more, </br>
that barely makes contact / pressure with the heatsink "even lower thermal transfer". </br>
but still the heatsink overheats like crazy. </br>

That AQC IC is on Fire, the Red color is Not a coincidence. </br>

Heatsink distance is Fixed, has round standoffs, does Not have springs like other heatsinks. </br>
but if the spring are Not strong enough, thermal transfer also lowers. </br>

Asus XG Heatsink is Extruded aluminum, for easy manufacture... </br>
is over all the PCB, exept the SFP+ cage "U" </br>
at the factory its a very long bar cut like 3.5" x2.0" bread slices for each card. </br>
Bracket is 0.725" but Heastsink is a few milimeters shorter = could be taller / bigger = </br>
there is room for improvement, but has a "safe margin". </br>

PCB has 2 coils taller vs. the AQC10x IC, capacitors & other IC's </br>

For Proper thermal transfer, Heatsink needs to make direct contact to the IC with thermal paste </br>
but Heatsink cannot be lowered without causing a short, </br>
unless its drilled in those exact places to make room for the coils & other componets. </br>

Other options: </br>
B) lower 1mm the standoffs, and use a thinner thermal pad that touces all components of the PCB "U" </br>
C) use a small square copper "coin/penny" the size of the IC but flat, or a bit bigger, </br>
2mm or 3mm tall with thermal paste on both sides to raise the heatsink. </br>

### Alternatives:

AQC IC is very nice... was also used in Sonnet 10G Solo card, </br>
the Original 10G Solo had a smaller but taller heatsink only for the Aquantia IC. </br>
much easy & better thermal sollution, but Sonnet discontinued the 10G Solo v1. </br>
The New Sonnet 10G Solo v2 is Not the same, has different Intel IC </br>

### The 2nd Problem: 
Newer High-End Gamer boards have Faster PCIe.v5 but less PCIe lanes, </br>
"older cards" are not updated for faster PCIe. </br>
ASUS XG-C100F/C is PCIe.v2/v3.x4 </br>
Sonnet 10G Solo.v1 is PCIe.v2/v3.x4 </br>
Sonnet 10G Solo.v2 is PCIe.v2/v3.x8 = a "Dual SFP+ card" without the 2nd SFP+ </br>

Newer versions should be: </br>
PCIe.v4.x2 </br>
PCIe.v5.x1 </br>

PCIe.v3.x4 has [3.938 GB/s](https://en.wikipedia.org/wiki/PCI_Express#Comparison_table) = 31.5 Gbp/s </br>
PCIe.v2.x4 has [2.0 GB/s](https://en.wikipedia.org/wiki/PCI_Express#Comparison_table) = 16 Gbp/s </br>
PCIe.v2.x8 has [4.0 GB/s](https://en.wikipedia.org/wiki/PCI_Express#Comparison_table) = 32 Gbp/s </br>
PCIe.v3.x8 has [7.877 GB/s](https://en.wikipedia.org/wiki/PCI_Express#Comparison_table) = 63 Gbp/s </br>

The card is 10G Full Duplex = 20Gbp/s per SFP+ </br>

placing a card designed for v2 or v3 PCIe lanes on a PCIe v4 or v5 does Not become magically v4 or v5. </br>
the boards autodetects the speed and runs slower. </br>
can be forced on the UEFI, but electric signals & protocols are Not the same. </br>

intel 12,13,14gen LGA1700 has 20 lanes, AM5 has 24 PCIe lanes. </br>
Older boards used special PCIe bifurcation IC's like Nvidia NF200 to have more PCIe.x16.v2 lanes. </br>
modern boards can be upgraded to have more PCIe.v5 & v4 lanes with PCIe expansion chassis. </br>
but are not cheap. </br>

most modern boards today: </br>
Z790, Z890, X680e, B650 have 1x or 2x PCIe.x1 that are near useless for today technology. </br>
some boards have PCIe.v4.x4 but is designed for Thunderbolt 4 / USB4 PCIe cards. </br>
Those cards are a "Must have" If like to Boot different Linux from USB4 at 40Gbps </bt>
or move PCIe cards using TB3 eGPU extenal chasis to other machines. </br>

some boards also have USB3.2 2x2 20Gbps, but requires an optional "Not included bracket" </br>
Out of the Box: USB3.2 2x2 does Not work, if case does Not have the weird connector. </br>

purchasing an external PCIe chassis for 1x card? 
TB3/4 eGPU chassis or direct PCIe external chassis ? </br>
¿using the x4 slot? ¿Not use TB4/USB4 card? </br>
Thunderbolt card probably cannot be used on the external PCIe chassis. </br>
Nor on the TB3 eGPU chasis. </br>
it gets tricky to expand modern boards. </br>

The board Z790, x670 or B650: </br>
msome boards have dual x4/x4 slots, one dedicated only for the TB4/USB4 card. </br>
some high-end boards allow dual x8/x8.v5 instead of the main PCIe.v5.x16 </br>
but the main PCIe.v5.x16 is also "shared" with the M.2 PCIe.v5.x4 </br>

when sharing lanes, "bifurcation" and you change the M.2 card from v5 to v4 UEFI goes crazy, </br>
thinks its a short circuit "self-protects" does Not turn-on, after many attempts / time, </br>
boots again, but takes a lot of time on a Black Scren doing "self-tests", before going to UEFI boot menu. </br>

in my experience is Not a good idea to share / bifurcate PCIe lanes, and change M.2 drive. </br>
is much better to use a PCIe.x4 to M.2 NVMe card to swap OS / Boot drives. </br>
boots instantly, does Not go crazy, works flawless. </br>

you lose the M.2 PCIe.v5 at Full speed, must go back to v4, but feels better Not sharing lanes. </br>
you get gray hair on the "self-protection" phase & loose time on the "self-test" phase. </br>

M.2 v5 is faster, but if something goes wrong, UEFI goes crazy, because its bifurcated / sharing lanes. </br>
using an external PCIe.v5 chassis should have No problems swapping M2 drives on PCIe cards. </br>

### Thunderbolt vs. Direct PCIe expansion vs. Both </bt>
Direct PCIe is always better, but more High-End. </br>
Thunderbolt3/4/5 eGPU is more consumer / gamer. </br>

Thunderbolt [eGPU.io list](https://egpu.io/best-egpu-buyers-guide/) </br>

#### Direct PCIe: </br>
[RocketStor 8631D:](https://www.highpoint-tech.com/gen5-copprlink-enclosure) </br>
1x internal PCIe.v5.x16 -to-> 1x external PCIe.v5.x16 </br>
[Razer Core X-Chroma:](https://www.razer.com/mena-en/gaming-laptops/razer-core-x) </br>
1x Thunberbolt3 -to-> 1x external PCIe.v3.x16 </br>
[Razer Core X](https://www.razer.com/mena-en/gaming-egpus/razer-core-x-v2) [V2:](https://mysupport.razer.com/app/answers/detail/a_id/14797/~/razer-core-x-v2-%7C-rc21-0227-support-%26-faqs) </br>
1x Thunberbolt5/4 -to-> 1x external PCIe.v4.x16 </br>
Magma expansaion chassis were very popular during the ProTools TDM, HD era, </br>
Now owned by OneStopSystems, older Magma chassis like EB7 were PCIe.v2 or PCI-X </br>
[PCIe expansion](https://onestopsystems.com/collections/expansion) </br>
Host/Target PCIe cards: </br>
[PCIe.v4.x16](https://onestopsystems.com/products/pcie-x16-gen-4-cable-adapter) </br>
[PCIe.v3.x16](https://onestopsystems.com/products/pcie-x16-gen3-ipass-cable-adapter) </br>
(+) cables + Backplane board. </br>
The other extreme are the Startech: </br>
[Large](https://www.startech.com/en-us/cards-adapters/4pcie-pcie-enclosure) PCIe.v2.x2 -to-> 4x PCIe.x1 </br>
[Small](https://www.startech.com/en-us/cards-adapters/pex2pci4) 1x PCIe.x1 -to-> 4x PCI 32-Bit </br>
[Large](https://www.startech.com/en-us/cards-adapters/pex2pcie4l) 1x PCIe -to-> 2x PCIe.x1 + 2x PCI 32-bit </br>
