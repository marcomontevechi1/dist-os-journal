---
layout: post
title:  "Buying the hardware and assembling it"
date:   2025-02-17
categories: hardware
---

1. [Main components](#main_components)
2. [Assembly](#assembly)\
  2.1 [Cabling](#cabling)\
  2.2 [Zipties, cabling, screws...](#fixing)\
3. [Estimated price](#price)
4. [Improvements](#improvements)

I could have started with virtual machines, but nah.

## Main components <a name="main_components"></a>

- 4 [Odroid N2+](https://www.hardkernel.com/shop/odroid-n2-with-4gbyte-ram-2/) with 4GB RAM each (specs can be seen in manufacturer's website);
- 4 [12V 2A generic power sources](https://www.amazon.se/Velain-Strömadapter-12V-2A-24W/dp/B07JLGHSFJ/ref=asc_df_B07JLGHSFJ/?tag=shpngadsglede-21&linkCode=df0&hvadid=476521591633&hvpos=&hvnetw=g&hvrand=7339316985373344424&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=1012442&hvtargid=pla-943339581105&psc=1&mcid=a9d473f2869334f2968b6da76a771a94), 5.5mm outer diameter, 2.1 inner diameter;
- 1 [8-Port gigabit switch GSW1008](https://www.kjell.com/se/produkter/natverk/tradburet-natverk/switchar/plexgear-gigabitswitch-8-portar-p93669?utm_source=google&utm_medium=cpc&utm_campaign=SE%20%7C%20MM%20%7C%20Standard%20Shopping&gad_source=1&gclid=CjwKCAiA2cu9BhBhEiwAft6IxNc8FC6Dx0T22HdT7kYysBPODezMs5MdHDc-AGKMJm8LOCFSTbvMaBoCKg0QAvD_BwE), along with it's power source;
- 5 Gigabit Ethernet cables;
- 2 [three-way outlet ruler](https://www.ikea.com/se/en/p/koppla-3-way-socket-earthed-white-80412016/) from IKEA (tried one 5-way but couldn't make all the power sources fit and didn't want to open them to make them smaller);
- 4 [128GB sandisk SD cards](https://www.proshop.se/Flashram-USB-Flash-Drives/SanDisk-Ultra-microSDSD-140MBs-128GB/3120859?srsltid=AfmBOoqgKroOTCWJ_H_RVzbLbVKg-cUDnCGkHIF1xN0N7O8NjybsxBtN);
- 4 Lithium 3V batteries for the BIOS clock (optional);
- Zipties. A lot of them;
- A pretty place to put it all together. I chose a [Skådis](https://www.ikea.com/se/sv/p/skadis-foervaringstavla-vit-10321618/) board from IKEA.

I already had a monitor, an hdmi cable and a keyboard.
I could add active refrigeration, but the manufacturer and several users seem to have a consensus that Odroids hold pretty well with just the heat sinks. So for now I am <s>happy</s> content.

## Assembly. <a name="assembly"></a>

Does it look pretty? No. But am I proud of it? Also, no.

<img src="/assets/grumpy.png" alt="Im-not-proud" width="200"/>

### Cabling <a name="cabling"></a>
Unfortunately, the holes in the board are too small to pass the power source connectors, so I couldn't hide them behind the board.
It's big enough for the small power source cables, though, so I could probably cut the connectors, pass the cables and re-connect them.
It's not big enough for the power outlet ruler cables, though. They are too thick.

Everything is connected via the switch and to my main router. After booted, each system got it's own IP normally via the local DHCP server.

### Zipties, cabling, screws... <a name="fixing"></a>
The board was bolted to my wall with little effort, it seems to hold out pretty well.\
The switch and power ruler are actually fixed to the board with double tape and zipties, just to be extra sure.\
The actual Odroid boards are fixed both by zipties and two screws each. The holes in the heat sink don't seem made for this particular
kind of bolting since if you go too deep the screw ends up touching the board PCB trails or connections, so I went as deep as possible
but without risking scraping the board.

<img src="/assets/bad_space.jpeg" alt="Bad-space" width="400"/>

![assembly](/assets/cluster.jpeg)

## Estimated price <a name="price"></a>

I bought it all in very different places and moments so I most certainly don't remember what was the actual cost of each component.
This is a rough estimate.

- Odroids plus delivery: $83 * 4 + $19.49 * 2 (I ordered two boards twice instead of once of four boards). Total $370.98.
- Power sources plus delivery (price varied, I bought some in different places): about $14 each. Total $56.
- Switch with power supply (no delivery, bought at store): about $46.
- Ethernet cables: about $14 each. Total about $70.
- Power outlet rulers: about $7.50 each. Total $15.
- SD cards: about $19 each. Total about $74.
- Lithium batteris: about $4 for a box with four.
- Zipties: $10 for a bag full of those.
- Skådis board:  about $20.

Estimated total: ~ $665.98 or 7.124 SEK.
If you plan better than I did you certainly can build this spending much less.

## What could be improved? <a name="improvements"></a>

Adding fans or active refrigeration (although Odroids seem to hold well with just the heat sink), hide the cables behind the board, use proper Ethernet cable length...

I also didn't plan buying the components in advance and just bought it as I figured out I would need, so probably the costs could be greatly reduced.