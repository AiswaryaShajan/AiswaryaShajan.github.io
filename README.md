# MSc Robotics Dissertation Log

## Week 1 (04 - 10 June 2026)
**Focus: Chassis research, early prototyping, CAD learning, and motor requirements.**

I started this week by exploring different chassis designs for my human‑following robot. I looked at wooden and aluminium builds, paying close attention to how others mounted motors, arranged electronics, and balanced payload. Projects like the [“Follow‑Me Cooler”](https://www.hackster.io/hackershack/make-an-autonomous-follow-me-cooler-7ca8bc) and ["Covid Bot"](https://www.hackster.io/343328/p3psi-a-web-driven-covid-19-carrier-robot-eab65a) gave me useful ideas such as using 3D‑printed brackets, LiPo batteries (lightweight and less power consumption),simple two‑wheel drive setups and neat ABS electrical enclosures. This early research helped me understand what kind of structure would be practical for my own design.

> picture

Alongside the research, I began learning Onshape to sketch the chassis digitally. I practiced basic tools like sketching, dimensioning, and extruding, although I ran into issues with the CAD dimensions not matching my physical measurements. This made me realize how important accurate measuring and consistent reference points are when designing a frame. The tutorial I referred for Onshape is [here](https://www.youtube.com/watch?v=GKI2H1mVyGY&list=PLxmrkna-ixrIQmsPR3MITi4Ru1bnMH4-l&index=2).

Mid‑week, I evaluated whether to jump straight into building the final robot or start with a prototype. I leaned toward prototyping and simply created a Bill of Materials for a wooden version, estimating the cost at around AED 750. To better understand load requirements, I bought a basket and filled it until it weighed about 10 kg. This helped me estimate the torque and motor specifications needed for the final build.

> - picture

Toward the end of the week, I focused on motor research. I studied DC gear motors and planetary gear motors, learning how torque, RPM, and wheel size affect performance. Using a 20 kg estimated load and 125 mm wheels, I calculated that I would need motors in the 15–25 kg·cm torque range. I wrapped up the week by sketching several prototype layouts, which helped me visualize how the motors, wheels, and electronics would fit together.

> - picture


## Week 2 (11 - 17 June 2026)
* **Focus: Human‑following research, tracking algorithms, mini‑robot experiments, and early electronics testing.**
- Shifted toward the software and sensing side of the project. I researched human‑following methods such as Bluetooth, UWB, and camera‑based tracking, and set up a ROS repository. I reviewed academic papers on indoor localization and human‑following robots, learning about perception layers, tracking algorithms like SORT/DeepSORT, and the importance of re‑identification during occlusions. 

I also explored evaluation metrics such as accuracy, precision, recall, and F‑score. To experiment practically, I ordered a small robot kit and assembled it, though it required soldering equipment I didn’t have. I attempted a temporary wiring setup using Arduino, and I will implement the camera based human following logic on this mini robot first before I attempt to upscale it.


.

