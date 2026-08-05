---
layout: post
title: FEA and Topology Optimization of a Bell Crank
description: >-
  Reduced the mass of a 90-degree bell crank by 55.8% using mesh-converged FEA,
  topology optimization, CAD reconstruction, and three-axis CNC manufacturing.
skills:
  - SolidWorks
  - Finite Element Analysis
  - Topology Optimization
  - CAD Reconstruction
  - Design for Manufacturing
  - Mastercam
  - Haas CNC Milling
main-image: /images.jpg
---

## Project Overview

Redesigned a **120 × 115 × 10 mm, 90-degree bell crank** to reduce weight while preserving its mounting interfaces and structural load paths. The central pivot was constrained, and perpendicular **2,000 N loads** were applied at the two end holes.

Topology optimization identified low-stress material for removal while preserving the pivot bore and load-application holes. The resulting mesh was reconstructed as a manufacturable CAD model and reanalyzed under the original loading conditions.

The final design reduced mass from **384.56 g to 170.00 g**, a **55.8% reduction**, while maintaining a reported static factor of safety above 2.6.

---

## Key Accomplishments

Performed a mesh-convergence study and established a converged baseline stress of **97.12 MPa** using 32,006 elements and a 2.5 mm maximum element size.

Used SolidWorks topology optimization to remove material from low-stress regions while preserving the central pivot, mounting holes, and primary load paths.

Reconstructed the topology result as clean CAD geometry, remeshed it, and compared it with the baseline using identical loads, constraints, material properties, and evaluation criteria.

Reduced component mass by **214.56 g** while limiting the increase in peak stress to **8.28 MPa** and displacement to **0.003 mm**.

Prepared the optimized geometry through a CAD/CAM workflow and manufactured it using a **three-axis Haas CNC mill**.

---

## Mesh Convergence

| Iteration | Elements | Degrees of freedom | Maximum element size | Peak von Mises stress |
|----------:|---------:|-------------------:|---------------------:|-----------------------:|
| 1 | 7,728 | 37,704 | 10 mm | 50.00 MPa |
| 2 | 8,624 | 43,864 | 7 mm | 80.00 MPa |
| 3 | 9,887 | 48,021 | 5 mm | 90.63 MPa |
| 4 | 22,264 | 103,896 | 3 mm | 96.93 MPa |
| 5 | 32,006 | 146,655 | 2.5 mm | 97.12 MPa |

The stress changed by approximately **0.2%** between the final two mesh levels, indicating adequate convergence for the reported comparison.

---

## Results

| Performance metric | Original design | Optimized design | Change |
|--------------------|----------------:|-----------------:|-------:|
| Mass | 384.56 g | 170.00 g | 55.8% reduction |
| Peak von Mises stress | 97.12 MPa | 105.40 MPa | 8.5% increase |
| Maximum displacement | 0.034 mm | 0.037 mm | 8.8% increase |

The optimized design achieved substantial weight reduction with comparatively small increases in predicted stress and displacement.

{% include image-gallery.html images="fea1.webp, fea2.webp, fea3.webp" height="350" %}

---

## Manufacturing

The redesigned bell crank was prepared for three-axis CNC machining by converting the topology result into smooth, accessible features without undercuts.

The manufacturing workflow included:

- CAD reconstruction in SolidWorks
- Toolpath planning using Mastercam
- Workholding and datum selection
- Pocket and contour machining
- Hole machining
- Deburring and dimensional inspection
- Fabrication using a three-axis Haas CNC mill

{% include image-gallery.html images="irl manufactured.webp" height="400" %}

---

## Future Improvements

- Verify the reported factor-of-safety and strain results
- Apply bearing-contact and pin-loading conditions
- Perform fatigue analysis under cyclic and reversing loads
- Conduct physical load testing of the machined component
- Compare measured strain and displacement with FEA predictions
- Evaluate additional manufacturing-constrained topology designs
