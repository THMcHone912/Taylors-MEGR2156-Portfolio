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

Item #	Quantity	Name	Cost/Item	Cost	Purchase Link
804T48	1	40 Series T-Slot Aluminum Framing, 80 mm × 40 mm, 3 m Long	$245.87	$245.87	Grainger
95120A592	2	932 Bearing Bronze ACME Flange Nut, 3/8"-12 RH	$111.78	$223.56	McMaster-Carr
98935A817	2	Carbon Steel ACME Lead Screw, 3/8"-12 RH, 36" Long	$10.15	$20.30	McMaster-Carr
Total Cost	$489.73	

## CAD MODEL-Nicholas Cornetta

For the parametric modeling portion of this assignment, I used Creo Parametric to design the crosshead based on my group's strength and deflection calculations. I created the crosshead using 6061-T6 aluminum with dimensions of 360 mm in length, 100 mm in width, and 30 mm in thickness. I then added the leadscrew holes, spacing them 300 mm apart to align with the leadscrew system. One challenge I encountered was determining the correct hole dimensions to ensure the selected leadscrews and bronze flange nuts would fit properly. I learned how important it is to reference the actual dimensions of purchased components when designing a part in CAD, since incorrect dimensions can create problems during assembly. This assignment also helped me better understand how engineering calculations influence the dimensions and features of a part and how parametric modeling allows changes to be made efficiently throughout the design process.

Crosshead

<img width="1794" height="712" alt="image" src="https://github.com/user-attachments/assets/d70e9263-deea-4ba8-b71f-501a0193e88a" />

<img width="1545" height="678" alt="image" src="https://github.com/user-attachments/assets/22eadeec-a3d9-41db-ab53-885b409c5154" />

<img width="949" height="756" alt="image" src="https://github.com/user-attachments/assets/e84fb9b2-374a-4eb5-b2a0-7e00eea2431f" />

Frame
<img width="1737" height="663" alt="image" src="https://github.com/user-attachments/assets/26ca6b5a-75e4-4aba-85a8-5216c8fcd3ab" />

Flange Nut
<img width="682" height="673" alt="image" src="https://github.com/user-attachments/assets/dcd1b70f-9a63-4ba5-872e-cfecbab1984b" />

Lead Screw
<img width="1977" height="1044" alt="image" src="https://github.com/user-attachments/assets/8c0458a4-8539-499e-904e-21e749f3565e" />

Assembly
<img width="1596" height="1041" alt="image" src="https://github.com/user-attachments/assets/c34ec927-95fd-4c2a-9af0-bbeb8cabaefc" />
<img width="852" height="1050" alt="image" src="https://github.com/user-attachments/assets/2ce2ee07-4501-4be1-b1cb-1cfada99a240" />


## Lessons Learned
Our group spent approximately 7 hours combined completing this assignment. Throughout the project, we learned how to apply engineering calculations to design a functional leadscrew system capable of supporting a 2 kN tensile load while maintaining a safety factor of 4. One important lesson we learned was how much the assumptions made during the design process can influence the final results. For example, when calculating the torque required to rotate the leadscrews, we had to consider whether the leadscrews and bronze nuts would be lubricated or unlubricated. This decision directly affects the coefficient of friction, which changes the required torque and could require an entirely different set of calculations based on the selected conditions. We also learned the importance of verifying that purchased components are compatible with one another, especially when selecting matching thread sizes and determining the dimensions needed for the crosshead mounting holes. Another challenge was translating our theoretical calculations into a practical CAD model while ensuring that the dimensions satisfied the strength and deflection requirements. Overall, this project helped us better understand the relationship between engineering analysis, material selection, component compatibility, and parametric modeling, while reinforcing the importance of communication and coordination when working as a team. Each team members name is next to the sections that they did.

## CAD Links
Crosshead: https://drive.google.com/file/d/1bq0rhZXaWHBxbweBtz2RrmGjUecE42SP/view?usp=sharing

Aluminium Frame: https://drive.google.com/file/d/13mhg8UuLy7-oSyzXsZ8ZKiqZM5FPr0Fl/view?usp=sharing

Flange Nut: https://drive.google.com/file/d/1EfdXIEs1OBQqaJKWrXGXwagvW3R4AfEF/view?usp=sharing

Lead Screw: https://drive.google.com/file/d/1x5t3TtvjypjKoXop3mC6aSoWEX3YOpd1/view?usp=sharing

Assembly: https://drive.google.com/file/d/1CqJOj0KF37N2bUD-ZTlEuXUCZpqLVyjo/view?usp=sharing


