---
layout: post
title: FEA and Structural Optimization of an Aviation Bracket
description: >-
  Redesigned an aviation mounting bracket using multiaxial finite element
  analysis and topology optimization, reducing reported mass by 84.8% while
  maintaining acceptable stress, deformation, and static yield margins.
skills:
  - ANSYS 
  - SolidWorks
  - FEA
  - Topology Optimization
  - Structural Design
  - DFM
  - CNC Machining
main-image: /table.webp
---

## Project Overview

Aviation mounting brackets transfer loads between structural and mechanical subsystems while contributing as little mass as possible to the aircraft. Traditional bracket geometries can contain material in regions that contribute minimally to the primary load paths, resulting in unnecessary weight and inefficient material utilization.

This project focused on redesigning an aviation mounting bracket to improve its strength-to-weight ratio using finite element analysis and topology optimization. The bracket was evaluated under vertical, horizontal, inclined, and torsional loading to identify critical stress regions and determine how material could be redistributed more efficiently.

Topology-optimization results were reconstructed into three manufacturable CAD configurations. The designs were compared using stress, strain, deformation, mass, static factor of safety, multiaxial performance, and manufacturability.

**Design 3** was selected as the preferred configuration because it provided the most balanced structural response across the four evaluated load cases while reducing the reported component mass from **10,353.79 g to 1,569.11 g**, an **84.8% reduction**.

---

## Engineering Challenge

The optimization process was developed around the following requirements:

- Identify stress concentrations around mounting holes, fillets, and load-transfer regions
- Remove material from low-stress regions without compromising structural integrity
- Evaluate the bracket under multiple loading directions
- Maintain predicted stresses below the assigned material yield strength
- Limit deformation to preserve alignment between connected components
- Retain mounting holes and functional assembly interfaces
- Convert topology results into smooth and manufacturable CAD geometry
- Develop a configuration compatible with CNC machining or metal additive manufacturing

{% include image-gallery.html images="OG_CAD.webp, topology.webp" height="400" %}
---

## Material Evaluation

Aluminum 2024-T3, Ti-6Al-4V, stainless steel, and mild steel were considered based on strength, density, corrosion resistance, cost, and manufacturing requirements.

A high-strength aluminum alloy was selected for the structural analysis because of its favorable strength-to-weight ratio and widespread use in lightweight aerospace structures.

<!-- VERIFY BEFORE PUBLISHING:
The source data identify this material as Aluminum 7076-T6 with a density of
2,180 kg/m^3. Confirm whether the intended material is Aluminum 7075-T6 and
verify the density used in the FEA model before reporting absolute mass values.
-->

| Assigned property | Reported value |
|-------------------|---------------:|
| Material | High-strength aluminum alloy |
| Young’s modulus | 71.7 GPa |
| Poisson’s ratio | 0.33 |
| Density | 2,180 kg/m³ |
| Yield strength | 502 MPa |

The reported material values must remain consistent with the material card used in the simulation. Changing the assigned density would alter the absolute mass values, although the percentage reduction would remain unchanged if the same density were applied to every design.

---

## Baseline Finite Element Analysis

Static FEA was performed to establish baseline structural performance and identify material that contributed minimally to the bracket’s load-bearing behavior.

The analysis evaluated:

- Equivalent von Mises stress
- Equivalent elastic strain
- Resultant displacement
- Static yield factor of safety
- Component mass
- Principal load paths
- Stress concentrations around mounting interfaces

Mounting holes and attachment surfaces were preserved throughout the optimization to maintain assembly compatibility.

---

## Loading Conditions

Four load cases were developed to represent different operating directions and load-transfer modes.

| Load case | Applied loading | Dominant structural response |
|-----------|-----------------|------------------------------|
| Vertical | 3,500 N in the Y-direction | Bending |
| Horizontal | 3,700 N in the X-direction | Bending and shear |
| Inclined | 2,500 N in X and 3,000 N in Y | Multiaxial bending, shear, and axial loading |
| Torsional | Applied twisting load | Shear and angular deformation |

Applying several load cases prevented the design from being optimized for only one favorable loading direction.

---

## Topology Optimization and CAD Reconstruction

Topology optimization was used to identify regions that contributed minimally to the bracket’s structural performance. Mounting holes, load-application surfaces, and other functional interfaces were designated as preserved regions.

The optimization results were reconstructed into three manufacturable CAD configurations. Each design used different:

- Material-removal patterns
- Wall and rib thicknesses
- Fillet radii
- Load-path geometries
- Transition profiles
- Manufacturing strategies

Irregular topology surfaces were not treated as final production geometry. They were converted into smooth CAD features before structural reanalysis.

The three redesigned brackets were then evaluated using the same nominal material properties, constraints, loading conditions, and output metrics.

{% include image-gallery.html images="CAD1.webp, CAD2.webp, CAD3.webp" height="350" %}
---

## Mass Comparison

| Configuration | Reported mass | Reduction from original |
|---------------|--------------:|------------------------:|
| Original bracket | 10,353.79 g | — |
| Design 1 | 1,695.56 g | 83.6% |
| Design 2 | 1,542.17 g | 85.1% |
| Design 3 | 1,569.11 g | 84.8% |

Design 2 was the lightest configuration, but minimum mass alone was not used to select the final design. Structural response and consistency across all four load cases were also considered.

---

## Structural Analysis Results

{% include image-gallery.html images="FEA1.webp, FEA2.webp, FEA3.webp" height="350" %}

### Vertical Loading

A vertical load of **3,500 N** was applied in the Y-direction.

| Parameter | Design 1 | Design 2 | Design 3 |
|-----------|---------:|---------:|---------:|
| Maximum stress | 52.3 MPa | 68.5 MPa | 55.1 MPa |
| Maximum strain | 0.00073 | 0.00096 | 0.00077 |
| Maximum deformation | 0.042 mm | 0.058 mm | 0.045 mm |
| Estimated yield factor of safety | 9.60 | 7.33 | 9.11 |

Design 1 produced the lowest stress and deformation under vertical loading. Design 3 nevertheless remained well below the assigned material yield strength.

### Horizontal Loading

A horizontal load of **3,700 N** was applied in the X-direction.

| Parameter | Design 1 | Design 2 | Design 3 |
|-----------|---------:|---------:|---------:|
| Maximum stress | 118.6 MPa | 72.4 MPa | 64.8 MPa |
| Maximum strain | 0.00165 | 0.00101 | 0.00090 |
| Maximum deformation | 0.061 mm | 0.039 mm | 0.034 mm |
| Estimated yield factor of safety | 4.23 | 6.93 | 7.75 |

Design 3 produced the lowest stress and deformation under horizontal loading. Its maximum stress was approximately **45.4% lower than Design 1**.

### Inclined Loading

The inclined condition combined **2,500 N in X** with **3,000 N in Y**.

| Parameter | Design 1 | Design 2 | Design 3 |
|-----------|---------:|---------:|---------:|
| Maximum stress | 105.2 MPa | 81.6 MPa | 70.3 MPa |
| Maximum strain | 0.00147 | 0.00114 | 0.00098 |
| Maximum deformation | 0.054 mm | 0.037 mm | 0.033 mm |
| Estimated yield factor of safety | 4.77 | 6.15 | 7.14 |

The inclined load was the governing condition for Design 3, producing a maximum stress of **70.3 MPa**. This was approximately **14% of the assigned 502 MPa yield strength**.

### Torsional Loading

| Parameter | Design 1 | Design 2 | Design 3 |
|-----------|---------:|---------:|---------:|
| Maximum stress | 79.5 MPa | 48.2 MPa | 52.6 MPa |
| Maximum strain | 0.00111 | 0.00067 | 0.00073 |
| Maximum deformation | 0.018 mm | 0.011 mm | 0.013 mm |
| Estimated yield factor of safety | 6.31 | 10.41 | 9.54 |

Design 2 produced the best torsional response. Design 3 produced slightly greater stress and deformation but maintained a substantial predicted static margin against yielding.

---

## Design Selection

Design 3 was selected as the preferred configuration because it provided the strongest overall compromise across mass, stress, deformation, static margin, and multidirectional loading.

Its principal advantages included:

- An **84.8% reported mass reduction**
- Lowest stress and deformation under horizontal loading
- Lowest stress and deformation under inclined loading
- Minimum estimated yield factor of safety of **7.14**
- More consistent performance across the four evaluated load directions
- Geometry that could be reconstructed for CNC machining or metal additive manufacturing

Design 3 was not the best configuration under every individual condition. Design 1 performed better under vertical loading, while Design 2 was lighter and performed better under torsion. Design 3 was selected because it provided the most balanced response for a multiaxial operating environment.

---

## Fatigue Considerations

A static yield assessment does not independently establish fatigue life. Aluminum alloys generally do not exhibit a true endurance limit, so maintaining maximum stress below yield does not guarantee infinite life under cyclic loading.

The governing static stress of approximately **70.3 MPa** was low relative to the assigned yield strength, but a defensible fatigue-life calculation would also require:

- Alternating stress
- Mean stress
- A verified S-N curve for the exact alloy and temper
- Surface-condition and size correction factors
- Stress-concentration or fatigue-notch factors
- Loading spectrum and cycle count
- Environmental and corrosion effects
- Mean-stress correction using the Goodman or another appropriate relation

A fatigue life of \(10^6\) to \(10^7\) cycles should therefore be presented as a preliminary analytical estimate unless supported by validated material data and physical fatigue testing.

---

## Manufacturing Considerations

The topology-optimized geometry was reviewed for compatibility with CNC machining and metal additive manufacturing.

{% include image-gallery.html images="drawing.webp" height="400" %}

Manufacturing-oriented redesign included:

- Smoothing irregular topology-generated boundaries
- Adding fillets around stress-sensitive transitions
- Retaining mounting holes and functional interfaces
- Avoiding unnecessarily thin unsupported features
- Providing tool access for CNC-machined surfaces
- Maintaining practical wall and rib thicknesses
- Identifying surfaces requiring post-processing
- Preserving dimensional control at attachment locations

A CNC-machined version would require accessible features, suitable internal radii, and sufficient tool clearance. A metal-additively manufactured version could retain more organic load paths but would require support planning, build-orientation studies, post-machining of interfaces, and inspection for porosity and distortion.

---

## Key Results

- Evaluated the bracket under vertical, horizontal, inclined, and torsional loading
- Reconstructed topology results into three manufacturable CAD configurations
- Reduced reported component mass from **10,353.79 g to 1,569.11 g**
- Achieved a reported mass reduction of **84.8%** with Design 3
- Limited Design 3 maximum stress to **70.3 MPa** under its governing inclined load
- Maintained an estimated minimum static yield factor of safety of **7.14**
- Reduced horizontal-load stress by approximately **45.4%** relative to Design 1
- Preserved mounting holes and functional interfaces throughout optimization
- Developed geometry suitable for further CNC or metal-AM process planning

---

## Engineering Insights

The project demonstrated that the lightest design is not necessarily the best engineering solution. Design 2 had the lowest mass and strongest torsional response, but Design 3 provided more consistent performance across the complete multiaxial loading environment.

Topology optimization was used as a material-distribution guide rather than as the final manufacturing geometry. The raw optimization result required CAD reconstruction, smoothing, filleting, interface preservation, and structural reanalysis before it could be considered manufacturable.

The analysis also reinforced the distinction between static strength and fatigue durability. A high static factor of safety does not establish long-term performance under repeated aircraft loading.

---

## Future Validation

- Verify the exact aluminum alloy, temper, density, and strength values
- Conduct a mesh-convergence study for each critical load case
- Perform sensitivity studies on constraints and load-distribution assumptions
- Apply bearing loads instead of idealized point or surface forces where appropriate
- Evaluate bolt preload and contact behavior at mounting interfaces
- Perform fatigue analysis using a verified material S-N curve
- Manufacture the selected design and conduct static load testing
- Compare measured strains and displacement with FEA predictions
- Inspect the manufactured component using dimensional metrology
- Conduct dye-penetrant or other nondestructive inspection where appropriate
