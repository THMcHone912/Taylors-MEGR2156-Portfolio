# A7 – [FEA On Bracket]

## Objective
The objective of this assignment was to improve the bracket developed in the previous two assignments by applying the Finite Element Analysis, or FEA workflow in our CAD software. The goal was to develop a bracket that satisfies the required strength and stiffness constraints while minimizing unnecessary material and maintaining the required fit within the rigid T-beam.
The existing bracket design was used as the starting point. Static stress simulations were performed to evaluate the maximum von Mises stress, maximum displacement, factor of safety, and mass of the components. The mesh was refined iteratively until the results converged within the required 7% difference of the maximum of three convergence attempts was reached.
After validating the simulation results, the bracket geometry was modified to improve its performance. At least three design iterations were evaluated to determine how changes to the bracket's dimensions affected structural fit, behavior and mass.
The final objective was to use simulation results to justify the selected geometry, and also to teach us to document the entirety of the engineering design process. 

## Analyze
<img width="424" height="284" alt="Top " src="https://github.com/user-attachments/assets/45ddf439-0ba6-43dc-aae8-8d43d09d3cd8" />
The above photo is a look at the bracket from the top angle. 
For this assignment, the existing model, as pictured above, served as the baseline design. Rather than redesigning and going down a rabbit hole, I focused on identifying dimensions that could be modified to improve the structural performance and fit. 
The main considerations for these improvements were strength, weight, fit, stiffness, and simulation accuracy. Before modifying the geometry, the baseline simulation was established using the current design of the bracket. The study was ran via using the material without changing it, applying fixtures that represent how the bracket attaches to the rigid body, applying the specified load to the appropriate region, generating a mesh and solving the static study, and recording the maximum displacement, stress, element count, mass, and safety factor.
The % Difference can be calculated using the absolute value of Rfine-Rcoarse/Rfine (100). R is the result being compared from a particular mesh. 
For the initial run, the result using the safety factor of 3 was 16.5 MPa. For displacement, I got an answer of 0.30mm. After running and analyzing the first design, the maximum stress and displacement was in the hinges, and most of the stress was dissipated through the bottom part of the hinge and into the bottom plate of the bracket.
Design II changed the original geometry by strengthening the hinges and bottom plate of the bracket. Compared with Design I, its mass increased by 2%, while the maximum stress and displacement decreased by 4.5%. This comparison indicates that the geometry change improved the material efficiency without compromising the required structural performance the bracket needs to have.
Design III incorporated further modifications to the hinges and bottom plate. The mass was 50g, the maximum stress was 12.3 MPa, and the displacement was 0.25mm. Based on the safety factor, mesh convergence results, and displacement limit, Design III satisfied the stated requirements.
The mesh convergences were evaluated by comparing successive simulations. The final percentage difference was 2.2% for stress, and 3.7% for displacement. These results met the 7% convergence target. 


## Decide
This project forced us to use what we have learned up to this point about reading the stress graphs and figuring out how to strengthen our initial designs all while keeping within the specified requirements from the assignment. The project also helped us get more used to FEA and put it into practice a bit using something we had created. We also got to sharpen our Solidworks/CAD skills with this assignment too via the simulations.
The preferred design should meet the required safety factor and the displacement limit, all while minimizing unnecessary material because it drives costs up, The final selection for the bracket should be based on the converged simulation results, rather than chosen based on geometry or mass alone.
The final design selected was Design III. As state before, Design III had the least amount of stress, it had a little bit more displacement than Design II, but still within the required displacement range, and the mass was lighter than both Designs I and II, despite having more material and more reinforcement on the hinges and bottom plate. These results satisfied the structural requirements from the assignment. I focused on adding material during Design II, and then removing some from Design III after seeing the stress plot and calculating the displacement for Design II.  

## Communicate
This project helped me learn a lot in CAD. Slowly but surely I am learning and getting better with 3D modeling. It is a tedious process at first, but the more I work on it, the better it gets. I also like seeing the simulation aspect of CAD as well. Knowing how to do these simulations will help me see aero changes on the front and rear spoiler and diffuser on cars.
Some challenges was trying initially to figure out what exactly to change from Design I to Design II. It took me more time than I want to admit of how long it took before I ultimately decided to add some material onto the hinge and bottom plate of the bracket. Also trying to get the mesh and the convergence to pass and all was time-consuming until I learned how to do it correctly.
Overall, from start to finish with the bracket modeling and everything, this project took me around 4.5 hours to do.

Link to CAD file:https://drive.google.com/file/d/1QD-yOyKUIyKwOPdMeffn0mHfW_ekcAtt/view?usp=sharing
