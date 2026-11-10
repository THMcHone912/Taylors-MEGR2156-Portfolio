# A9 – Pulleys

## Objective

The objective of this project is to design and analyze a belt-driven pulley system capable of transferring rotational power between two parallel shafts. The system consists of two identical 3-inch-diameter pulleys connected by a polyurethane rubber belt.

The design must satisfy the dimensional, operating, material, and safety requirements established in the assignment. Engineering principles involving static equilibrium, friction, torque transmission, material strength, shaft design, and journal bearing performance will be applied to evaluate the system.

The design requirements are: Two pulleys with identical diameters of 3 inches, shaft center distance between 4 and 6 inches, operating rotational speed between 1,000 and 2,000 rpm, static belt tension between 4 and 6 lbf, polyurethane rubber belt with a specified yield strength of 471 psi, aluminum, ABS, or steel pulley construction, and a minimum design safety factor of 3.

Journal bearings selected based on pressure, surface velocity, and PV limitations.


## Analyze

We are given the knowns of the diameters (3 inches), radii (1.5 inches), circumference (5 inches), N=1500 rpm, Fi=5lbf, mew=0.20, sigmay=471 psi, and n=3. The unknowns are T1, T2, torque, belt area, belt diameter, and belt circumference. 

Based on a free body diagram, we can come up with the equation that torque=(T1-t2)r; substituting values in, we get torque= 63025(0.10)/1500= 4.202 lbf*in. After we figure this out, we need to rearrange to find the difference in the belt tensions. we get T1-T2=torque/4, after substituting values in once again, we get T1-T2=4.202/1.5, which ends up equaling 2.801 lbf.

We also need to take into account that the belt drive has an initial static tension of 5 lbf. The equation we use is Fi=T1+T2/2. Rearranging this, we get T1+t2=2Fi. Substituting values in, we end up getting T1+T2=10 lbf. 

We now have both equations needed to figure out both tensions. For T1, we use 2T1=12.801; we divide this by two and get T1=6.401 lbf. We then subtract this and end up getting 2T2=7.199. We divide this number by two and get T2=3.599 lbf. The initial static tension remains at 5 lbf before power goes through the pulleys.

We now need to check and ensure there is no slippage of the pulley. We can use T1/T2<e^mew*theta. The equation to use here for two equal pulleys on an open belt is theta=pi*radians. We calculate the tension ratio by doing T1/T2=6.401/3.599, and end up getting 1.778. We then need to figure out the maximum allowable tension ratio, so we plug in e^0.20*pi and get 1.874. Since 1.778<1.874, these calculations predict that the belt can transmit the torque without slipping.

Now, we need to figure out the required belt cross-sectional area. The yield strength of our material is 471 psi. Using the equation of the safety factor, n=sigmay/sigmaallow and rearranging via algebra, we get sigmaallow=sigmay/n. Substituting values in, we get 471/3, and we get that sigmaallow=157psi. Our normal stress equation is sigma=F/A; after we rearrange to solve for A, we get 6.401/157, which means our area is 0.04077in^2. For the circular cross section, we have A=pi*d^2/4. After rearranging, we get d= sqrt 4A/pi. After substituting values, we get that the diameter is 0.2279 in. A preliminary belt size of 1/4 inch is selected. That means that the actual area is 0.04909 in^2. The resulting tensile stress we get with actual numbers is 130.40psi, and the safety factor is 3.61.

Lastly, we need to calculate the belt circumference. For two pulleys that are connected on an open belt, the equation is L=2C+pi*d. After substituting values in, we get L=19.425 in. The actual belt circumference must be adjusted for the groove geometry and the belt seating. This number is just an approximate pitch-line circumference, assuming that the belt runs at the pulley pitch diameter. 

Next we need to determine the minimum shaft diameter required to transmit the calculated torque. We can use solid circular shafts made from 1060 hardened steel. The shaft calculations need to consider torsional loading, since the assignment requests it.

Our knowns are the transmitted torque (4.202 lbf*in), shaft material (1060 hardened steel), assumed yield strength (100000 psi), required safety factor (3), shaft type (solid circular shaft), and a number of shafts (2). Our unknowns are maximum allowable shear stress, minimum shaft cross-sectional area, minimum shaft diameter and the selected practical shaft diameter.

We need to have a material assumption here. The 100 ksi yield strength is just a preliminary design value currently; it is not a verified property of every 1060 hardened steel condition. Actual yield strength depends on the heat treatment and hardness. We need to verify the material specification before finalizing the shaft design. 

We calculate our torque using Ty=Sy/sqrt 3. Substituting numbers in, we get Ty=57735.03 psi. After we apply the safety factor using Tallow=Ty/n, we get 19245.01 psi. 

We now need to calculate the maximum torsional shear stress using Tmax=16T/pi*_d^3. Rearranging, we get d^3=16T/pi*tallow. Substituting values, we get the minimum diameter must be 0.1036 in. The minimum cross sectional area is A=pi*d^2/4; once we plug in values, we get the minimum cross sectioal area= 0.00843 in^2.

We also need to have journal bearings that support the shafts while allowing them rotation. The bearings material must withstand the radial loads and rotational speed without exceeding the allowable pressure velocity rating. For the preliminary design, I am selected oil impregnated porous bronze bearings.

Our knowns for these bearings are their diameter (0.250 in), shaft speed (1500 rpm), tight side tension (6.401 lbf), loose side tension (3.599 lbf), bearings per shaft (2), selected bearing length (0.500 in), and the material (porous bronze). Our unknowns are the radial load on each bearing, the projected bearing pressure, the journal surface velocity, the PV rating, and if the material is a suitable bearing material.

For an idealized pulley that has two parallel belt strands, the radial load on the pulley is around the sum of the belt tensions. We can roughly approximate this by using Fr=T1+T2; after substituting values, we get Fr=10.00 lbf. We can assume that the bearings are equally spaced and share the radial load equally. The equation we use here is Ra=Rb=Fr/2, Ra=Rb=10/2, and we get 5.00lbf. This number assumes that the pulley load is centered between the two supports. An actual overhung pulley or unequal bearing spacing would require a different reaction calculation.

Our projected bearing pressure is P=W/LD; after we substitute values, we get P=40 PSI. The journal surface velocity is V=pi*D*N/12, after we substitute values, we get V=98.17ft/min. Now we can calculate the PV rating using our PV=O(V). We substitute values once again and get that PV=3926.99 psi*ft/min. For a preliminary comparison, porous bronze bearing guidance gives a general PV limit of around 50000 psi*ft/min without 20000psi*ft/min suggested for long-term operation without more lubrication. Using the more conservative 20000 value, we get PVcalculate<PVallowable, annd 3926.99<20000, meaning that the preliminary PV check passes.

The supporting frame needs to hold the two pulley shafts in alignment and resist the forces generated by the belt. The knowns are the pulley center distance (5 in), radial belt force (10 lbf), frame material (6061-T6 aluminum), assumed yield strength (35000 psi), frame member width (3 in), frame member thickness (0.25in), unsupported span (5 in) and a minimum safety factor (3). The 35 ksi yield strength is also another assumed preliminary value for the 6061-T6 aluminum. Our unknowns are the support reactions, maximum bending moment, area moment of inertia, the maximum bending stress, the frame safety factor and the maximum deflection. 

The reactions are Fy=0, so Ra+Rb-10=0; by symmetry, Ra=Rb, and these both equal 5 lbf.
Now we can calculate the maximum bending moment using Mmax=PL/4. After we substitute values, we get that Mmax=12.5 lbf*in. We can also calculate our area moment of inertia for a rectangular cross section using I=bh^3/12. We substitute our values in, and we get that I=0.003906 in^4. We can also calculate our maximum bending stress with sigmamax-Mc/I. After we plug in our values, we get that sigmamax=400 psi. We can also calculate the frame safety factor using n=Sy/sigmamax; we plug in values and get that n=87.5 The caluclated safety factor is greater than the required minimum of 3. We can then calculate the meximum deflection using deflectionmax=PL^3/48EI; we assume that the elastic modulus of aluminum is 10000000 psi. We plug in our values and get the max deflection= 0.000667 in. This suggests very little deflection under the assumed loading conditions.
## Decide

Now that our calculations are finished, we need to select a belt. The preliminary calculations we have done calls for a 1/4 inch diameter round belt. The site provided (McMaster-Carr), lists a 1/4 inch polyurethane round belt in an outer circumference range that includes the required length. The catalog always identifies 2 inches as the minimum pulley diameter for the 1/4 inch round belting, so the 3 inch pulley that we are given satisfies the limitation. However, it should be noted that the catalog's outer circumference is not the same as the belt centerline circumference. Therefore, the final purchase length should be selected using the outer-circumference measurement and checked against the pulley groove geometry.

The belt design was developed using the torque transmitted between two identical pulleys. Both pulleys have a diameter of 3 inches, and the system has a 1:1 speed ratio. The selected operating speed of 1500 rpm results in both pulleys rotating at the same speed.

The tensions were calculated using the initial static tension and the torque transmitted through the pulley. The tighter side was found to be around 6.40 lbf, and the looser side was around 3.60 lbf.

The required belt cross-sectional area was determined using the specified polyurethane yield strength and a safety factor of 3. A 1/4 inch belt was selected because its calculated tensile stress is around 130.40 psi, and it produces a safety factor of around 3.61.

The friction relationship also shows that the selected tension ratio is below the calculated limiting ratio for the assumed coefficient of friction. This shows and suggests to us that the belt can transmit the selected torque without slippage. 

We do have a limitation that involves the friction coefficient and belt properties. These must be verified for the actual polyurethane compound and aluminum pulley surface. The calculations also neglect centrifugal tension and assumes that it is an idealized belt contact model. 

We need to now select a practical shaft diameter. Although the calculations show that the minimum diameter is around 0.104 inches, I am going to select a larger shaft to provide additional stiffness and manufacturing dimensions. I'm selecting a diameter of 0.250 inch. Therefore, our actual torsional stress=1370.7 psi, and our actual safety factor=42.12. The selected 1/4 inch shaft exceeds the required minimum safety factor under the torsion only model.

However, this calculation does not include stress concentrations at keyways or shoulders, bending stress, or shaft deflections. These factors would need to be evaluated using the actual shaft and bearing geometry before treating this as a complete shaft design and going forward with it.

The journal bearings were evaluated using the radial load generated by the belt tensions. The combined belt force was calculated as 10 lbf and divided equally between two bearing supports. The projected pressure was calculated as 40 psi, the surface velocity was around 98.17ft/min. Multiplying these two values together gave a PV rating of around 3927 psi*ft/min. This value is below the conservative preliminary PV limit of 20000 psi*ft/min used for the material comparison. Therefore, the oil-impregnated porous bronze is a suitable preliminary bearing selection.

The bearing length of 0.5 inches was selected because it provides sufficient projected bearing area while maintaining the compact assembly. 

The preliminary pulley system was designed around two identical 3-inch pulleys separated by a 5-inch center distance. An operating speed of 1,500 rpm was selected, resulting in a 1:1 rotational speed ratio between the two shafts.

The belt analysis established the tension difference required to transmit the assumed 0.10 hp. A 1/4-inch polyurethane belt was selected based on its calculated cross-sectional area and tensile stress.

The shaft analysis determined that a minimum diameter of approximately 0.104 inches was required under torsional loading alone. A 1/4-inch shaft was selected to provide additional strength and a practical mounting dimension.

The journal bearing analysis evaluated the radial load, projected pressure, surface velocity, and PV rating. Oil-impregnated sintered bronze was selected as the preliminary bearing material because its properties are suitable for rotating shaft applications.

The supporting frame was evaluated as a simply supported aluminum member subjected to a central 10 lbf load. The material selected for the preliminary design was 6061-T6 aluminum due to its strength, relatively low weight, and suitability  for structural applications. 

The maximum bending stress was calculated as 400 psi, resulting in a safety factor of 87.5 using the assumed yield strength of 35000 psi. The calculated deflection was around 0.000667 inches.

These results show that the proposed frame member has sufficient bending strength under the simplified loading model. The small calculated deflection also shows that the member should maintain its shape under the assumed load.

The frame analysis is preliminary because the actual support geometry, mounting locations, local bearing loads and fasteners have not been fully modeled. These features must be considered before the structure is finalized.

Overall, the calculations indicate that the proposed design satisfies the minimum safety factor requirement in the individual simplified analyses. Additional verification of material properties, friction, bearing specifications, and actual structural geometry is necessary before considering the design finalized.

## Communicate

Throughout this project, I learned how multiple mechanical engineering concepts work together when designing a power transmission system. One of the most important concepts was understanding the relationship between belt tension and transmitted torque. The difference between the tight-side and loose-side tensions determines the amount of torque transferred between the pulleys. Increasing this tension difference increases the torque that can be transmitted, but it also increases the loading experienced by the shafts and bearings.

Another important lesson was understanding how friction affects belt performance. The friction relationship between the belt and pulley determines whether sufficient traction is available to transmit power without slipping. This demonstrated that selecting a belt requires more than simply matching its diameter and circumference to the pulley dimensions.

I also learned how material selection and safety factors influence component dimensions. The shaft calculations demonstrated that a component may have sufficient strength at a relatively small diameter, but selecting a larger practical diameter can provide additional strength and accommodate manufacturing and mounting requirements.

The journal bearing calculations introduced the importance of pressure and surface velocity when selecting bearing materials. A bearing must support the applied load while operating within its allowable PV rating. Selecting a bearing based only on its physical dimensions would overlook the effects of friction and heat generation during operation.

Finally, the frame analysis demonstrated the importance of evaluating both stress and deflection. A frame must maintain sufficient strength while also limiting deformation to preserve shaft alignment. Excessive deflection could affect belt tracking and the overall operation of the pulley system.

This project helped me understand how static analysis, rotational dynamics, friction, material properties, and mechanical design are interconnected. Each component must be evaluated not only individually but also in relation to the forces and operating conditions of the complete system.

This assignment took me around 2.5 hours to complete from start to finish.
