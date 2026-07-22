# MSc Robotics Dissertation Log – Battery Analysis for an Indoor Porter Robot

## My first idea (The "What?")
The idea for this project came from noticing a common household challenge. It is often difficult for my father to carry heavy monthly groceries or for my sister to manage bulky shopping bags while looking after a toddler. Transporting these items from the building parking area or lobby to the apartment involves significant physical effort and often requires multiple trips.

My initial idea was to develop an autonomous indoor porter robot that could carry shopping bags and follow a resident to their apartment. The aim was to create a shared robotic assistant that residents within an apartment building could use whenever required.

To understand whether this problem was experienced by others, I conducted a WhatsApp poll among residents in my apartment building. The responses indicated that many neighbours face the same difficulty and expressed interest in using a shared indoor transport robot.

## Does this kind of robot already exist? What would be my improvement? (The "Why"?)
Companies already make robots that can follow people or carry cargo. Some examples are:
Piaggio Gita - a personal robot assistant
Starship robot - famous little cooler-shaped robots that drive around university campuses to deliver food.
EffiBOT / Industrial AMRs: Heavy-duty robots used in giant DHL warehouses to follow workers and carry massive loads.
While these examples are incredible, they can be expensive and less practical for a shared residential setting. So the goal is to build an affordable version that is designed to specifically navigate tight hallways, standard doorways and handle lighting changes. 

## The Refined Idea
My initial intention was to design and prototype an affordable porter robot suitable for indoor apartment environments. However, after reviewing the project requirements and discussing the scope with my supervisor, it became clear that developing and validating every subsystem including mechanical design, navigation, human following, obstacle avoidance and system integration would exceed the available project timeframe.

As a result, the dissertation scope was refined. Instead of implementing a complete autonomous porter robot, the project now focuses on one of its key engineering subsystems: analysing and comparing battery technologies for an indoor porter robot. The robot platform is therefore treated as the application case study while the dissertation investigates battery performance, runtime, weight, cost and suitability for the intended operating conditions.


## Roadmap (The "How"?)


## Week 1 (25 June - 02 July 2026)
**Focus: Chassis research, early prototyping, CAD learning, and motor requirements.**

I started this week by exploring different chassis designs for my human‑following robot. I looked at wooden and aluminium builds, paying close attention to how others mounted motors, arranged electronics, and balanced payload. Projects like the [“Follow‑Me Cooler”](https://www.hackster.io/hackershack/make-an-autonomous-follow-me-cooler-7ca8bc) and ["Covid Bot"](https://www.hackster.io/343328/p3psi-a-web-driven-covid-19-carrier-robot-eab65a) gave me useful ideas such as using 3D‑printed brackets, LiPo batteries (lightweight and less power consumption),simple two‑wheel drive setups and neat ABS electrical enclosures. This early research helped me understand what kind of structure would be practical for my own design.

<div align="center">
  <img width="300" height="240" alt="image" src="https://github.com/user-attachments/assets/e584ab3a-5a36-46ce-be29-ac5bd4c2aabf" />
  <p><i>Figure 1: Follow-me Cooler</i></p>
</div>

Alongside the research, I began learning Onshape to sketch the chassis digitally. I practiced basic tools like sketching, dimensioning, and extruding, although I ran into issues with the CAD dimensions not matching my physical measurements. This made me realize how important accurate measuring and consistent reference points are when designing a frame. The tutorial I referred for Onshape is [here](https://www.youtube.com/watch?v=GKI2H1mVyGY&list=PLxmrkna-ixrIQmsPR3MITi4Ru1bnMH4-l&index=2).

Mid‑week, I evaluated whether to jump straight into building the final robot or start with a prototype. I leaned toward prototyping and simply created a Bill of Materials for a wooden version, estimating the cost at around AED 750. To better understand load requirements, I bought a basket and filled it until it weighed about 10 kg. This helped me estimate the torque and motor specifications needed for the final build.

<div align="center">
  <img width="700" height="240" alt="image" src="https://github.com/user-attachments/assets/29010def-4947-439b-a490-a00c7dcf24e0" />
  <p><i>Figure 2: Basket for carrying the items</i></p>
</div>



Toward the end of the week, I focused on motor research. I studied DC gear motors and planetary gear motors, learning how torque, RPM, and wheel size affect performance. Using a 20 kg estimated load and 125 mm wheels, I calculated that I would need motors in the 15–25 kg·cm torque range. I wrapped up the week by sketching several prototype layouts, which helped me visualize how the motors, wheels, and electronics would fit together.

<div align="center">
  <img width="852" height="347" alt="image" src="https://github.com/user-attachments/assets/ea1da69d-8c6e-47db-82c2-0e46d756c937" />
  <p><i>Figure 3: Chassis Designs</i></p>
</div>


## Week 2 (03 - 10 July 2026)
* **Focus: Literature Review and ordering all parts (motors, wheels, casters, Raspberry Pi, INA219, driver, battery).**
- Rather than finalising a research question immediately, I started reading relevant papers to understand the current research and identify potential gaps.

My initial research focus is to investigate how the carried load affects a porter robot's energy consumption and what this means for battery sizing, daily runtime and recharge cycles in a residential building. However, I expect the research question to be refined as I continue reviewing the literature.

Alongside the literature review, I also began researching suitable motors and wheels for the robot, as these components directly influence the robot's power requirements and battery selection.

## Week 3 (10 – 16 July 2026)
* **Focus: Hardware acquisition, software environment setup, CAD drawing.**

This week, the hardware procurement process was completed by collecting the Raspberry Pi 5 from the laboratory and finalising the remaining component orders. Some component selections were revised due to availability and specification constraints.

**Components Acquired**
- Raspberry Pi 5
- DC geared motors with wheel and encoder (12V /20RPM)
- Li-ion 3S Battery
- Power bank (for RPi)

The software development environment was also set up by installing WSL, Ubuntu, and ROS 2 Humble. The installation was verified by successfully running the teleoperation package, providing the foundation for subsequent robot development.

**CAD Drawing**
- After becoming familiar with the basics of CAD modelling in Onshape, I began designing the robot and assembling its individual components. The current design consists of a lower enclosure to house the electronics, with the drive motors mounted inside such that the motor shafts extend through the side walls to accommodate the wheels. A removable lid is fitted to the enclosure, and a loading platform is supported above it using spacers.
The CAD models for the JGB-37 motors, 65 mm wheels, motor brackets, and shaft couplers were obtained from GrabCAD, while the spacer model was sourced from the McMaster-Carr library. The progression of the design is shown below.

<div align="center">
  <img width="1030" height="198" alt="image" src="https://github.com/user-attachments/assets/d48e32b3-30d8-4671-aade-4ea299972ef6" />
  <p><i>Figure 4: CAD Progression</i></p>
</div>

- Problem encountered - During the initial assembly, it was observed that the drive wheels do not make contact with the ground. Further evaluation of the chassis dimensions, motor mounting position, and wheel arrangement is required to resolve this issue. The caster wheels were not selected at this point and will only be incorporated in the later design iteration.

## Week 4 (17 – 24 July 2026)
* **Focus: CAD refinement,Pi-ROS installation, and Methodology research .**

