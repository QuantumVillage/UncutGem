# Uncut Gem

A prototype Full Stack fully Open Source NV Center Diamond Magnetometer!

V1 - this document and repository...

V2 - **RELEASED @ DEF CON 33 in 2025!**

There are several sections detailing the parts of the build: 

- [`/science`](./science) - a folder with an explanation and references for the science behind the sensor. 
- [`/firmware`](./firmware/) - details the firmware used in the sensor.
- [`hardware`](./hardware/) - has two main sections
  - [`hardware/pcb`](./hardware/PCB/) - details the PCB schematics and parts
  - [`hardware/DiamondMount`](./hardware/DiamondMount/) - details how the diamond is mounted
- [Build Guide](./BuildGuide/BuildGuide.md) - a comprehensive build guide for the sensor.

<img src="images/device-front.jpeg" style="width: 50%"/><img src="images/device-back.jpeg" style="width: 50%"/>

## Project Mission

We are creating the world's first fully open-source quantum sensing platform designed from the start to be accessible, future-proof, and most importantly; hackable! 

We are designing, building, provisioning, and aiming for distribution of a fully open hardware platform, complete with fully open firmware, that gives a firm basis for anyone to start learning about quantum sensing through nitrogen vacancy center diamond magnetometry. 

By incorporating key design decisions, we are building the basis for what we think will be quantum technology's 'Apple II moment'; the opportunity for anyone who is curious to gain access to a quantum device that they can operate safely at home, with the full capability to customize, improve, develop with, and share knowledge about this incredible technology. 

## Design Philosophy

We have used the following four principles to guide the initial development of this project:

* Aim to create a platform for exploration.
* Use Consumer Off-the-shelf (COTS) components as much as possible.
* Create a hardware stack that allows as many aspects of the sensing process to be ‘software problems’ as possible.
* Where assembly is required, simplify!

## Features

The design is in two iterations, but generally our features are:

* Using easy-to-acquire, all-generic parts for our PCBs.
* Low-noise photodiode signal amplifier design that is robust and inexpensive.
* Using off the shelf, low cost, widely available daughter boards.
* Easy and reasonably compact construction from carefully considered design.
* Optimized control stack and firmware, written using Arduino IDE for portability and future-proofing.
* Full build guide and growing documentation.
* Growing community around these devices. 

## Contents Overview

We aim to cover all of the essential information for someone interested to learn about quantum sensing with Nitrogen Vacancy Centre Diamonds, and then have the information and parts-list to go ahead and construct such a device. To that end, we cover:

* The basic science behind this kind of solid state quantum sensing
* A run down of our design choices and devices/parts used to make the sensor
* A build guide for putting together a working sensor

Everything is open source, including the firmware, and we welcome contributions to improve this design!

## Why Open Source?

> “Information flow is what the Internet is about. Information sharing is power. If you don't share your ideas, smart people can't do anything about them, and you'll remain anonymous and powerless.”
> -- Vint Cerf

We think that more projects in quantum technology should be open source, so that quantum tech can benefit from the rich ecosystem of 'ready-made' tooling that our existing software and classical technology stacks have enjoyed! We firmly believe that by creating an open-source baseline for quantum and quantum-related technologies we immediately gain a number of things:

* The dissemination of knowledge around quantum technologies allows the general workforce to gain the skills needed to further develop quantum tech. 
* By creating a testbed platform that is designed to be hackable, it is natural to extend its functionality into areas that nobody is currently considering.
* By using COTS parts and creating and open design, we can drive down the costs associated with quantum sensing.
* The value proposition for commercial products and services is immediate by comparison to an open-source 'free' baseline.

## Cost per Device

The ballpark costs are as follows (in GBP):

| Item                   | Number | Cost      |
|:-----------------------|:------:|----------:|
| Battery pack           | 1      | Free to £5|
| OpAmp + electronics    | 1      | up to £5  |
| Laser Module           | 1      | ~£5-15    |
| ADF4350/1 MW Generator | 1      | £15-25    |
| MW Gain (40dB) + BNC   | 1      | £10       |
| PCB (unit from run)    | 1      | ~£5       |
| OLED Screen            | 1      | £5        |
| ESP32 board            | 1      | ~£10      |
| NV Center Diamond      | 1      | ~£10      |
| Epoxy and Cu Wire      | 1 ea.  | £10-15    |
|                        | **TOTAL** | ~£115  |

## Acknowledgements 

We would like to thank the following folk for their help during this project:

* **Victoria Kumaran** - Prototyping, design and conceptualisation, and project contextualisation.
* **Dr. Mark Carney** - Prototyping, initial designs for hardware/firmware.
* **Dr. Matthew Markham** - Key contact at Element6, tech support and providing quantum material.
* **Prof. Ben Varcoe** - testing support and physics expertise/advisory.
* **Dr. Brian McDermott** - Expert Advisor.
* **Rick Altherr** - Design and engineering expertise and support.
* **Elle Dowling** - Orthographic Services.

## Resources

Here are some key resources for this project:

* [ADF4351 Datasheet](./firmware/resources/adf4351.pdf)
* [ADF435x Cheatsheet](./firmware/resources/ADF435x-cheatsheet.pdf)
* Stegemann et al. - Modular low-cost 3D printed setup for experiments with NV centers in diamond - [Stegemann_2023_Eur._J._Phys._44_035402.pdf](./science/resources/Stegemann_2023_Eur._J._Phys._44_035402.pdf)
* Acosta and Hemmer - Nitrogen-vacancy centers: Physics and applications - [mrs.2013.18.pdf](./science/resources/mrs.2013.18.pdf)
* Frellsen and Ahmadi - Sensing magnetic fields with diamonds and green laser light - [Sensing%20magnetic%20fields%20with%20diamonds%20and%20green%20laser%20light%20–%20Quantum.pdf)](./science/resources/Sensing%20magnetic%20fields%20with%20diamonds%20and%20green%20laser%20light%20–%20Quantum.pdf) 

## Laser and Electrical Safety Notice

Adapted in part from a [safety sheet from Edmund Optics](https://www.edmundoptics.co.uk/document/download/485774).

### Electrical Safety

1. Disconnect any main power lines before working on any electrical equipment when it is not necessary for the equipment to be operating. 
1. Never work on electrical equipment unless there is another person nearby who is familiar with the operation and hazards of the equipment, and who is competent to administer first aid. 
1. When possible, keep one hand away from the equipment to reduce the danger of current flowing through the body if a live circuit is accidentally touched. 
1. Always use approved, insulated tool when working on equipment. 
1. Special measurement techniques are required for some systems. Ground references must be selected by a technician who has a complete understanding of the system operation and associated electronics. If this is not you, seek someone who can do this with you.

### Laser Safety

1. DO NOT aim any laser on yourself or others, especially do not aim at the face and eyes. 
  * Even temporary exposure can cause significant damage to the face and the eye, so much as burning and blind. 
2. DO NOT aim this laser on animals. 
3. Never use your laser in the vicinity of highways and airports. 
  * DO NOT target moving vehicles and airplanes. 
4. Never randomly aim a laser out the window. 
5. DO NOT use a laser at the place marked "No smoking" "inflammable and explosive".
6. Avoid pointing a laser at any reflective surfaces, e.g. mirror, glass and bright metal. 
  * Unintentionally reflected beams can easily violate laser safety protocols. 
7. Never import a laser which disobeys the laser safety regulation or law of the country you live in. 
8. Wearing a set of proper laser safety goggles is a good idea. 
  * Though laser safety goggles can protect a person's vision, it's always best to remember NEVER to look into a laser beam or bright reflection even when wearing laser safety goggles. 
9. Never place the laser anywhere that may easily hurt another human or yourself. 
10. If experimenting with an infrared emission laser, use an infrared detector to verify that the laser beam is on or off before working on the laser
  * No, you can't see nor smell it. Use a detector. 
11. Set up controlled access areas for laser experimentation, and work only in well marked areas with controlled access. 
  * Be sure to post appropriate warning signs visible to all. 
12. The operation of lasers should be under the supervision of qualified personnel only. When not in use, lasers should be shut down completely and made off-limit to unauthorized personnel. 
13. Limit access to a laser system only to persons required to be present. 
14. Laser should be operated in a clean and dry environment, free from dust, moisture, and sources of spurious electric charge. 
15. Maintain experimental setups at low level to prevent inadvertent eye encounter with beams and minimize risk.

## Licensing

This project is under the Affero GPL license. This is a paritcularly restrictive license that demands any and all updates from anyone using this project. The AGPL is designed specifically to ensure that any modified material becomes available to the community. Specifically:

> Notwithstanding any other provision of this License, if you modify the Program, your modified version must prominently offer all users interacting with it remotely through a computer network (if your version supports such interaction) an opportunity to receive the Corresponding Source of your version by providing access to the Corresponding Source from a network server at no charge, through some standard or customary means of facilitating copying of software. [...]

We have chosen this license as it promotes fairness to the community and broadens the scope of those benefiting from this project.

However, if you would like to re-license this for commercial use under a more forgiving license, such at the MIT License, then we are open to negotiations from companies who would like to use this work in return for substantial support of Quantum Village Inc. You can reach us at `hello [a t] quantumvillage [d0t] org`.
