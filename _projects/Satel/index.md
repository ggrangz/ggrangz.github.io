---
layout: post
title: Lightweight Satellite Wall-Panel Design and Optimization
description: >-
  Compared solid, isogrid, and honeycomb satellite wall panels using ANSYS,
  outsourced mechanical testing, parametric optimization, and CNC-oriented
  redesign to improve structural performance per unit mass.
skills:
  - ANSYS
  - SolidWorks
  - FEA
  - Structural Optimization
  - Modal Analysis
  - Mechanical Testing
  - CNC Manufacturing
  - Mastercam
  - GD&T
main-image: /satellite assembly manufactured.png
---

## Project Overview

Satellite structures experience static acceleration, vibration, shock, and multidirectional loading during transportation and launch. Their wall panels must provide sufficient strength and stiffness while contributing as little mass as possible.

Solid aluminum panels offer straightforward manufacturing and high stiffness, but they can contain material that contributes inefficiently to the principal load paths. Excessive material removal, however, can introduce local buckling, rib rippling, reduced panel stiffness, lower natural frequencies, and excessive deformation.

This project compared solid, isogrid, and honeycomb wall-panel architectures using finite element analysis and outsourced mechanical testing. The selected architecture was subsequently optimized, redesigned as a monolithic skinned isogrid, prepared for three-axis CNC machining, and integrated into a complete hexagonal satellite assembly.

---

## Project Objectives

- Compare solid, isogrid, and honeycomb wall-panel architectures
- Maximize mechanical performance per unit mass
- Maintain natural frequencies above the cited launcher requirement
- Identify local buckling behavior
- Remove unnecessary material without compromising structural integrity
- Avoid adhesive joints between the grid and outer skin
- Develop a panel suitable for three-axis CNC milling
- Integrate the selected panel into a complete satellite assembly
- Compare numerical predictions with outsourced mechanical test data

---

## Material Selection

The panels were modeled using **Aluminum 7075-T0**, selected for its low density, machinability, and applicability to lightweight aerospace structures.

| Property | Value |
|----------|-------|
| Material | Aluminum 7075-T0 |
| Yield strength | 103 MPa |
| Ultimate tensile strength | 228 MPa |
| Starting plate thickness | 6 mm |
| Final side-panel dimensions | 115 × 90 mm |

The T0 temper has substantially lower strength than heat-treated 7075-T6. Therefore, the temper designation was retained when reporting material properties and calculated structural margins.

---

## Initial Wall-Panel Designs

Five panel configurations were developed:

1. Solid aluminum panel
2. Isogrid panel with 2 mm ribs
3. Isogrid panel with 3 mm ribs
4. Honeycomb panel with 1 mm cell walls
5. Honeycomb panel with 1.5 mm cell walls

The isogrid panels used repeated triangular cells, while the honeycomb panels used hexagonal cells. Each lightweight configuration was evaluated against the solid panel to quantify the relationship between mass removal and mechanical performance.

| Test type | Specimen dimensions |
|-----------|---------------------|
| Compression | 54.39 × 32.75 × 6 mm |
| Three-point bending | 108.75 × 32.75 × 6 mm |

{% include image-gallery.html images="configs.jpg, fea configs.jpg" height="400" %}

---

## Finite Element Analysis

### Compression Simulation

Compression was modeled in ANSYS using explicit dynamic analysis. A prescribed displacement of **18 mm** was applied over a simulation duration of **0.0005 seconds**.

The analysis evaluated:

- Equivalent von Mises stress
- Load-carrying response
- Local buckling behavior
- Rib and cell-wall deformation
- Structural performance per unit mass

### Three-Point Bending Simulation

Static structural analysis was used to simulate three-point bending. The model included one upper loading cylinder and two lower support cylinders.

The numerical setup incorporated:

- A 2 mm cylinder radius
- A friction coefficient of 0.1 at the upper contact
- Frictionless contact at the lower supports
- Ten load steps over a nominal solution time of one second
- Equivalent stress and total-deformation evaluation

### Modal Analysis

Modal FEA was used to predict the natural frequencies and mode shapes of each panel. The analysis helped evaluate stiffness-to-mass performance and the potential for resonance with the launch environment.

The modal predictions were not experimentally validated and should therefore be interpreted as simulation results rather than measured frequencies.

{% include image-gallery.html images="Total deformation and specimen mode shapes of mode 1.jpg, natural frequency modes.png" height="350" %}

---

## Outsourced Mechanical Testing

Compression and three-point bending tests were conducted by an external testing facility. The experimental results were supplied for processing and comparison with the ANSYS predictions.

The outsourced testing included:

- Compression testing at a displacement rate of 2 mm/min
- Load-displacement measurements
- Three-point bending testing
- Specimen mass measurements
- Documentation of post-test deformation and failure behavior

The supplied data were processed to calculate strength-to-weight metrics, compare the five configurations, and assess whether the simulations captured the observed structural trends.

{% include image-gallery.html images="experimental testing results.jpg" height="400" %}

---

## Initial Design Results

| Configuration | Specimen mass | FEA compression result | Experimental compression result | Experimental result/mass | FEA bending result | FEA bending result/mass |
|---------------|--------------:|-----------------------:|--------------------------------:|-------------------------:|-------------------:|------------------------:|
| Solid | 30.060 g | 738.22 MPa | 782.99 MPa | 26.05 MPa/g | 1,667.1 MPa | 27.79 MPa/g |
| 2 mm isogrid | 21.750 g | 728.01 MPa | 691.03 MPa | 31.77 MPa/g | 2,136.5 MPa | 49.69 MPa/g |
| 3 mm isogrid | 21.760 g | 720.88 MPa | 679.13 MPa | 31.21 MPa/g | 2,053.6 MPa | 47.24 MPa/g |
| 1 mm honeycomb | 17.998 g | 354.83 MPa | 321.47 MPa | 17.86 MPa/g | 1,183.3 MPa | 34.85 MPa/g |
| 1.5 mm honeycomb | 18.745 g | 496.66 MPa | 576.89 MPa | 30.78 MPa/g | 1,615.3 MPa | 44.07 MPa/g |

The solid panel produced the highest experimental compression result, but its greater mass reduced its mechanical efficiency.

The **2 mm isogrid** achieved the highest experimental compression result per unit mass at **31.77 MPa/g** and the highest simulated bending result per unit mass at **49.69 MPa/g**. It was therefore selected as the preferred initial lightweight architecture.

---

## FEA and Experimental Correlation

| Configuration | FEA result | Experimental result | Difference relative to experiment |
|---------------|-----------:|--------------------:|----------------------------------:|
| Solid | 738.22 MPa | 782.99 MPa | −5.7% |
| 2 mm isogrid | 728.01 MPa | 691.03 MPa | +5.4% |
| 3 mm isogrid | 720.88 MPa | 679.13 MPa | +6.1% |
| 1 mm honeycomb | 354.83 MPa | 321.47 MPa | +10.4% |
| 1.5 mm honeycomb | 496.66 MPa | 576.89 MPa | −13.9% |

The differences between the numerical and experimental compression results ranged from approximately **5.4% to 13.9%**. The models captured the overall performance trends, although the 1.5 mm honeycomb produced the greatest discrepancy.

Potential sources of disagreement included:

- Manufacturing tolerances
- Initial geometric imperfections
- Material-property variation
- Idealized contact and friction assumptions
- Sensitivity of thin ribs and cell walls to buckling
- Simplification of the numerical material model
- Differences between ideal CAD geometry and manufactured specimens

Physical testing showed local buckling in the grid specimens, consistent with the slender ribs and cell walls represented in the designs.

---

## Panel-Level Modal Results

| Configuration | First simulated natural frequency |
|---------------|----------------------------------:|
| Solid | 420.43 Hz |
| 2 mm isogrid | 338.95 Hz |
| 3 mm isogrid | 332.27 Hz |
| 1 mm honeycomb | 189.03 Hz |
| 1.5 mm honeycomb | 249.94 Hz |

The solid panel produced the highest predicted first natural frequency. Among the lightweight architectures, the 2 mm isogrid produced the highest predicted first natural frequency.

Reducing the isogrid rib width from 3 mm to 2 mm increased the predicted frequency from **332.27 to 338.95 Hz**. Increasing the honeycomb wall thickness from 1 mm to 1.5 mm increased it from **189.03 to 249.94 Hz**.

These modal results were not experimentally validated.

---

## Isogrid Parametric Optimization

After selecting the 2 mm rib width, the triangular cell length was varied between **12, 18, and 24 mm** for a 115 × 90 × 6 mm panel.

| Configuration | Panel mass | Compression result/mass | Bending result/mass | First simulated natural frequency |
|---------------|-----------:|------------------------:|--------------------:|----------------------------------:|
| 12 mm open isogrid | 102.020 g | 6.71 MPa/g | 19.37 MPa/g | 1,241.5 Hz |
| 18 mm open isogrid | 91.057 g | 7.82 MPa/g | 27.54 MPa/g | 1,131.5 Hz |
| 24 mm open isogrid | 66.379 g | 10.87 MPa/g | 45.47 MPa/g | 1,031.1 Hz |
| 24 mm isogrid with integral skin | 91.341 g | 7.94 MPa/g | 29.20 MPa/g | 1,308.7 Hz |

{% include image-gallery.html images="12_18_24_compression_bending_testing.jpg, triangular configs.png" height="350" %}

Increasing the open-isogrid cell length from 12 mm to 24 mm reduced the panel mass from **102.020 to 66.379 g**, representing a **34.9% reduction**.

The 24 mm open isogrid produced the highest reported compression and bending performance per unit mass. However, its wider rib spacing also produced the lowest predicted frequency among the three open-isogrid designs.

---

## Skinned Isogrid Redesign

To increase stiffness and improve manufacturability, the selected panel was redesigned with a **1 mm integral outer skin**.

The final panel incorporated:

- 2 mm rib width
- 24 mm triangular cell length
- 0.75 mm internal corner fillets
- 1 mm integral outer skin
- 115 × 90 mm external dimensions
- Four 6 mm mounting holes
- Monolithic CNC-machined construction

Compared with the open 24 mm isogrid, the integral skin increased mass from **66.379 to 91.341 g** but raised the predicted first natural frequency from **1,031.1 to 1,308.7 Hz**, an improvement of **26.9%**.

The monolithic construction also eliminated the adhesive interface that would otherwise be required to attach a separate face sheet to the grid.

{% include image-gallery.html images="von mises 2 mm skinned.png" height="400" %}

---

## Satellite Assembly

The selected wall-panel architecture was incorporated into a hexagonal satellite structure consisting of:

- Six skinned isogrid side panels
- One top plate
- One bottom plate
- Six 120° brackets between adjacent side panels
- Twelve 90° brackets connecting the side panels to the end plates
- Rivet nuts and flat-head fasteners

The top and bottom plates had a reported hexagonal diagonal of **166.14 mm**, a thickness of **6 mm**, and six **4 mm countersunk through-holes**.

{% include image-gallery.html images="satellite assembly.png, satellite assembly manufactured.png" height="400" %}

---

## Assembly-Level Static Analysis

The satellite assembly was constrained at the top and bottom rail interfaces and subjected to simultaneous quasi-static accelerations of **11g in the X, Y, and Z directions**.

| Result | Predicted value |
|--------|----------------:|
| Maximum von Mises stress | 89.431 MPa |
| Maximum total deformation | 0.0134 mm |
| Material yield strength | 103 MPa |
| Calculated yield factor of safety | 1.15 |

{% include image-gallery.html images="von mises satellite assembly.png" height="400" %}

The simulated maximum stress remained below the assigned material yield strength. However, the calculated factor of safety of **1.15 represents a limited structural margin** and should not be described as substantial without assembly-level physical testing.

---

## Assembly-Level Modal Analysis

The simulated first natural frequency of the assembled satellite was **300.85 Hz**, exceeding the cited minimum launcher requirement of **50 Hz**.

This result indicates predicted frequency separation from the stated minimum requirement. It does not guarantee avoidance of resonance without comparison against the launcher excitation spectrum, experimental mode shapes, damping, and measured frequency-response data.

{% include image-gallery.html images="natural frequency modes for satellite.png" height="400" %}

---

## Manufacturing Approach

The skinned isogrid panel was designed for three-axis CNC machining from 7075-T0 aluminum plate. Because its pockets are accessible from one side and contain no undercuts, a three-axis milling machine is sufficient.

A practical manufacturing sequence would include:

1. Face the 6 mm aluminum plate and establish datum surfaces.
2. Secure the plate to a fixture or sacrificial backing plate.
3. Rough-machine the triangular pockets while retaining the 1 mm skin.
4. Finish the 2 mm ribs and 0.75 mm internal corner fillets.
5. Drill or ream the mounting holes.
6. Machine countersinks and attachment interfaces.
7. Deburr the ribs, pockets, and hole edges.
8. Inspect rib width, skin thickness, hole position, flatness, and external dimensions.
9. Apply the required corrosion-protection treatment.

Mastercam was used to support the CAD/CAM workflow and generate the required CNC toolpaths and G-code.

---

## Key Results

- Compared five solid, isogrid, and honeycomb panel configurations
- Processed outsourced compression and three-point-bending test data
- Correlated compression FEA results with experimental data to within approximately **5.4–13.9%**
- Identified the 2 mm isogrid as the strongest initial lightweight configuration per unit mass
- Achieved a **34.9% mass reduction** by increasing open-isogrid cell length from 12 mm to 24 mm
- Increased the predicted first natural frequency of the 24 mm panel by **26.9%** by adding an integral skin
- Eliminated the need for a separate adhesive-bonded face sheet
- Developed a monolithic panel suitable for three-axis CNC milling
- Predicted a maximum assembly stress of **89.431 MPa** under simultaneous 11g acceleration
- Limited predicted assembly deformation to **0.0134 mm**
- Achieved a predicted assembly first natural frequency of **300.85 Hz**

---

## Engineering Insights

The project demonstrated that the lightest panel is not automatically the best design. Increasing cell spacing improved performance per unit mass but reduced modal stiffness, requiring a compromise between weight, mechanical efficiency, and natural frequency.

The 2 mm isogrid outperformed the other lightweight configurations because its triangular load paths provided efficient structural reinforcement without the mass of a solid panel.

The integral skin increased panel mass but improved predicted modal performance and eliminated an adhesive interface. This produced a more manufacturable and structurally integrated design.

Correlation with physical compression data showed that simplified FEA models can reproduce overall design trends while still differing from experiments because of manufacturing imperfections, contact assumptions, material variability, and buckling sensitivity.

---

## Future Validation and Improvements

- Conduct impact-hammer modal testing
- Measure frequency-response functions using accelerometers
- Compare measured and predicted natural frequencies and mode shapes
- Perform vibration and shock testing
- Incorporate experimentally measured damping into the ANSYS model
- Increase the static factor of safety through local reinforcement or material changes
- Conduct assembly-level static load testing
- Perform dimensional inspection of CNC-machined components
- Investigate nonlinear material behavior and geometric imperfections
- Compare simulation results with launcher-specific load spectra
