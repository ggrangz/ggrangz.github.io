---
layout: post
title: Lightweight UAV Chassis Design and Optimization
description: >-
  Designed and optimized a parametric UAV chassis in Fusion 360, reducing mass
  by 15% while maintaining structural-integrity and manufacturability requirements.
skills:
  - Fusion 360
  - Parametric CAD
  - Finite Element Analysis
  - Structural Optimization
  - Design for Manufacturing
  - Engineering Drawings
  - Bill of Materials
main-image: /highlight_1784475403273.webp
---

## Project Overview

Designed and optimized a lightweight UAV chassis that balanced structural strength, stiffness, mass, and manufacturability for aerial operation.

The project addressed the challenge of reducing structural weight without weakening critical load paths or compromising the chassis’s ability to support propulsion components, electronics, payload, and assembly interfaces.

A parametric chassis model was developed in Fusion 360 and evaluated using finite element analysis under representative operating loads. Stress, deformation, and load-path results guided iterative changes to the geometry and material distribution.

The final design achieved a **15% mass reduction** while maintaining the required structural-integrity targets.

{% include image-gallery.html images="highlight_1784475403273.webp" height="450" %}

---

## Design Requirements

The chassis was designed to:

- Support propulsion components and electronics
- Provide mounting interfaces for the payload
- Maintain structural stiffness under operating loads
- Protect critical components
- Preserve assembly and maintenance access
- Minimize unnecessary structural mass
- Remain compatible with the intended manufacturing process

---

## Parametric CAD Development

Developed the UAV chassis in Fusion 360 using parameter-driven dimensions and reusable geometric features.

The model incorporated:

- Motor and propulsion-system interfaces
- Electronics mounting locations
- Payload attachment features
- Fastener locations
- Assembly clearances
- Structural ribs and cutouts
- Manufacturing constraints

The parametric model allowed major dimensions and structural features to be revised without rebuilding the complete chassis.

---

## Finite Element Analysis

Performed FEA to evaluate:

- Equivalent von Mises stress
- Total deformation
- Structural stiffness
- Critical stress concentrations
- Primary load-transfer paths
- Effects of material removal

Simulation results were used to identify highly loaded regions requiring reinforcement and lower-stress regions suitable for weight reduction.

---

## Structural Optimization

The chassis was refined through an iterative **CAD–FEA–redesign–verification** workflow.

Optimization changes included:

- Removing material from low-stress regions
- Refining structural cutouts
- Adding ribs along principal load paths
- Strengthening mounting interfaces
- Smoothing transitions with fillets
- Adjusting local wall thickness
- Maintaining assembly and manufacturing clearances

Each revised design was reanalyzed to confirm that the mass reduction did not compromise the required structural performance.

---

## Key Accomplishments

Developed a parametric UAV chassis in Fusion 360, incorporating component interfaces, assembly clearances, and manufacturability requirements.

Performed FEA to evaluate stress, deformation, and load paths, then refined cutouts, ribs, fillets, and material distribution in structurally critical regions.

Reduced chassis mass by **15%** while maintaining the required structural-integrity targets and produced engineering drawings, section views, and a bill of materials for fabrication.

---

## Engineering Documentation

Prepared technical documentation to support manufacturing and assembly, including:

- Detailed engineering drawings
- Section views
- Component dimensions
- Mounting-interface information
- Assembly requirements
- Bill of materials

---

## Engineering Insights

The project demonstrated that effective lightweight design requires selective material removal rather than uniform thinning. Material was retained around mounting points and primary load paths while lower-stress regions were modified to reduce mass.

FEA was used throughout the design process to guide geometry changes rather than only as a final validation step.

---

## Future Improvements

- Conduct a formal mesh-convergence study
- Evaluate landing-impact and hard-landing conditions
- Perform modal and vibration analysis
- Include motor thrust and torque in combined load cases
- Manufacture and physically test the chassis
- Compare measured strain and deformation with FEA predictions
- Perform fatigue analysis under repeated flight loading
