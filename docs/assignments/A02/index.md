# A2 – Truss Stress Analysis

## Objective
The objective of this project was to design a truss able to hold a given load. We had to design the truss on paper and CAD as well as calculate the dimensions based on certain properties.

## Analyze
## Design Phase
I chose to go with the trapezoid and have two beams where the truss formed two triangles and a rectangle. The requirements for this project are given in the photo below.

<img width="317" height="215" alt="download" src="https://github.com/user-attachments/assets/24e91bf2-eac3-4d3b-a687-b7545956c490" />

I chose to have 25kN as my P, and my width at 0.4m, and height at 0.3m, like the instructions told us too. 

## Forces
<img width="1276" height="278" alt="1" src="https://github.com/user-attachments/assets/c443427d-6c77-4db0-8fcb-202fcffb29e0" />
In the photo above, the truss design I described in the beginning is shown. I drew a trapezoid, and then added two more beams to make two triangles and a rectangle. This involved also finding the forces at those two points, labeled E and F, alongside finding the rest of both the internal and external forces. For the external forces, I found the moment around A, and discovered that my By was what I initially picked for my P. Continuing the math, as seen below, I also discovered that Ay was also 25kN as well. Every square on my graph paper was 0.4m, so it would make it easier to draw the truss design I had in mind.

<img width="1276" height="893" alt="1" src="https://github.com/user-attachments/assets/21606124-f614-4a14-8d10-70be7f2aed9f" />
For the internal forces, I took the inverse tangent of the width and height and found my theta. Then, using the sum of the forces in the x-direction, I found what my AB section was, which was 33.3333 kN compression, since the initial answer was negative. I continued this process with AD, BC, and CD, and also found that points E and F had the same force as my P, because the truss is not moving, and it is in static equilibrium. I drew pictures that helped me visually keep the parts separated so I could focus on one section at a time. 

## Cross-Sectional Area
Alongside seeing the rest of the force math I did, I also included the math of finding the cross-sectional area and yield strength. I found what Fmax was, and that was from previous calculations involving the forces. After doing some research, I chose an alternative metal; steel. The density of steel is 7850kg/m^3. Taking into account the safety factor of 3.5, I found the area by multiplying the force and safety factor, then dividing the answer by the stress. This stress number also came from the research I did on steel.
I found the weight of the truss using the area and length from before. I also found the mass and weight. 
I took into account another safety factor, this one of 4, and found the area of the pin by multiplying Vmax and the safety factor, then dividing by Ty to get my answer. I also found the diameter of the pin as well, and drew a free body diagram showcasing where Vmax on the pin would be.
<img width="1276" height="761" alt="1" src="https://github.com/user-attachments/assets/387d91e5-dcf6-4730-8d13-e81943bc8298" />
<img width="1276" height="155" alt="1" src="https://github.com/user-attachments/assets/f44efc2a-2c0c-4def-aab1-d6cd6c3efc55" />

## CAD Design
This is where I became frustrated with myself and how rusty my skills were. As shown initially, I drew a sketch of how I wanted the truss to look. It looks exactly how the sketch in the previous section looks; there is a trapezoid as the exterior, and then two beams inside with hollow areas of the two triangles and rectangle to make the truss. 
<img width="676" height="278" alt="Screenshot 2026-08-31 232727" src="https://github.com/user-attachments/assets/6fba212a-4d4a-41ff-a9af-8c49b15af9c4" />
<img width="575" height="307" alt="Screenshot 2026-08-31 232739" src="https://github.com/user-attachments/assets/ff273b4c-c938-46f2-ba1e-a7edf2620c20" />

Then came the part I got more and more frustrated with. I wanted to extrude the base (the trapezoid), and then cut out the interior face with the two beams so it would be hollow except for the beams. This did not work how I wanted it too; I extruded, and the software would not let me extrude more than one part of the initial sketch at the time. I tried weldments, and had easier success this way, but when it came to trying to rotate and get the parts to line up, I grew more and more frustrated, so I took what I had and screenshotted it to show my work up to this point.

<img width="780" height="320" alt="Pt2" src="https://github.com/user-attachments/assets/3473a3bf-0d2d-43e4-b89c-9fa4701eae91" />

Due to my frustrations, I did not model the pin. I did find the diameter and everything for it that was required, but did not model it. If I had modeled it, it would've been a cylinder with some tweaks on the edges to ensure diameter and everything that was found in the last photo, such as the length, worked and there was nothing over-defined or under-defined in Solidworks.



## Decide
I selected a trapezoid base with two more beams in between the curves and straightness of the trapezoid. I chose this design because even though it required a bit more math to figure out the forces, it also made more sense too in terms of safety and structural security. The two beams on the inside provide more support, rather than just having the truss be an open all the way around trapezoid, to me it made sense to put some support beams on the inside, so that the inside would be secure, and the safety factor and weight of the entire truss was taken into account for, and provided more safety if there was to ever be a strong wind or anything of the nature that would endanger a truss of a bridge.

## Communicate
I discovered very quickly through working on this assignment that my CAD skills are extremely rusty! I went to extrude the base of the trapezoid and two beams that formed the triangles and rectangle and found that the software would not let me do it the way I wanted too. I also attempted to use weldments, and that method was going fine until the rotations and having to merge everything together got me frustrated. For other assignments that require CAD, I will ensure my skills are up to par for what is required for the upcoming assignments. 

