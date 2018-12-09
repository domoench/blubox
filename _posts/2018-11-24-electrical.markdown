---
layout: post
title:  "Electrical"
date:   2018-11-24 00:00:00 -0400
categories: update
---

This tiny house's power needs are low enough that it can be powered by an extension
cord, but can also handle a 240V direct connection to a main panel for more power if needed
in the future.

<!--more-->

{% include youtube-light-embed.html%}

# SIP electrical rough-in

The electrical system had to be fully planned before ordering the SIPs.
Unlike traditional stick-frame structures, a SIP building's electrical layout
is not easily modified after the design phase. Internal electrical wire chases are
manufactured into the panels according to the designs, and adding more later is
painful because you can't cut the OSB skin without negating the panel's strength.

Electrical rough-in involved drilling holes through the OSB into the chases at
both ends of each electrical run and pulling Romex through with fish tape.

<div class="youtube-player" data-id="RQ5G_AKgbzs"></div>
{% include caption.html text="Electrical rough-in in the SIPs." %}

# Power supply

I've tried to design the electrical system to be compatible with a multiple power
supply options. From simply plugging the house into an electrical outlet (tiny-house-as-an-appliance
setup), to wiring a permanent connection to a main panel, to plugging into a camper electric
service pole.

This flexibility is possible because the power demands of the house are low and
the system's hardware can handle higher loads than it presently requires.

## Tiny house as an appliance: 20A 120V

Keeping the power requirements of the tiny house minimal allows me to plug it in to an
outlet as if it's just an appliance. Currently I'm powering everything with an extension
cord to a 20-Amp outdoor outlet.

Some of the decisions/appliances that keep the power demands low:

1. [2-burner induction cooktop][induction-cooktop]: This modest cooktop draws a max of 15 Amps
at 120V. It'll be a struggle to cook an 8 course feast, but this cooktop should be enough for
1 to 2 people, and it doesn't require more power than a standard extension cord can supply.
1. [Propane tankless water heater][water-heater]: An electric tankless water heater is a power guzzler
(on the order of 12K Watts for an application like this) that would necessitate a
serious electrical supply (50A 240V). I decided the convenience of the tiny-house-as-an-appliance
setup was worth the added pain of installing a electricity-sipping propane heater.
1. [LED lighting][armacost]: All the lights are dimmable LED. The whole system uses about 48 Watts
at 100% brightness.
1. Energy-concious behavior: Even with low-power appliances, one could still easily exceed the
20-Amp allotment if they aren't careful. Turning on both stove burners and
simultaneously firing up an electric kettle (all while the range hood, minisplit, fridge, and
lights are on) would already exceed 20-Amps. This would mean a walk over to reset the breaker
at the main panel before continuing breakfast, this time making the coffee first before starting
the eggs and pancakes on the stove. If one is willing to live conscious of their energy usage
like this, the tiny-house-as-an-appliance setup could work permanently.

### My setup

![Electrical feeder hardware](https://images.ctfassets.net/rwi5x73ignkx/2oRz3TFJvuQsW8gIwyO8wQ/3513ea0010c2143f0f4b02e2bd73a9b2/electrical-feeder.jpg?w=1170)
{% include caption.html text="Feeder hardware. Components labeled and detailed below." %}

1. Outdoor outlet on the main house: 1-pole 120V. In my setup this outlet is on a 20-Amp circuit.
2. Extension cord. Mine needs to run about 100 feet, so I made my own out of [10-2 wire][10-2]
(thicker than a typical extension cord) to prevent excessive [voltage drop][voltage-drop].
3. ["Dogbone" connector][dogbone]: This serves 2 functions. First as an adapter connecting the
receptacle end of the extension cord power inlet box twist-lock plug (plug/receptacle
[NEMA codes][nema-plugs] labeled in the diagram). The second function is splitting the 120V 1-pole
circuit from the extension cord across both hot conductors of the power inlet. This is
the key to having 2-pole 240V compatible hardware in the tiny house but powering it with a 1-pole
120V extension cord. *I'm actually doing a not-great thing by using this dogbone as it is only
rated for 15 Amps, but since I'm just building and testing at the moment that is all I draw. What
I should do, if I continue this setup permanently, is terminate my extension cord with a TT-30R plug
and use a [30-Amp dogbone][30a-dogbone] that would be sure to handle the full 20-Amps I could draw.*
4. [50-Amp power inlet][power-inlet]: This is the first component that is a permanent part of the
tiny house (it's mounted to the underside). The system can handle 50A 240V from this component on.
5. [6-3 wire][6-3]: 6 gauge 3 conductor (+ ground) NM cable connects the inlet plug to the electrical
panel.
6. [Electrical panel][panel]: I'm using a 6-space panel that's rated up to 100 Amps. This takes the
incoming power and branches it out to my circuits, with a breaker at each branch for protection. I've
wired the panel as a subpanel, meaning the neutral and ground are separate.

## Getting more power

While I'm *pretty* confident the current 20A 120V setup is sufficient (assuming some energy-concious
behavior), I designed the system so 50A 240V power is an easy possibility. This could be quite useful
someday if the small cooktop is too inconvenient, or one wants to stop messing with propane and would
prefer an electric water heater.

To get more power one will need to connect to a breaker on the main panel.

1. Single pole (120V): It seems 30-Amps is the max 120V hookup one could acheive. I've only seen
dogbone adaptors up to [30-Amps][30a-dogbone].
1. Double pole (240V): This is to get a lot more power. Connect to a 15, 20, 30, or
even 50 Amp 2-pole breaker at the main and run an approprately sized cable terminating in a
[NEMA SS2-50R][nema-ss250r] plug out to the power inlet on the tiny house. `P = IV`, so a 50A 240V
setup one can deliver 12K watts -- 5 times the wattage of my current 20A 120V setup.

<div class="youtube-player" data-id="pMgzgNgaTds"></div>
{% include caption.html text="Wiring the panel and testing the circuits." %}

# Circuits

Here is how the circuits are organized in the tiny house:

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
with NEC codes. I've done my best to research and follow electrical codes, built in some extra
safety measures, and had an unofficial inspection of my panel and rough-in by an electrician.
I've also been using the system daily for many months with zero fires or deaths!

Some misc notes:

- Grounding: In addition to the connection back to the main panel's ground via the feeder
cable, my electrician friend recommended adding a grounding electrode at the tiny house subpanel. I
ran a 6-gauge wire from the subpanel's ground bar out through the floor that can be attached to
a grounding rod when the tiny house comes to its permanent location. The propane system's CSST and
the metal trailer frame are both bonded to the system ground.
- Wire gauge: I'm using 12-gauge wire everywhere (except some sections of the
[low voltage LED System][led-section]) even though none of the circuits draw more than 15 Amps.
Only 14-gauge wire is required in that case, but thicker wire ⇨ less resistance ⇨ less heat ⇨
more safety in case of an unexpected power draw.
- Ground Fault + Arc Fault protection
  - [GFCI][gfci]: Ground fault circuit interrupters protect people from electric shock. Their sensor
		monitors that all current flows from hot to neutral. If that is not the case, it means the electricity
		is taking another return path (such as a person's body -- ouch, or dead), and the GFCI shuts off
		the circuit. GFCI is required by code in wet areas like bathrooms and kitchens. I've installed
		GFCI outlets in the kitchen, and in the bathroom used a GFCI breaker for protection of the
		whole circuit.
  - [AFCI][afci]: Arc fault circuit interrupters are a fire prevention measure. They detect and
		prevent unwanted electrical paths and the extreme heat produced along those paths. AFCI
		is required by code to protect all receptacles in dwelling areas.

I've also attempted to slog through the [IRC][irc] and [NEC][nec] code books, but they're
quite hard for a layperson to decipher. Instead I've mostly relied on summaries of the key
safety points of electrical code ([one useful summary here][nec-summary]) so I've followed the
spirit, if not the letter, of the code.

# LED Lighting

I used [Armacost][armacost] LED lighting. I learned about their products through [shedsistence][shedsistence]
and it so happends the company is based near me in Baltimore, which is cool. They have plenty of
documentation about how their systems work, but some things I think are worth mentioning about their
12V DC system:
  - Their LED lights run on low voltage 12V DC current. So you need to convert the 120V AC to 12V DC
		with their power supply bricks ([rectifiers][rectifier]).
  - At low voltages like 12V, voltage drop is a more pronounced issue. I used thick 12-gauge wire for most
		of the LED wiring, not for safety (there isn't safety code around 12V circuits as the voltage
    is too low to shock people or cause fires) but to cut down on resistance and therefore voltage drop
		(`V = IR`).
  - If 12V DC wiring and 120V AC wiring run in parallel, the cycling of the AC current can induce
		flickering in the LED lighting. One must layout the wiring so there is always 6" between DC and AC
		wires, and where they must come close they should cross perpendicularly.

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
[30a-dogbone]:https://www.amazon.com/Camco-55582-PowerGrip-Locking-Electrical/dp/B00C5T54M8
[nema-ss250r]: https://www.amazon.com/Conntek-50-Assembly-Connector-Listed/dp/B001TNW2BW
[irc]: https://codes.iccsafe.org/content/IRC2015/toc
[nec]: https://www.nfpa.org/codes-and-standards/all-codes-and-standards/list-of-codes-and-standards/detail?code=70
[nec-summary]: http://www.nojolt.com/residential_electrical_wiring_rough_in_guide.shtml
[rectifier]: https://en.wikipedia.org/wiki/Rectifier
[led-section]: {{ site.baseurl }}{% link _posts/2018-11-24-electrical.markdown %}#led-lighting
