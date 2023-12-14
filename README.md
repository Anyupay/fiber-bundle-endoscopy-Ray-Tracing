# Optical Path Design for Fiber Bundle Endoscopy using Zemax

## Project Overview
This project focused on designing the objective part of a fiber bundle endoscope using Zemax for optical path tracing. The design process involved extensive literature review, with a particular paper providing the necessary parameters for the design.

## Key Steps in Design
- **Setting Aperture and Fields:** Correct aperture and field settings were established as per the requirements.
- **Lens Selection:** Based on the information in the chosen paper, three types of lenses were selected: a negative lens, a positive lens, and a cemented doublet. All lenses used were spherical.
- **Adjusting Parameters:** Parameters such as Radius, Thickness, and Semi-Diameter were set within reasonable limits. The correct grating was also established.
- **Material Selection:** Despite the reference paper's recommendation, the DZF94 glass was unavailable (possibly discontinued). Therefore, an alternative material was selected, which necessitated changes in other material pairings to approach the image quality described in the paper. Zemax's automatic material replacement feature was utilized.
- **Optimization Operations:** The objective was continually optimized to approximate the state and results presented in the paper.

## Optimization Operands Used
- **EFFL:** This operand measures the focal length of the system in lens units. The wavelength used for this measurement is defined by the 'Wave' parameter in Zemax.
- **DIMX:** This represents the upper limit of the absolute value of distortion. It is used to constrain the amount of distortion present in the optical system to ensure it remains within acceptable limits.
- **TTHI:** The sum of the thicknesses of all the surfaces between Surf1 and Surf2. It provides a measure of the physical length of the optical path within a specified portion of the system.
- **OPLT:** This operand is used to ensure that the value of an operand, defined by Op#, remains less than a target value specified by this OPLT operand. It is useful for setting upper bounds on certain parameters during optimization.
- **RAID:** This operand measures the angle of incidence, which is the angle between the incoming ray and the normal to the surface at the point of incidence, for a given surface (surf) and wavelength (Wave). This is crucial for controlling and limiting the angles at which light can enter the system.

## Results
- The spot diagram and MTF curve closely matched the results in the reference paper.
- The layout showed slight differences, likely due to the change in materials.
- The MTF curve was superior to that in the reference paper.
- Overall, the project successfully replicated the design with some improvements.

## Conclusion
This work represents a replication and enhancement of a fiber bundle endoscope's objective design using Zemax, demonstrating a successful application of optical design principles and software capabilities.

## Location Contents
- **Zemax Files**
	- `.ZMX` and `.ZDA` files: These files contain the detailed Zemax designs.
- **Final Design Outputs**
	- Layout diagrams
	- Spot diagrams
	- MTF curve plots
- **Paper**
	- Chinese and English version
