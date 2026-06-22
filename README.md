# MSc Robotics Dissertation Log - Porter Robot

## My first idea (The "What?")
The idea for this project came from noticing a common household struggle. It is a hassle for my father to carry heavy monthly groceries or for my sister to balance bulky shopping bags while managing a toddler. Moving these loads from the building parking lot or lobby up to the apartment door is a recurring physical strain.
The idea is to have a porter assistant which carries the cargo for you. Instead of carrying heavy bags or making multiple trips, you just load up the robot. It handles the lifting and follows you safely right upto your destination (Ex: from basement to your apartment door).

I wanted to design something that the residents can share. To see if this was a widespread issue, I ran a WhatsApp poll among the residents in my apartment building. The results were clear: neighbors actively face this same bottleneck and would gladly utilize a shared indoor transport assistant.

## Does this kind of robot already exist? What would be my improvement? (The "Why"?)
Companies already make robots that can follow people or carry cargo. Some examples are:
Piaggio Gita - a personal robot assistant
Starship robot - famous little cooler-shaped robots that drive around university campuses to deliver food.
EffiBOT / Industrial AMRs: Heavy-duty robots used in giant DHL warehouses to follow workers and carry massive loads.
While these examples are incredible, they can be expensive and less practical for a shared residential setting. So the goal is to build an affordable version that is designed to specifically navigate tight hallways, standard doorways and handle lighting changes. 

## Roadmap (The "How"?)


## Week 1 (04 - 10 June 2026)
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


## Week 2 (11 - 17 June 2026)
* **Focus: Human‑following research, tracking algorithms, mini‑robot experiments, and early electronics testing.**
- Shifted toward the software and sensing side of the project. I researched human‑following methods such as Bluetooth, UWB [[1]](https://www.proquest.com/docview/3188899797?accountid=12441&parentSessionId=nhQnlnMhFZaP3jBT3qcdB5s8jbQfOx79nXVwf5isG4g%3D&pq-origsite=primo&sourcetype=Scholarly%20Journals), and camera‑based tracking, and set up a ROS repository. I reviewed academic papers on indoor localization and human‑following robots, learning about perception layers, tracking algorithms like SORT/DeepSORT, and the importance of re‑identification during occlusions[[2]](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10910101). 

I also explored evaluation metrics such as accuracy, precision, recall, and F‑score. To experiment practically, I ordered a small robot kit and assembled it, though it required soldering equipment I didn’t have. I attempted a temporary wiring setup using Arduino, and I will implement the camera based human following logic on this mini robot first before I attempt to upscale it.

<div align="center">
  <img width="335" height="300" alt="image" src="https://github.com/user-attachments/assets/74411356-17b3-4802-b9a9-524cfddb6a46" />
  <p><i>Figure 4: Toy Robot Kit</i></p>
</div>

