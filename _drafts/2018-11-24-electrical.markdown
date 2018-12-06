---
layout: post
title:  "Electrical"
date:   2018-11-24 00:00:00 -0400
categories: update
---

The house's electrical system has low-enough power needs that it can be powered
by a standard extension cord, but has the hardware to handle a more serious
double-pole direct connection to a main panel if it's needed in the future.

<!--more-->

{% include youtube-light-embed.html%}

# SIP electrical rough-in

Unlike traditional stick frame structures, a SIP building's electrical layout
is not easily modified after the design phase. Electrical wire chases are built
into the panels when they are manufactured, and adding them later is painful because
you can't cut the OSB skin without negating the panel's strength.

So the electrical system was almost fully planned out before ordering the panels,
and electrical rough-in involved drilling holes through the OSB into the existing
wire chases at both ends of an electrical run and pulling the wire through with fish
tape.

<div class="youtube-player" data-id="RQ5G_AKgbzs"></div>
{% include caption.html text="Electrical rough-in in the SIP panels." %}

# Power supply

I've tried to design the house to work with variety of power supply options.
From simply plugging the house into an electrical outlet (tiny-house-as-an-appliance
setup), to wiring a permanent connection to a main panel, to plugging into a camper electric
service pole if you're not set up near a house.

This flexibility is possible by minimizing the power usage of the house while
installing hardware that can handle higher power demands than it currently requires.

## Tiny house as an appliance: 20A 120V

Keeping the power requirements of the tiny house low allows the simplest supply setup:
just plug it in to an outlet as if it's just a big appliance. If the tiny house is set
up near a not-tiny house, as this one is now, the not-tiny house will likely have a 20 Amp
outdoor outlet.

The power requirements are kept low in the following ways:

1. [2-burner induction cooktop][induction-cooktop]: This modest cooktop draws a max of 15 Amps
at 120V. It'll be a serious struggle to cook an 8 course feast, but it should be enough for 1 to 2
people, and it doesn't require more power than a standard extension cord can supply the
house.
1. [Propane tankless water heater][water-heater]: An electric tankless water heater is a power guzzler
(on the order of 12K Watts for an application like this) that would necessitate a
serious electrical supply (50A 240V). I decided the added pain of dealing with a propane
system (learning to work with propane, copper piping, venting, etc.) was worth it to
keep the convenience of simply plugging the house in with an extension cord.
1. [LED lighting][armacost]: All the lights are dimmable LED and the whole system uses about 48 Watts
at 100% brightness.
1. Energy-concious behavior: Even with the above low power appliances, casual non-conservative electrical
usage could still easily exceed the 20 Amp allotment. If one turned on both stove burners
and simultaneously fired up the coffee pot (all while the range hood, minisplit, fridge, and
lights are on) that's already 20 Amps. They'd trip the breaker in the main house and
need to walk over to reset it before continuing breakfast, this time finishing the
coffee first before cooking the eggs and pancakes. If one is willing to live conscious of
their energy usage like this, the tiny-house-as-an-appliance setup could work permanently.
But if they think that sounds too annoying they'll want to go with one of the other supply options.

Besides requiring energy-conciousness, the other limitation of the tiny-house-as-an-appliance
approach is [voltage drop][voltage-drop]. The longer the distance of the extension cord, the
greater the voltage drop (the `R` goes up in `V = IR`).
This limits how far the tiny house can be from the main house, which could be less ideal for
privacy. __TODO__ measure voltage drop of my setup.

## Getting more power

If one finds the limitations of the tiny-house-as-an-appliance setup outweigh the benefits, they
can go with a more substantial power supply. A few options:

1. Single pole (120V) from a 50 Amp breaker.
1. Double pole (240V), this will require some rewiring of the subpanel in the tiny house

These options are possible because I've chosen hardware that can handle a more serious power supply
__(up to 240V ....)__

![Electrical feeder hardware](https://images.ctfassets.net/rwi5x73ignkx/2oRz3TFJvuQsW8gIwyO8wQ/3513ea0010c2143f0f4b02e2bd73a9b2/electrical-feeder.jpg?w=1170)
{% include caption.html text="Feeder hardware. Components labeled and detailed below." %}

1. Outdoor outlet on the main house: 1-pole 120V. In my setup this outlet is on a 20 Amp circuit.
2. Extension cord. Mine needs to run about 100 feet, so I made my own extension cord out of
[10-2 wire][10-2] (thicker wire than a typical extension cord) to prevent too much voltage drop.
3. ["Dogbone" connector][dogbone]: This serves 2 functions. First as an adapter to connect the
receptacle end of the extension cord power inlet box twist-lock plug (plug/receptacle
[NEMA codes][nema-plugs] labeled in the diagram). The second function is to split the 120V single
pole input coming from the extension cord across both hot conductors of the power inlet. This is
the key to having 2-pole 240V compatible hardware in the tiny house but powering it with a 1-pole
120V extension cord.
4. [50 Amp Power inlet][power-inlet]: This is the first component that is a permanent part of the
tiny house (it's mounted to the underside). From this component on the system can handle 50A 240V.
This could be quite useful someday if one decides the small cooktop isn't powerful enough, or they
don't want to deal with propane anymore and would prefer an electric water heater.
5. [6-3 wire][6-3]: 6 gauge 3 conductor (+ ground) NM cable connects the inlet plug to the electrical
panel.
6. [Electrical panel][panel]: I'm using a 6-space panel that's rated up to 100 Amps. This takes the
incoming power and branches it out to my circuits, with a breaker at each branch for protection. I've
wired the panel as a subpanel, meaning the neutral and ground are separate.

<div class="youtube-player" data-id="pMgzgNgaTds"></div>
{% include caption.html text="Wiring the panel and testing the circuits." %}

# Circuits

Here is how the circuits are organized:

![Circuits](https://images.ctfassets.net/rwi5x73ignkx/3EVI6YixiUgWAeU4YC6iEo/7daf217f2236a9ffeeb73e0677ca56c2/circuits.jpg?w=1170)

Here are links to the breakers I used:
[20A AFCI][20a-afci]. [20A GFCI/AFCI][20a-afci-gfci]. [15A AFCI][15a-afci]. [15A Tandem][15a-tandem].

{% include carousel.html
  img1="https://images.ctfassets.net/rwi5x73ignkx/fEloDX9Xs4WoGoI6GAO4K/d5a748aeb69055cca5b73873dbc8c695/IMG_20180329_202449.jpg?w=1170"
  img2="https://images.ctfassets.net/rwi5x73ignkx/5s4v6KVmQo2MIAiS0Aqmy4/b336a0cc814b797b682293035d50b864/IMG_20180329_202435.jpg?w=1170"
%}
{% include caption.html text="Electrical panel close ups." %}

# Code And Safety

__*Full Disclosure*__: I'm not an electrician, nor has my work been officially inspected for compliance
with NEC codes. I have done my best to research and follow electrical codes, built in some extra
safety measures, and had an unofficial inspection of my panel and rough-in by an electrician.

Some misc notes:

- Grounding: In addition to the ground connection back to the main panel through the feeder
cable, my electrician friend recommended adding a grounding electrode at the tiny house subpanel. I
ran a 6-gauge wire from the subpanel's ground bar out through the bottom that can be attached to
a grounding rod when the tiny house comes to its permanent location. The propane system CSST and
the metal trailer frame are both bonded to the system ground.
- Wire gauge: I'm using 12-gauge wire everywhere (except some sections of the
[low voltage LED System][led-section]) (__TODO update <-- link to posts__) even though none of
the circuits draw more than 15 Amps. Only 14-gauge wire is required by code in that case, but
thicker wire ⇨ less resistance ⇨ less heat ⇨ more safety in case of unexpected power draw.
- Ground Fault + Arc Fault protection
  - [GFCI][gfci]: Ground fault circuit interrupters protect people from electric shock. The sensor expects
		to see all current moving from hot to neutral. If that is not the case, it means the electricity
		is taking another return path (such as a person's body -- ouch, or dead), and the GFCI shuts off
		the circuit. GFCI is required by code in wet areas (bathroom + kitchen). I've installed GFCI outlets
		in the kitchen, and in the bathroom used a GFCI breaker for protection of the whole circuit.
  - [AFCI][afci]: Arc fault circuit interrupters are a fire prevention measure. They detect and
		prevent unwanted electrical paths and the extreme heat produced along those paths. AFCI
		is required by code to protect all receptacles in dwelling areas.

# LED Lighting

I used [Armacost][armacost] LED lighting. I learned about their products through [shedsistence][shedsistence]
but it turns out the company is based near me in Baltimore, which is cool. They have plenty of
documentation about how their systems work, but some things I think are worth mentioning about their
12V DC system:
  - Their LED lights run on low voltage 12V DC current. So you need to convert the 120V AC to 12V DC
		with their power supply bricks.
  - At low voltages like 12V, voltage drop is a more pronounced issue. I used thick 12-gauge wire for most
		of the LED wiring, not for safety (there isn't safety code around 12V circuits as the voltage
    is too low to shock people or cause fires) but to cut down on resistance therefor voltage drop.
  - If 12V DC wiring and 120V AC wiring run in parallel, the cycling of the AC current can induce
		flickering in the LED lighting. So you need to layout your wiring such that there is always 6"
		between your DC and AC wires, and where they must come close they should cross perpendicularly.

![LED lights in kitchen](https://images.ctfassets.net/rwi5x73ignkx/1GcDQ2kQzm2YMucUeIkGsk/7c5ec643540595d3ffdbbcaa7df96d5f/kitchen-leds.jpg?w=1170)

[induction-cooktop]: https://www.amazon.com/True-Induction-MD-2B-Portable-Counter/dp/B019KZXVHE/ref=sr_1_1?s=kitchen&ie=UTF8&qid=1498567253&sr=1-1&keywords=induction+cooktop
[water-heater]: https://www.eccotemp.com/eccotemp-i12-indoor-3-0-gpm-liquid-propane-tankless-water-heater/
[armacost]: http://www.armacostlighting.com/store/
[voltage-drop]: https://en.wikipedia.org/wiki/Voltage_drop
[10-2]: https://www.homedepot.com/p/Southwire-100-ft-10-2-Solid-Romex-SIMpull-CU-NM-B-W-G-Wire-28829028/202316241
[dogbone]: https://www.amazon.com/gp/product/B002CCLFUI
[nema-plugs]: https://www.coxhardware.com/pdf_files/NemaPlugChart.pdf
[power-inlet]: https://www.amazon.com/Conntek-80SS2-WTBX-CS6365-Temporary-Generator/dp/B013GGACCU
[6-3]: https://www.amazon.com/gp/product/B00QJEGJHY
[panel]: https://www.homedepot.com/p/Square-D-QO-100-Amp-6-Space-12-Circuit-Indoor-Flush-Mount-Main-Lug-Load-Center-with-Cover-Door-QO612L100DF/100209798
[afci]: https://en.wikipedia.org/wiki/Arc-fault_circuit_interrupter
[gfci]: https://en.wikipedia.org/wiki/Residual-current_device
[20a-afci]: https://www.homedepot.com/p/Square-D-QO-20-Amp-Single-Pole-AFCI-Circuit-Breaker-QO120AFIC/100077019
[20a-afci-gfci]: https://www.homedepot.com/p/Square-D-QO-20-Amp-Single-Pole-Dual-Function-CAFCI-and-GFCI-Circuit-Breaker-QO120DFC/204844647
[15a-afci]: https://www.homedepot.com/p/Square-D-QO-15-Amp-Single-Pole-Combination-Arc-Fault-Circuit-Breaker-QO115CAFIC/202353327
[15a-tandem]: https://www.homedepot.com/p/Square-D-QO-2-15-Amp-Single-Pole-Tandem-Circuit-Breaker-QOT1515CP/100076261
[shedsistence]: https://shedsistence.com/
[armacost]: http://www.armacostlighting.com/store/
[led-section]: {{ site.baseurl }}{% link _drafts/2018-11-24-electrical.markdown %}#led-lighting
