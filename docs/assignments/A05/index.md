# A5 – [Bracket Design]

## Objective
The objective of this project was to design and analyze a mechanical bracket subjected to a horizontal load applied to symmetrically through a polyester strap. The component will be designed using strengths of materials provided, including bending stress, stiffness analysis, and normal stress. The final dimensions will be selected by comparing the requirements from deflection and stress.

## Analyze

## Requirements
In the assignment handout, we are given that the applied force must be between 500 and 800 lbf. We are also given a safety factor of 4. The maximum allowable deflection for the bracket is 0.005 in. Both shear deflection and direct shear failure is neglected. The design method is for stress and stiffness, and we are given 3 materials to work with and design the bracket.

## Assumptions
Before the calculations and multi-sectional drawings are shown, we're going to state our general assumptions here first and foremost so we know what we're working with assumption-wise. 
Our assumptions are that our material is isotropic and homogeneous. The applied load is static. The load is distributed symmetrically. Direct shear failure is neglected. Shear deflection is negligible. Small-deflection beam theory is applicable. The connections are treated according to the simplified models that are seen in the assignment. A safety factor of 4 is used, and the maximum allowable deflection is 0.005 in. 

## Feature A Stress Analysis

Now that we have stated our assumptions, we dive into the features and their stress analysis. For Feature A, we are told in Appendix D to treat A as a cantilever beam. In the photo below, I drew a quick model of how I ideally would like Feature A to look.

<img width="383" height="189" alt="IMG_3636" src="https://github.com/user-attachments/assets/96369f50-e5b4-45a5-81e4-ec12202f1537" />


For a cantilever beam, the force at the free end produces a maximum bending moment at the fixed end. For my working assumption, I'm using F=750 lbf, L=1.00in, the safety factor is N=4, I'm using A36 steel as my material, and my Sy=36 ksi. 

In the photos below, I show my calculations for finding the max bending moment, the allowable stress, the required section modulus, the solid circular section and the required diameter. 

<img width="363" height="487" alt="1" src="https://github.com/user-attachments/assets/0e322abb-fc67-4d0a-9451-b93c6f243de9" />


## Feature A Stiffness Analysis
The maximum allowable deflection is given to us in the assignment; it is 0.005 in. We still treat A as a cantilever beam. I have to find the minimum area moment of inertia to keep the deflection exactly at 0.005 in or lower. In the picture below, I show the algebra I used to get I by itself so we can solve for it. I then plug my numbers in and do some math. 

I found the minimum area moment of inertia at 0.00172 in^4. I then turned this number into a diameter. In the picture below, I show the algebra and the calculations to find it. 

<img width="382" height="296" alt="1" src="https://github.com/user-attachments/assets/c9f1fa2b-72a2-4b73-bc49-de243958c68d" />


I then did my free body diagram to show why I did the calculations I did.

<img width="440" height="234" alt="1" src="https://github.com/user-attachments/assets/42b76312-0b8d-49eb-bb90-05decb914e41" />

## Feature B Stress Analysis

Appendix B tell us to treat B as an axially loaded bar. This means that B will primarily experience axial forces. I drew my free body diagram, and placed it below.

<img width="273" height="193" alt="IMG_3642" src="https://github.com/user-attachments/assets/5b3cc15e-d22c-43c4-8698-c1ff3606ce9d" />


Since the bracket is symmetrical, I cannot automatically assume that the entire 750 lbf is going to be applied to B, and need to figure out if B will carry the full applied force, or just a portion of it. In the picture below, we see the set up I use to figure out if it's just a portion or the entire load.

I then find the cross-sectional area required for the normal stress. Feature B is a rectangular bar, so the cross-sectional area equation is A=bt, where b is the width of B, and t is the thickness of T. From my current model on CAD, I have t set at 1.00 in, and we can use this here to solve for the required width. From the picture below, you can see the calculations I did, and that I found the minimum width B based on normal stress under my current assumptions

<img width="340" height="193" alt="IMG_3637" src="https://github.com/user-attachments/assets/8b3ec6f4-2ed6-4ed9-83f7-09ecf9dcea58" />


# Feature B Stiffness Analysis
I show the algebra in the picture below to rearrange for A since I need to find the required area. I then plug in my knowns and calculate the area needed. Seeing the number I calculated, under my current assumptions, the stress requires a larger cross-sectional area.

I can also use the same cross-sectional area to find the minimum width. In the next picture, I show my calculations to get the minimum value I need for width. 

<img width="853" height="409" alt="1" src="https://github.com/user-attachments/assets/5d5ae2f7-ef48-4258-a290-88657ed6ef15" />

<img width="373" height="589" alt="1" src="https://github.com/user-attachments/assets/8f259aa2-4cac-45c0-9865-4dd7044e3c4a" />

Stress governs Feature B, because 0.04167>0.00559. However, an important caveat is that these are theoretical minimums based on the the current assumptions. That does not necessarily mean that these are the dimensions that will go into CAD. The actual bracket geometry and load path will determine the practical dimensions used.

## Feature C Stress Analysis
Appendix D tells us to treat Feature C as a simply supported beam with a concentrated load at the center. Below is what the free body diagram would look like. 

Since the loading is symmetric, we need to establish the load that is acting on C. In the next picture, I show my calculations to determine what force C actually carries. 

Now I can use the same equation used in Feature A to find the required section modulus. In the photo below, the calculations to find this value are shown.

Now I need to convert the section modulus into a dimension for Feature C. Since C is a rectangular beam, we'll use the equation S=bh^2/6. In the next picture, I show the algebra to isolate h, and then the math to find the value of h we need for the height. So the minimum beam height of 0.357 is needed based on the bending stress.

## Feature C Stiffness Analysis
The assignment states that our maximum deflection can be equal to or less than 0.005 in. In the photo, I show myself rearranging the deflection equation for a center point load of a simply supported beam to find I. After I isolated I, I plugged in the values I had to find. 

Now, we need to turn the I value into a required height of C. I show my work in the photo below to find these calculations and limit.

<img width="364" height="193" alt="IMG_3645" src="https://github.com/user-attachments/assets/b2cebede-4ed3-4803-8882-74b79d31a202" />

<img width="332" height="193" alt="IMG_3643" src="https://github.com/user-attachments/assets/8ce45809-34a9-4f9f-856b-89c3937577d7" />


After finding the required height of C, we see that stress also governs Features C because the stress requirement is larger. 

# Feature D Stress Analysis 
I started off by drawing my FBD for Feature D. It is seen in the photo below.

<img width="570" height="399" alt="1" src="https://github.com/user-attachments/assets/a4b13e90-723f-4891-a2fc-8541af401242" />


Next I use the M-PL and plug in my values. I then move onto finding the required section modulus. I then turned S into a physical dimension, and the work is also in the photo below. Under our current working assumptions, D needs to have a bending height of at least 0.5362 in. to satisfy the allowable bending stress.

<img width="506" height="368" alt="1" src="https://github.com/user-attachments/assets/4fb6fb9f-6716-460d-b879-1aef88a28d0b" />


# Feature D Stiffness Analysis
Now, I show my algebra in the photo below and plug in my values to find the required moment of inertia I. I then had to find the required thickness, and my working dimensions is currently b=1.00in, so after we rearrange and solve for the cube root of h, we get 0.2506 in. This means that under the current working assumptions, stress controls Feature D as well because it requires the larger dimension. HD is greater than or equal to 0.5362 in. 

<img width="485" height="1003" alt="1" src="https://github.com/user-attachments/assets/8c710148-4355-4c87-98e9-13c9e453a0f9" />

<img width="411" height="193" alt="IMG_3646" src="https://github.com/user-attachments/assets/01cc78f8-dac8-43fd-a104-68bc774b9fed" />



# Feature E Stress Analysis
Seen below is the free body diagram needed for feature E.
<img width="386" height="426" alt="1" src="https://github.com/user-attachments/assets/565908b1-0dcf-4475-9035-0fddfc67975d" />


I moved into my maximum M=PL, I solved for my M, and then continued into the required section modulus, much like the features earlier. I also did the rectangular cross section and found that hE must be greater than or equal to 0.500 in under the current assumptions. The photo below displays all of the calculations.

<img width="408" height="554" alt="1" src="https://github.com/user-attachments/assets/f77fbeef-966d-448c-ae51-edcc1d2e5fa9" />



Next, I moved into rearranging my deflection equation to solve for I, and then plugging in my values. I then found the required thickness from a rectangular cross-section, and found that my stiffness was approximately 0.218 in. In the photo below, the calculations are shown. The stress requirement is larger under this working model, so stress governs E. 

<img width="408" height="554" alt="1" src="https://github.com/user-attachments/assets/0327901b-8e41-4bc0-b61c-b1ff5ee366da" />

Attached below here is my multiview of my bracket.

<img width="398" height="515" alt="1" src="https://github.com/user-attachments/assets/bf54f497-21c2-49ba-a8ac-e1e56c4ee32f" />



## Decide
Before starting the calculations, I had to make a few design choices for the material, loading, and overall geometry of the bracket. For the applied load, I chose to use 750 lbf as my working load. This is within the required 500–800 lbf range, while also giving me a relatively high load to design around without automatically designing for the absolute maximum of 800 lbf. Since the bracket is symmetric, I also had to account for how the load would be distributed through the different features instead of assuming that every feature experiences the entire 750 lbf.

For the material, I chose ASTM A36 steel. One of the main reasons I chose A36 was because it gives me a good balance between strength and stiffness for this type of bracket. It also has a relatively high yield strength compared to the allowable stress after applying the safety factor, which gives me a reasonable starting point for the design. The modulus of elasticity of A36 steel is also useful for the stiffness calculations because the bracket has a fairly strict deflection limit of 0.005 in.

I chose to use a safety factor of 4 as required by the assignment. This means that instead of designing directly around the yield strength of the material, I reduced the allowable stress to account for uncertainty and give the design some additional margin. This was important because the theoretical calculations are based on simplified beam models, and the actual bracket geometry will not behave exactly like the idealized models.

For the overall geometry, I wanted to keep the bracket relatively simple and consistent with the shape shown in the assignment. I started with the main upper frame and then worked downward through the different features. I also kept the design symmetric because the applied load is symmetric. This makes the load distribution more reasonable and avoids creating unnecessary uneven loading on one side of the bracket.

Another reason I chose the geometry I did was because I wanted to be able to actually model it in SolidWorks without making the design unnecessarily complicated. Since I am still getting more comfortable with CAD, I wanted the design to be something I could build, modify, and dimension while still meeting the requirements of the assignment. As I went through the stress and stiffness calculations, I could then compare the theoretical minimum dimensions to what I had in CAD and make changes where necessary.


## Communicate

One of the biggest challenges I had during this project was figuring out how the different features of the bracket actually carried the applied load. At first, it was tempting to just use the 750 lbf everywhere, but because the bracket is symmetric, that would not accurately represent the load path. I had to stop and think about how the force travels through the bracket and how much of the load each individual feature actually sees.

Another challenge was translating the beam models from the assignment into the actual bracket geometry. The assignment gives us simplified models for the different features, such as treating A as a cantilever beam, B as an axially loaded bar, and C as a simply supported beam. The actual CAD model is more complicated than these individual models, so I had to decide which portion of the bracket each equation was representing.

CAD was also a challenge for me during this project. I am not the greatest with CAD, so there were times where I had to go back and figure out how a feature needed to be created before I could continue with the design. I had some difficulty determining which plane to use for certain features and how the different extrusions should connect together. I also had to make sure that the geometry I was creating in SolidWorks matched the physical idea I had in my calculations.

One thing that helped me was breaking the bracket down into individual features instead of trying to model the entire bracket at once. Once I started looking at A, B, C, D, and E separately, it became easier to understand what each feature was doing and what type of loading it was experiencing.

Another challenge was keeping track of the difference between a theoretical minimum dimension and an actual CAD dimension. The calculations give me the smallest dimension that satisfies a particular stress or stiffness requirement under my assumptions. That does not automatically mean that I should put that exact number into CAD. The actual geometry, connections, manufacturing considerations, and load path all have to be considered before choosing the final dimension.


One of the biggest things I learned from this project was that the load path is just as important as the equations being used. I can use the correct bending or deflection equation, but if I use the wrong force or length in that equation, the final answer will still be wrong. The symmetry of the bracket made this especially important because the full 750 lbf does not necessarily act on every individual feature.

I also learned more about the difference between strength and stiffness. Before doing these calculations, I mostly thought of the material strength as being the main thing that determined whether a component was large enough. Through this project, I learned that a component can be strong enough to avoid yielding but still deflect too much. This is why I had to perform both the stress and stiffness analyses for every feature.

For this design, I was able to compare the theoretical requirements from both analyses. In several of the features, the stress requirement was larger than the stiffness requirement. This means that, under my current working assumptions, bending stress is generally the governing requirement rather than deflection. However, I also learned that this conclusion depends on the assumptions used for the loading and geometry.

Here is my CAD model so far: https://drive.google.com/file/d/1QD-yOyKUIyKwOPdMeffn0mHfW_ekcAtt/view?usp=sharing


