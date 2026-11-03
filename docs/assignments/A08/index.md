# A8 – Gear Box Design

## Objective
The objective of this assignment was to design a gearbox that could be both assembled and disassembled, analyze and size input and output shafts for strength, design journal bearings to support the shafts, creating a gearbox housing that had the proper fastening and clearance, designing a CAD model to generate a final design, and to continue practicing calculations, lessons learned and sketches.

## Analyze
Before I even touched CAD/Solidworks, I went ahead and did some calculations, and drew my Free-Body Diagrams. The gearbox uses two spur gears with 48 teeth, and a smaller gear with 18 teeth. The RPM input calculated was 2933.33RPM. I also solved for input torque, and doing the torque output times the gear ratio gave me an input torque of 0.46875in*lbf. I also found the center distance between the gears, which was 0.6875 inches. The tangential force was 2.50 lbf. The radial force was 0.910lbf.

The calculated gear ratio indicates that the output gear reduces the rotational speed while it increases torque. The ideal gear train produces an output torque of 1.25 in*lbf at 1100 rpm. The calculated tangential and radial forces will be used in both the bearing and shaft analyses.
<img width="1668" height="2420" alt="unnamed" src="https://github.com/user-attachments/assets/6dd82a07-6dda-4524-b4d7-468b803730f1" />

In the photo, you can see the lists of givens/knowns, and unknowns. Plus, my calculations, freebody diagrams and even more calculations are seen in the image. I also found the bearing pressure, the pressure-velocity factor, and the knowns we knew about the gears from McMaster-Carr products.

The gearbox housing I designed consists of two separate parts. It has a bottom housing, and a removeable top cover. The design provides an enclosed space for the gears, but it also supports the shafts and bearings.  Seen below is a sketch and extrusion of the top housing and the bottom housing.

<img width="226" height="167" alt="Screenshot 2026-11-02 190601" src="https://github.com/user-attachments/assets/03b713ac-eb73-451e-baf6-b12f786a0176" />

<img width="341" height="308" alt="Screenshot 2026-11-02 191026" src="https://github.com/user-attachments/assets/29bba2ef-d5e9-43a1-8b59-9830ec5f0bbf" />

<img width="341" height="241" alt="Screenshot 2026-11-02 201939" src="https://github.com/user-attachments/assets/10b9ab34-2cce-4e8f-be6c-bd0802a8576a" />

<img width="508" height="254" alt="Screenshot 2026-11-02 201742" src="https://github.com/user-attachments/assets/08f9076c-4184-44e9-92f7-c65209a3b47e" />

<img width="291" height="186" alt="Screenshot 2026-11-02 211827" src="https://github.com/user-attachments/assets/a77d2726-9bc3-4933-954c-eb0de627e5cb" />

The fasteners I chose to use were M3 fasteners. This is seen and reflected on the complete assembly model seen below where the four screw holes are mounted on both the top and bottom. These screws allow the top part of the assembly to be removed to check on the gears in the cavity underneath. 

<img width="291" height="186" alt="Screenshot 2026-11-02 211827" src="https://github.com/user-attachments/assets/8bcf76b1-cfa8-436d-980e-d749038adbc0" />

<img width="508" height="254" alt="Screenshot 2026-11-02 201742" src="https://github.com/user-attachments/assets/72e19414-67f7-4a41-bdc9-b2758eac2cf1" />


## Decide

The gearbox itself was designed to be a two-stage housing assembly that contained the pair of spur gears, the two rotating shafts, and the journal bearings. The design I chose uses an 18 tooth input gear, and a 48 tooth output gear to achieve the gear reduction in the assignment.

The overall design focuses on maintaining the proper gear alignments, providing adequate shaft support, allowing the gearbox to be assembled and serviced, and minimizing friction. 

The input shaft uses a diameter of 0.125 inches. The output shaft uses a diameter of 0.250 inches. Both shafts are designed with an extrusion length of 1.00 inch.

The shafts are also meant to be positioned parallel to one another. Their theoretical center distances from each other is 0.6875 inches between their centerlines. 

The journal bearings are incorporated into the housing to support the rotating shafts and reduce friction between the gears during their operation. The bearing locations were designed around both the output and input shaft positions. The housing includes raised bearing-support features to accommodate the selected bearings and provide support at the shaft openings. Also, the bearing dimensions and material were finalized based on the calculated surface velocity, PV operating requirements, and pressure.

The gearbox has a two-piece housing that consists of a bottom section, and a removeable top cover. This was designed to enclose the gear train while continuing to provide sufficient internal clearance for the gears to rotate. The circular bearing support locations were incorporated into the end walls to help support the shafts. Four fastener locations were added around the perimeter to secure the top cover to the bottom housing. The initial housing dimensions and internal cavity were also developed to accommodate the selected gear arrangement, bearing locations, and the shafts.

My design uses the readily available parts and spur gears in particular from McMaster-Carr. The housing components and shafts were modeled as separate Solidworks pieces before being added to an assembly of the entire model of the gearbox. 

<img width="469" height="269" alt="Screenshot 2026-11-02 215031" src="https://github.com/user-attachments/assets/2ab2538a-2b6f-4ad9-af7e-50a149ea13a3" />

<img width="469" height="269" alt="Shaft" src="https://github.com/user-attachments/assets/d13586e2-41f1-4132-9d46-0f7cb8417cc6" />

The journal bearings and their material and dimensions were selected by comparing available options against the calculated requirement operations. The final material selections for this gearbox must include wear resistance, a compatibility with the other gearbox components, and strength.

Several important considerations I used that helped influence my gearbox design was maintaining the correct distance between the gears' center distances. I also took into consideration supporting both shafts with journal bearings, allowing the housing to be separated for assembly and maintenance, providing sufficient wall thickness and fastening support. I lastly also considered having the adequate clearance between the house and gears, and maintaining the alignment between the bearing openings and the shafts. 

## Communicate

I will not lie, this project honestly got me frustrated; especially trying to fit the gears into the cavity. I had everything lined up and working on the outside before I went back and reread the assignment for like a 20th time and realized that the gears had to be inside the cavity.

The gears not wanting to get inside the cavity alongside learning the mating feature and trying to get everything to line up on the centerline. The gears and trying to get them inside the gearbox frustrated me in particular, because I had a working design on the outside, but also knew that I needed to maintain the wear and tear of the gears, and that had me frustrated because I tried repeatedly to move the gears inside the cavity and kept getting odd like parts of the gears sticking out. 

Even though my gears rotated, meshed, did everything they needed to, the glaring of having them being encapsulated inside the cavity of the gearbox frustrated me a lot. Alongside the frustration, I did learn more and more of how to continue to hone my skills in Solidworks.

All in all, this assignment took me around 6.5-7 hours, from the calculations to the part of modeling on CAD that I got to.

Link to my CAD file is here: https://drive.google.com/file/d/17BFa7nf1kiOWDbRzVRG0IQsCTbU2v17L/view?usp=sharing
