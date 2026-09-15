# A4 – [Motor Mount]

## Objective
The objective of this assignment is to use the working knowledge acquired to design a motor mount. We have two distinct directions, the first direction is obtained from stress; the second is from the deflection using beam calculations.

## Analyze
To approach this assignment, I first needed to figure out yield/stress and the maximum deflection for the beams. The assignment gave us a variety of parameters; these including the specs of the motor, structural requirements, such as the material, neglecting the motor weight, the safety factor, the maximum deflection, and what we needed to analyze for each feature.
<img width="1276" height="401" alt="1" src="https://github.com/user-attachments/assets/10fa82bf-0b53-4153-9dc5-ac3ff14c66a6" />

Before I started even opening up Solidworks, I went ahead and decided how to treat the safety factor. The maximum torque of the motor is approximately 3.6 kgcm. I had to convert this to N*mm. 
<img width="1276" height="179" alt="1" src="https://github.com/user-attachments/assets/5b78584b-cc40-4403-870f-6953d254e84d" />
In the image above, we see the work I did to convert kg*cm to N*mm. This results in 353.16 N*mm. The appendix B beam diagram, the applied moment of M=PL. The P is 900N, we will not divide the material yield strength by 3. 
<img width="1276" height="698" alt="1" src="https://github.com/user-attachments/assets/64a5cec5-0de5-4f96-a070-c524821b0caf" />
We are given three materials to choose from the assignment. I decided to choose PLA as my material. Young's modulus is 2346.5 MPa, and the tensile yield is 49.5 MPa. I chose PLA because it is a reasonable, readily printable material with a relatively well-defined stiffness value for the calculation. However, 3D printed parts are not perfectly isotropic. The actual stiffness depends on geometry, print settings, layer adhesion, infill, extrusion temperature, and print orientation. 

## Feature 1
After looking at Appendix B, I decided to break the features down into a shelf almost.  The motor sits on the horizontal section that will become Feature 1, and the right side of the motor will be attached to the vertical part of the shelf, which will become Feature 2.
<img width="1276" height="698" alt="1" src="https://github.com/user-attachments/assets/b9f4aeb7-6354-470f-a59f-be1ba107e5d3" />
For this, I made a design assumption; the beam length. Going off of the motor body (38mm), the gearbox (36.6mm) and shaft (18mm), the total length of the beam I assumed was going L1=38+36.6+18=92.6mm. I am assuming the beam's fixed end is approximately at the rear of the motor, and that the load acts near the shaft end. 
I drew a FBD, and we can see the fixed end, and the load end. 
<img width="1108" height="1396" alt="1" src="https://github.com/user-attachments/assets/d7f101a4-002f-4624-9aff-6a61b4474e0d" />
The moment here is 83,340 N*mm. For the beam calculation, I simplified Feature 1 into a rectangular cross section. To calculate the rectangular beam, we need to find the inertia using the equation I=bh^3/12. The h^3 is huge here, because increasing the beam depth has a huge effect on stiffness. This means that deeper sections and ribs will be useful in the actual CAD model. 
To find the bending stress, we use the equation shown below after lots of substitution.
<img width="1113" height="1396" alt="1" src="https://github.com/user-attachments/assets/7375c3c9-49a8-49e0-b2ba-bd7a047de2c4" />
After substitution and solving, we get a height of h1 stress yield-strength of approximately 14.2mm. 
Now to find the maximum deflection for Feature 1 , more substitution happens, and we get an equation looking like the one below. After plugging in the known values, we get a deflection for h1 deflection of approximately 49.6 mm. 
<img width="1113" height="1396" alt="1" src="https://github.com/user-attachments/assets/f5880fe8-db28-4bf9-9dc3-2fcf2cc82c44" />
I don't want to manufacture something exactly at 49.6mm, so I rounded up to 50mm. The deflection governs Feature 1, so the analytical section is 50mm wide * 50mm deep. 
After checking that both the stress of 4.00<49.5, this means that the yield part holds up, and the beam passes. The deflection of 0.292<0.30 also shows that the deflection part of the beam passes, and passes under the maximum required deflection. 

## CAD Model (Parametric)
<img width="421" height="364" alt="1" src="https://github.com/user-attachments/assets/ba60d565-0bb6-4808-b75e-a15f4d3113ad" />
This is the first step I did, I sketched on the front plane and did a rectangular cross section of 50*50. I extruded it 8 mm, and then added another part on, which is what the second overlap is. This was also extruded to 8mm, so now there is a horizontal bit of the shelf, and that is what we are looking for in Feature 1.
<img width="996" height="688" alt="1" src="https://github.com/user-attachments/assets/b88e6a20-1076-4f40-ba69-d8a6964fee66" />
I drew a .30mm circle as a reference, and then attempted to draw 4 .22mm M3 holes using the hole wizard and the points on SolidWorks. Unfortunately, this process took a lot longer than I anticipated, and began to grow quite frustrated with it. These four holes would be where the parts of the motor with the fixed end would go. I am realizing that SolidWorks has a lot of smaller things that need to be ensured are properly fixed all the way, or things will not work!

## Feature 2
Feature 2 is the vertical portion of the mount for the motor. This support Feature 1, but in the y-direction rather than the x-direction. Appendix B diagram also represents the lower, or free section as bending under another applied moment; this made me decide to use another cantilever-type beam to model this part.
Moment 2 is equal to Moment 1, so M2 is also 83,340 N*mm. Appendix B does not give a numerical Feature 2 height. I made another assumption, and said that L2 was 50 mm. I carried over the base as 50mm as well. So the variables here are B2=50mm, L2=50mm, and M2=83,340N*mm. 
Using the same equations as used in feature 1, we get that h2 stress is approximately 14.2 mm. The deflection for h2 is approximately 32.9 mm. I rounded this deflection up to 35 mm to give some wiggle room for errors.
The moment of inertia for this beam is (50)(35)^3/12, which is approximately 178,646 mm^4, The stress is 6(83,340)/(50)(35)^2, which is approximately 8.16 MPa. Since 8.16<49.5, this beam also passes the yield test. For deflection, we get approximately 0.249mm, and 0.249<0.30, the deflection also passes.

I calculated the motor mount geometry using the Appendix A. The gearbox diameter is 28mm, the shaft diameter is 6mm, the shaft length is 18mm, and the mounting holes 4*M3, which means that the mounting hole circle needs to be .22m in diameter to accommodate the mounting holes. These will go 90 degrees from each other around the 22mm diameter mounting circle. 

I also planned on having a shaft clearance, which would be around the 6 mm diameter shaft. Two gussets that would be triangular and support both Features 1 and 2, and then fillets at the Feature 1/Feature 2 intersection. I would have created variables like the Motor_diameter=28mm, Shaft_diameter=6mm, etc., just like last week's assignment.

## Decide

I chose a simple L-shaped motor mount consisting of the horizontal mounting platform alongside the vertical rear support. I chose this design because it was a straightforward way to support the motor while keeping the design compact and easy to manufacture The horizontal features support the motor, and the vertical component transfers the loading from the motor into the mounting surface surface. I also decided this design because it was a good starting point to begin to incorporate more kind of like elegant designs, like the fillets and gussets. These allow the design to use the additional material in the areas where it contributes more effectively to stiffness, and allows the mount to remain lightweight while improving the resistance to bending. 

I modeled the horizontal and vertical portions as simplified cantilever beam features so it made it easier to determine the required dimensions analytically, rather than guessing on the dimensions. The gussets were important because they allowed the design to have the required stiffness without creating an unnecessarily large block of material. The triangular gusset provides additional structural depth between the horizontal platform and vertical wall. By increasing the effective section depth, it has a huge effect on the bending stiffness I learned due to the H^3 relationship in the inertia equation. 

## Communicate
I have learned throughout this assignment that SolidWorks is extremely particular and you have to be precise with every single click. Whether this means ensuring the points are in the right spots for the hole wizard to work correctly. I am still learning all of the ins and outs of SolidWorks while also learning new design applications and how to fully use them on SolidWorks itself. 
Another thing I learned was correctly applying the safety factor. The first time I did this, I applied it twice on accident. When I went back and rechecked, and had AI check my math to ensure everything was working properly, we both caught that I had done the safety factor twice instead of just once. 
Deflection became the huge requirement for this project. A component can have a relatively low calculated stress, but still fail the design requirements because of excessive deflection. For this assignment, stiffness became the important design consideration compared to the others.
This project in total took me about 7-8.5 hours from start to finish, alongside the frustrations of SolidWorks.
