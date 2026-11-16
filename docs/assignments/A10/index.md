# A10 – Lead Screw Translating System

## Objective
The objective of this assignment is to design a leadscrew system by determining the minimum leadscrew diameter, rotational speed range, and maximum torque. The assignment requires selecting an appropriate bronze nut and flange, designing a crosshead that meets the strength and deflection requirements, and comparing material costs. The assignment involves parametrically modeling and assembling the components in CAD, as well as detailing the engineering lessons learned.

## Analyze

## Leadscrew-Taylor McHone

## Minimum Diameter
<img width="333" height="934" alt="image" src="https://github.com/user-attachments/assets/0c044c23-99a5-4bf4-aa64-c83bbf944b30" />
I calculated the minimum leadscrew diameter needed to support the applied load. The total force of 2000 N was divided between t wo leadscrews, giving each screw a load of 1000 N. Using 1018 carbon steel with a yield strength of 64,000 psi and a safety factor of 4, I calculated the allowable stress and used the axial stress equation to determine a minimum diameter of 6.79mm. 

## Rotational Speed
<img width="322" height="417" alt="image" src="https://github.com/user-attachments/assets/4306b8df-97e2-49e2-838c-36be58acef41" />
I calculated the minimum and maximum rotational speeds needed for the leadscrews to move at the required velocities of 1mm/min and 50mm/min. I selected a standard 3/8"-12 single-start leadscrew with a lead of 2.1167 mm/rev. Using the relationship between linear velocity, rotational speed, and screw lead, I calculated a minimum rotational speed of 0.4724 RPM and a maximum rotational speed of 23.62 RPM. 

## Max Torque
<img width="607" height="820" alt="image" src="https://github.com/user-attachments/assets/8c145651-147b-4330-887f-f7377264cbdc" />
<img width="432" height="424" alt="image" src="https://github.com/user-attachments/assets/30f05ed5-7748-4b41-a6cc-0b427c2a2a5d" />
I calculated the torque required to raise the applied load using the selected 3/8"-12 leadscrew. I determined the coefficient of friction and used the mean diameter, screw lead, and applied force to calculate the torque. The maximum torque was approximately 1.2314 N*m per leadscrew, giving a total torque of 2.4628 N*m for both leadscrews. These calculations assume the leadscrews and nuts are lubricated.

## Nut and Flange-Dina Chouffani
<img width="619" height="928" alt="image" src="https://github.com/user-attachments/assets/10b99013-5fb3-479e-b297-1fed81a4d934" />
For the nut and flange section, I analyzed the internal thread of my selected 673 bronze nut to determine whether they could support the applied load. I used a 3/8"-12 Acme thread with a 5/8-inch nut length and calculated the thread bending stress using the equation from the lecture notes. The bending stress was approximately 2,612 psi, which is below the allowable stress of 16,500 psi. The calculated safety factor was 25.3, exceeding the required safety factor of 4.

## Crosshead- Dina Chouffani

Strength Analysis
<img width="685" height="990" alt="image" src="https://github.com/user-attachments/assets/9e3d7046-cdfe-45b6-8e97-d08a1b03819d" />
I calculated the minimum required height of the crosshead based on bending stress using 6061-t6 aluminum. I used an applied load of 2000 N, a length of 300 mm, a width of 100mm, a yield strength of 241 N/mm^2, and a factor of safety of 4. I used the equilibrium equations to determine the reaction forces at each support, which were both 1000 N. I then calculated the maximum bending moment and used the bending stress equation along with the allowable stress to solve for the minimum required height. The calculated height was 12.2 mm, which satisfies the bending stress requirement with a factor of safety of 4.

Deflection Analysis
<img width="646" height="990" alt="image" src="https://github.com/user-attachments/assets/54a1d6d2-01ab-4f58-9241-0ce2e0971359" />
I calculated the minimum required height of the crosshead based on deflection using 6061-T6 aluminum. I used an applied load of 2000 N, a length of 300 mm, a width of 100 mm, and a maximum allowable deflection of 0.1 mm. The calculated minimum height was 26.96 mm. Since this was greater than the height required from the stress analysis, deflection controlled the design. I then substituted the calculated height back into the deflection equation and obtained a deflection of approximately 0.09999 mm, which is below the allowable 0.1 mm. Therefore, the deflection requirement was satisfied.

Multiview Sketch
<img width="763" height="523" alt="image" src="https://github.com/user-attachments/assets/7e849a54-d5d5-4ea9-84b9-224d0ba9d0db" />

Tabulating Costs

## Decide
_Reference your concept selection (Pugh matrix) here. How does this design follow from that decision?_

## Communicate
Parametric Modeling
Lessons Learned
