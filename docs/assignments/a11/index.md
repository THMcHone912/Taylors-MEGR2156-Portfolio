# A11 – Motor Selection

## Objective
The objective of this assignment is to select a motor, design motor mounts, and select or design a coupler for the tensile tester. The assignment also involves designing a frame to support the crosshead and tensile load, analyzing and designing clamps, creating a complete CAD model, and developing a bill of materials with engineering costs. Additionally, the assignment requires documenting any mistakes made throughout the design process, recording the actual time spent completing the project from start to finish, and including a Lessons Learned section.

## Analyze
## Motor Selection and Attachments - Dina Chouffani and Taylor McHone
<img width="706" height="480" alt="image" src="https://github.com/user-attachments/assets/e792c324-317f-43a5-bbf5-cfc93185df96" />

<img width="1489" height="1056" alt="image" src="https://github.com/user-attachments/assets/ddadb702-3c57-47b5-b3bc-31a6e2457b2c" />

The selected motor is a McMaster-Carr #6470K71 DC gearmotor with a rated torque of 11.299 N·m and a rated speed of 30 RPM. The required torque, including a safety factor of 4, is 4.9256 N·m. Since the motor's rated torque exceeds the required torque, the motor satisfies the calculated torque requirement for the maximum 2 kN load.

<img width="1429" height="930" alt="image" src="https://github.com/user-attachments/assets/331db7f1-9459-451b-887f-117bac08b63d" />

The torque-speed curve shows the relationship between the motor's output torque and rotational speed at 90 V DC. The graph shows approximately 200 in·lbf of torque from 0 to 26 RPM, after which the torque decreases as speed increases. The required operating speed range of 0.4724–23.6217 RPM falls within this region.

<img width="700" height="967" alt="image" src="https://github.com/user-attachments/assets/dab0a57c-3b38-48d3-89b7-3e42488c3df5" />
I calculated the reaction force at each mounting bolt and used bearing stress to determine the minimum bracket thickness of 0.2194 mm. I selected a 4 mm thick 6061-T6 aluminum bracket to provide additional strength and stiffness.

<img width="676" height="970" alt="image" src="https://github.com/user-attachments/assets/12eafe00-b01c-48c8-bd2d-59081e5f87f3" />
I selected a 13 mm inner diameter to provide clearance for the 12.7 mm motor shaft. I calculated an allowable shear stress of 34.76 MPa and used torsional shear stress to determine a minimum outer diameter of 15.23 mm and a minimum wall thickness of 1.11 mm.

## Analyze and design a frame
<img width="682" height="873" alt="image" src="https://github.com/user-attachments/assets/8247864b-4f51-4c47-854a-143e6d18548a" />
<img width="1447" height="595" alt="image" src="https://github.com/user-attachments/assets/3ab65525-5e4d-499c-97ad-86a6a3950034" />

I analyzed the motor torque acting on the top frame and calculated a reaction force of 62.77 N at each end. Using a safety factor of 4, I determined a design force of 251.08 N and a bolt shear stress of 1.25 MPa. I selected the Grainger 5JRP7 inside-corner bracket with M8 class 4.6 steel bolts. The calculated bolt shear stress was below the allowable shear stress of 34.62 MPa, indicating that the bolts are sufficient for the assumed loading.

## Frame Analysis and Design - Nick Cornetta
Prior to modifying the previous design, I needed to evaluate the allowable stress acting on the frame from motor torque. To achieve this, I outlined the given parameters and variables, then sketched a free-body diagram (FBD) mapping out the combined forces on the structure. My assumptions specified that the assembly would use M5 screws sourced from Grainger. Based on a shear stress analysis, the acceptable stress limits were determined to range from 50.93 MPa to 278.07 MPa

<img width="3023" height="1192" alt="image" src="https://github.com/user-attachments/assets/62eea79a-bbc9-4263-b346-1e887d272b9e" />
## Frame FEA
Prior to initiating the simulation, I attached the wide corner brackets from Grainger to the frame, leaving out the individual screws because modeling each fastener was overly tedious. By applying a 2 kN load to the upper crossbar and setting fixed constraints on the lower legs, I executed a three-step mesh study.

Although the deflection values converged successfully, the stress levels failed to converge and vastly exceeded the maximum allowable threshold. The exceptionally high stress resulted from the missing fasteners, whereas the convergence difficulties were triggered by the bracket's sharp internal corners. We could resolve this by incorporating corner fillets or adding a central reinforcement web to the bracket. As another option we could weld the frame assembly together using a TIG welding procedure or a MIG setup equipped with an aluminum spool torch.

<img width="1078" height="705" alt="image" src="https://github.com/user-attachments/assets/fff384e7-d20b-4d0b-8e7e-b51b7cef1271" />
<img width="1051" height="712" alt="image" src="https://github.com/user-attachments/assets/199befac-101b-4233-8f23-55e3e02944f3" />
<img width="3021" height="2569" alt="image" src="https://github.com/user-attachments/assets/27a93662-d0aa-47ef-b417-3ab289f56e24" />

## Design Floating Bearing Mount
For the bearing mount design requiring an RC3 fit, I consulted the Machinery's Handbook. By referencing Table 8a on page 654, I established the known outer diameter and required tolerances. Afterward, I sketched a free-body diagram and applied torque analysis equations to calculate the appropriate inner wall thickness and diameter.
<img width="3021" height="1386" alt="image" src="https://github.com/user-attachments/assets/16a234f3-4aaf-4f9b-a3df-9e583dce0e08" />
<img width="567" height="558" alt="image" src="https://github.com/user-attachments/assets/dc59b2c3-c6e6-4744-a12c-6166b6cab911" />
<img width="703" height="511" alt="image" src="https://github.com/user-attachments/assets/80c7606c-d218-4164-9104-e7f6d7bb67db" />
Bill of Materials
Item #	Quantity	Name	Cost/Item	Cost	Purchase Link
804T48	1	40 Series T-Slot Aluminum Framing, 80 mm × 40 mm, 3 m Long	$245.87	$245.87	Grainger
95120A592	2	932 Bearing Bronze ACME Flange Nut, 3/8"-12 RH	$111.78	$223.56	McMaster-Carr
98935A817	2	Carbon Steel ACME Lead Screw, 3/8"-12 RH, 36" Long	$10.15	$20.30	McMaster-Carr
3333_0	2	NEMA 23 Stepper Motor	$72.00	$144.00	Phidgets
5JRU7	6	Wide Inside-Corner Bracket	$10.92	$65.52	Grainger
55MT26	24	Hammer Nut	$3.50	$21.00	Grainger
3613N15	2	Set Screw Shaft Coupling	$74.49	$148.98	McMaster-Carr
Total Cost	$869.23	
Labor Cost
Person	Hours Worked	Cost/Hour	Cost
All Members	16 hrs	$35/hr	$560
Total Cost
1,429.23

Final Design
Following the cost tabulation and finite element analysis (FEA), I finalized the design and constructed the tensile tester. To mitigate high stress concentrations and improve structural rigidity, I integrated wide brackets and hammer nuts at the corners, while also building additional support legs from leftover T-slot framing to ensure stability during loading.

<img width="531" height="864" alt="image" src="https://github.com/user-attachments/assets/d2a2fe24-4e85-40d4-83d3-0787dd193c6b" />

Lessons Learned
We learned how to select the right motor using torque and speed requirements from the leadscrew design and how to design a motor mount bracket to attach the motor to the tester frame while maintaining precise alignment with the leadscrew, accommodating service access for assembly and maintenance, and withstanding operational torque and reaction forces without excessive deflection. We also learned how to select and design a coupler using shear stress torsion analysis and how to select proper connectors for T-slot framing by analyzing the twist caused by the motors. Additionally, we learned how to use FEA to verify that the top of the frame provides enough strength to withstand the leadscrew load and torque. Finally, we learned how to design a mounting bearing that allows the end of the leadscrew to rotate using an RC3 fit class and attaches to the bottom of the frame.

This assignment took us approximately 7 hours to complete.

CAD Files
assemblymotor.zip

