---
layout: post
title: Structural and Fatigue Analysis of a Perforated Plate
description: >-
  Evaluated yielding, fracture, fatigue, and crack-growth limits of a perforated
  plate using ANSYS and analytical failure criteria, then improved allowable
  stress by optimizing hole spacing.
skills:
  - ANSYS
  - Finite Element Analysis
  - Structural Mechanics
  - Fracture Mechanics
  - Fatigue Analysis
  - Tresca Criterion
  - Goodman Criterion
  - Paris Law
  - Parametric Optimization
main-image: /perforated_plate_wallpaper.jpg
---

## Project Overview

Evaluated the structural integrity and fatigue performance of a **250 × 250 mm perforated plate** under biaxial tensile loading.

I developed an ANSYS finite element model to characterize stress concentrations around five circular holes and determine the maximum allowable applied stress. The plate was assessed against four failure modes:

- Tresca yielding
- Static fracture using Linear Elastic Fracture Mechanics
- Fatigue without a crack using the Goodman criterion
- Fatigue crack growth using Paris Law

A parametric geometry study was then performed to improve structural durability without changing the plate material or external dimensions.

{% include image-gallery.html images="dimensions.webp" height="400" %}

---

## Finite Element Model

The plate contained one central hole and four surrounding holes. A biaxial tensile load was applied to represent multidirectional in-plane loading.

ANSYS was used to evaluate:

- Maximum shear stress
- Maximum principal stress
- Stress concentration around the holes
- Critical load-transfer regions
- Changes produced by increasing hole spacing

A nominal **1 MPa trial load** was used for the linear-elastic analysis. The resulting stresses were scaled analytically to determine the allowable applied stress for each failure criterion.

---

## Failure Analysis

### Tresca Yielding

Maximum shear stress from ANSYS was compared with the allowable shear stress of the material. The original design produced an allowable applied stress of **121.83 MPa**.

### Static Fracture

Maximum principal stress was used to calculate the Mode I stress-intensity factor. Using a **0.6 mm initial crack**, fracture toughness, and a factor of safety of 1.5, the original static-fracture limit was calculated as **139.90 MPa**.

### Fatigue Without a Crack

The Goodman criterion was used to account for alternating and mean stress. The original design produced an allowable fatigue stress of **71.09 MPa**.

### Fatigue With a Crack

Paris Law was used to evaluate crack propagation from an initial **0.6 mm crack** for a target life of **10⁶ cycles**.

Fatigue crack growth governed the original design, limiting the allowable applied stress to **17.48 MPa**.

{% include image-gallery.html images="fea-analysis.webp" height="400" %}

---

## Geometry Optimization

The original radial hole-location dimension of **50 mm** was increased to **91.92 mm**. This repositioned the surrounding holes to create more uniform spacing between the holes and plate edges.

The same material properties, boundary conditions, and failure criteria were applied to both configurations to provide a controlled comparison.

---

## Results

| Failure mode | Original allowable stress | Redesigned allowable stress | Improvement |
|--------------|--------------------------:|----------------------------:|------------:|
| Tresca yielding | 121.83 MPa | 133.96 MPa | 9.8% |
| Static fracture | 139.90 MPa | 153.84 MPa | 10.0% |
| Fatigue without crack | 71.09 MPa | 78.17 MPa | 9.9% |
| Fatigue with crack | 17.48 MPa | 18.88 MPa | 8.1% |

The redesign reduced the maximum FEA stress-concentration factor from approximately **3.529 to 3.210**, a reduction of about **9%**.

Fatigue crack growth remained the governing failure mode, but its allowable applied stress increased from **17.48 to 18.88 MPa**.

---

## Key Accomplishments

Developed an ANSYS model of a perforated plate under biaxial tensile loading and identified critical stress concentrations around five circular holes.

Evaluated four governing failure modes using the Tresca criterion, Linear Elastic Fracture Mechanics, the Goodman fatigue relation, and Paris Law crack-growth analysis.

Determined that fatigue propagation from a **0.6 mm pre-existing crack** governed the design for a target life of **10⁶ cycles**.

Increased the radial hole-location dimension from **50 to 91.92 mm**, reducing the maximum stress concentration by approximately **9%**.

Improved allowable applied stress by **8.1–10.0%** across all four failure modes without changing the plate material or external dimensions.

---

## Engineering Insights

The analysis demonstrated that meeting static yield requirements does not guarantee adequate fatigue durability. Although the yielding and static-fracture limits exceeded 120 MPa, the cracked-fatigue condition limited the original allowable stress to only **17.48 MPa**.

Redistributing geometric discontinuities reduced stress concentration without increasing component size or changing material. However, a complete design validation would require mesh-convergence studies, experimentally verified fatigue properties, and physical cyclic testing.

---

## Future Improvements

- Perform mesh-convergence analysis around the hole and crack-tip regions
- Model crack-tip behavior using refined fracture-mechanics elements
- Evaluate additional hole arrangements and diameters
- Apply experimentally verified material fatigue properties
- Conduct physical biaxial and cyclic testing
- Compare predicted and measured crack-growth rates
