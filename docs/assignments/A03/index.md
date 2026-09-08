# A3 – [Topic]

## Objective
The purpose of this assignment was to design a circular aluminum bar that would be subjected to a direct tensile load while maintaining a maximum axial deflection within the required limit. The assignment alto introduced parametric modeling and finite element analysis (FEA) as methods for designing and verifying an engineering component. 

For my design, I chose an applied force of 400 lbf and an elastic modulus of 10.0*10^6 psi. I used a circular cross section with a diameter of 0.500 inches. The maximum allowable axial deflection was 0.009 inches.

The first part of the assignment involved using analytical calculations to determine the required dimensions of the bar. I then created a parametric model in SolidWorks so that the dimensions of the bar were related to the design variables. Finally, I used SolidWorks Simulation to verify the design using FEA.

## Analyze
For the initial design, I selected a circular cross section with a diameter of: d=0.500 in. The cross-section area of a circular bar is: A=pi*d^2/4. Substituting the selected diameter into this equation, we get A=pi(0.500in)^2/4, which equals 0.19635in^2. The direct tension equation used to determine the length of the bar was: δ=FL/AE. Rearranging the equation to solve for the length, we get L=δAE/F. Using the knowns, we get L=(0.009)(0.19635)(10,000,000)/400= 44.18in. Therefore, the final analytical dimensions I used for the model were:
Applied force=400lbf, Elastic Modulus=10,000,000psi, Diameter=0.500in, Cross-Sectional Area=0.19635in^2, Maximum Deflection= 0.009in, Calculated Length=44.18in
<img width="683" height="883" alt="image" src="https://github.com/user-attachments/assets/7e2974eb-0b6e-4361-b766-f2acef719895" />
The photo above shows the calculations that were used to determine the cross-sectional area and length of the aluminum bar.

I also calculated the nominal tensile stress in the bar using: σ=F/A. Substituting the values in, σ=400/0.19635, and σ=2037 psi, or σ=2.04 ksi. 
Using the required aluminum yield strength of Sy=40 ksi, the theoretical safety factor is: n=Sy/σ. Plugging in the values, n=40/2.04, and n is approximately 19.6. This number means that based on the nominal analytical stress, the circular bar has a theoretical safety factor of approximately 19.6 against yielding.

## CAD
After completing the analytical calculations, I shifted over to SolidWorks to create the bar. I started by creating a sketch with a circular cross section and assigned the diameter as a parameter. The diameter was set to 0.500 inches, and the extrusion length was controlled using the calculated length of 44.18 inches. 

<img width="808" height="525" alt="1" src="https://github.com/user-attachments/assets/2fd0179c-72f4-48a1-8c20-d784f4881d4a" />

Here is my initial sketch with the diameter dimension defined parametrically.
I then extruded the circular sketch to create the bar. The extrusion depth was linked to the calculated length through the SolidWorks equation manager. This was one of the more challenging parts because I had never played around with global variables until this assignment. 

<img width="1168" height="612" alt="1" src="https://github.com/user-attachments/assets/ef20686a-ce2b-4283-9066-87eb842ece24" />

The picture above is the completed circular aluminum bar after I extruded the length of 44.18 inches.

## Parametric Design
One of the main goals of this assignment was to make the model parametric. To accomplish this, I created global variables for the major design parameters. 
The parameters used in my SolidWorks model included:
Force=400 lbf
Elastic Modulus=10,000,000 psi
Maximum Deflection= 0.009 in
Diameter= 0.500 in
Area= pid^2/4
Length=δAE/F
The area and length were calculated automatically from the other parameters. 

<img width="1015" height="414" alt="1" src="https://github.com/user-attachments/assets/839978b6-55d4-41f2-9e00-1f553f2cf4eb" />

The photo above is SolidWorks, the global variables, and equations used to parametrically control the bar geometry.
The extrusion length was then linked to the calculated Length parameter. It took some digging, and help from AI to help me figure out how to link these two so that if the length was changed, then if I changed the length of the bar, then the other parameters would change in response to the whatever the length was changed to. This was a neat feature to learn and learn how to link the different variables together!

<img width="1041" height="421" alt="1" src="https://github.com/user-attachments/assets/66901faa-a9e7-4583-a08f-e73ed4be485a" />

In addition to showing that the parametric parameters were working, this feature also is extremely useful. The model could be modified without having to manually recalculate and modify every dimension. For example, changing the applied force or maximum allowable deflection would automatically change the calculated length of the bar.

## FEA Simulation
After completing the parametric CAD model, I created a static FEA study in SolidWorks Simulation. This was also a neat bit to learn with as AI also helped me figure out what exactly I was looking at and how to set it up so I could see the stress, strain and displacement. The purpose of the FEA simulation was to verify the analytical calculations and determine the actual displacement and stress distribution throughout the bar.
The material assigned to the bar was 6061-T6 aluminum. The assignment called for an aluminum alloy of some kind with an elastic modulus between the givens on the assignments. 6061-T6 aluminum worked perfectly for this scenario.

For the boundary conditions, one circular end face of the bar was fixed. This represented the end of the bar being held in place. 

<img width="751" height="397" alt="1" src="https://github.com/user-attachments/assets/c05fdbc4-9ce7-4b34-8f93-1fbc558aa75f" />

Seen above is the fixed boundary condition applied to one end of the bar. 
A tensile force of 400 lbf, which is equivalent to approximately 1779.3N, was applied to the opposite circular face. I then created a mesh for the model before running the static study. After the mesh was generated, I ran the static FEA simulation. The simulation produced both a displacement plot and a von Mises stress plot.

## Deflection Curve
The first result examined was the resultant displacement of the bar.

<img width="101" height="318" alt="URES displacement" src="https://github.com/user-attachments/assets/aae5cafb-afc1-4dd5-bb51-4899d19e23f3" />

Seen above is the resultant displacement distribution along the aluminum bar. 
The analytical calculation predicted a maximum axial deflection of δcal=0.009in. The maximum displacement obtained form the FEA simulation was δFEA=0.05611 mm. Inverting this to inches gives the maximum displacement of δFEA=0.002209 in. My analytical value was δcalc=0.00900 in. The percentage difference here was the absolute valve of 0.002209-0.00900/0.00900 (100). This resulted in the percentage difference of 75.46%. The FEA deflection was 75.46% lower than the analytical value.
The differences between the analytical and FEA results can be attributed to the differences between the assumptions made in the analytical calculation and the conditions represented by the FEA model. The analytical equation assumes a uniform bar subjected to ideal axial loading, while the FEA model incorporates the specific fixture, loading condition, mesh, and material properties used in SolidWorks.

## Von Mises Stress
The second result examined was the von Mises stress distribution. 

<img width="349" height="705" alt="1" src="https://github.com/user-attachments/assets/33d55dac-753c-4f9f-93ae-6e8d6336a5dc" />

Seen above is the von Mises stress distribution throughout the aluminum bar.
The analytical nominal stress was σcalc​=2.04 ksi. The FEA simulation produced a maximum von Mises stress of σFEA=3.672 MPa. The stress plot showed 3.672*10^6 N/m^2, and since 1 MPa=10^6 N/m^2, that is how I got the σFEA of 3.672 MPa. Converting this to KSI, we do 3.672 MPa(0.145038)=0.5327 ksi. The analytical nominal stress was σcalc=400/0.19635=2.037 ksi. So the σcalc is 2.037 ksi. The percentage difference is the absolute value of 0.5327-2.037/2.037*100. The percentage difference is 73.83%, meaning the FEA maximum stress was approximately 73.83% lower than the analytical nominal stress.
The assignment also specified Sy=40 ksi. Therefore, n=Sy/σFEA, plugging in the values we have, we have n=40/0.5327, and n approximately equals 75.09. Our FEA safety factor is approximately n=75.1m and the maximum FEA stress was required aluminum yield strength of 40 ksi. Since this value is below the 40-ksi yield strength, the design of this beam passes the required yield-strength condition.

## Decide
After analyzing the overall results, I was able to compare the analytical calculations with the SolidWorks FEA results. The analytical calculation predicted a maximum axial deflection of 0.009 inches, while the FEA simulation produced a deflection of σFEA=0.002209 inches. The percentage difference between the two results was approximately 75.46%.

The difference between the analytical and FEA results can be explained by several factors, including the material properties used in the simulation, the assumptions made in the analytical equation, the boundary conditions, and the mesh used during the FEA analysis. The analytical calculation assumes an ideal uniform bar under direct axial tension, while the FEA model attempts to represent the actual loading and fixture conditions.

The FEA simulation also produced a maximum von Mises stress of σFEA=0.5327 ksi, which was compared to the required aluminum yield strength of 40 ksi. The resulting safety factor was approximately n=75.1. Since the maximum stress remained below the yield strength, the bar satisfies the required strength condition.

Overall, I believe the analytical calculation is useful for determining the initial dimensions of the design because it provides a quick way to estimate the required length. However, I would trust the FEA result more when evaluating the behavior of the actual modeled part because the simulation accounts for the specific geometry, constraints, loading conditions, and mesh. The analytical calculation is still important because it provides a way to check whether the FEA result is reasonable

Adding a hole would create a stress concentration around the hole's location. The nominal stress away from the hole would not fully represent the maximum stress at the edge of the hole. The peak stress can be estimated using the stress concentration factor: σmax=Ktσnominal where Kt is the stress concentration factor, and σnominal is the nominal stress away from the hole. The FEA nominal stress away from the hole would be used with an appropriate Kt obtained from Peterson's Stress Concentration Factors or Machinery's Handbook.

The estimated peak stress would then be compared with the 40-ksi aluminum yield strength: n=40 ksi/σmax. If the resulting safety factor remains greater than the required value, the design would still pass. If the stress concentration causes the safety factor to become too low, the hole would make the design unacceptable even though the original bar without the hole passes.

I would not rerun the FEA for this part, since the assignment specifically asks for the hole effect to be estimated using the stress concentration factor. 

## Communicate
This assignment helped me better understand how analytical calculations, parametric CAD modeling, and FEA can be used together during the engineering design process.

One of the most useful parts of the assignment was learning how to make the SolidWorks model parametric. Instead of manually entering the length of the bar, I was able to connect the length to the force, elastic modulus, maximum deflection, diameter, and calculated cross-sectional area. This allowed the model to automatically update when the design variables changed. AI helped me understand and how to set up the global variables and how to link them.

I also learned more about setting up an FEA simulation. I had to learn how to assign the material, apply a fixed fixture, apply the tensile load, create the mesh, run the simulation, and interpret the displacement and von Mises stress results. AI was also extremely helpful here because it helped walk me through what I needed to ensure was working correctly. 

I did have some difficulty learning the SolidWorks FEA tools, particularly when setting up the simulation and making sure that the correct loading conditions were being used. However, working through these problems gave me a better understanding of how FEA is used as an engineering design tool.

Overall, this assignment demonstrated a more realistic approach to engineering calculations because I was able to use theoretical equations to create the initial design and then verify the design using a computer simulation. This showed me that analytical calculations and FEA can complement each other when evaluating an engineering design. This assignment as a whole took me about 5 hours; the simulation and setting the global variables took the longest time in the whole assignment.

Here is the link to my part: https://drive.google.com/file/d/1gVDgQwTVCpp5MYb0-Quvh19PHpMP_FDU/view?usp=drive_link
