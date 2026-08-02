---
layout: post
title: SMA-Actuated Soft Robotic Finger
description: >-
  Designed, manufactured, and tested a cast-silicone soft robotic finger with
  SMA actuation, tendon routing, and directional-friction features for repeatable
  bending and surface locomotion.
skills:
  - SolidWorks
  - Soft Robotics
  - Design for Additive Manufacturing
  - FDM Mold Tooling
  - Silicone Casting
  - Shape-Memory Alloys
  - Experimental Validation
  - Root-Cause Analysis
main-image: /highlight_1784475201361.webp
---

## Timeline

**12-week multidisciplinary project**

---

## Project Overview

Collaborated with mechatronics students to design, manufacture, and test a silicone soft-robotic finger capable of repeatable bending and surface locomotion.

The project integrated mechanical design, multi-part FDM mold tooling, silicone casting, tendon routing, shape-memory-alloy actuation, resistance wiring, and experimental validation. Early prototypes experienced asymmetric bending, lateral twisting, inconsistent actuation, and tendon-anchor tearing.

These problems were addressed through iterative SolidWorks revisions, controlled prototype testing, cross-sectional inspection, and quantitative comparison between the CAD geometry and manufactured parts.

---

## Key Accomplishments

### Finger and Mold Design

Developed the baseline finger geometry in SolidWorks and produced rigid PLA prototypes to evaluate dimensions, joint placement, range of motion, and manufacturability before silicone casting.

Designed multi-part FDM-printable molds using Draft Analysis, Parting Line, Tooling Split, alignment features, and wall-thickness verification. Produced cast components with airtight chamber walls and less than **5% dimensional deviation from CAD**.

### Deformation Control

Adjusted local wall thickness, hinge geometry, chamber spacing, and fillet radii to concentrate deformation at the intended knuckle regions while retaining additional material around structural and actuator interfaces.

### Fabrication and Integration

Cast and assembled silicone prototypes containing internal tendon paths, SMA actuators, resistance wiring, and reinforced anchor features. Evaluated casting quality, dimensional accuracy, bending angle, lateral deviation, actuation time, and repeated-cycle behavior.

### Root-Cause Analysis

Isolated asymmetric bending as a mechanical problem by manually pulling the tendon with the SMA disconnected. Because the finger continued twisting without electrical actuation, the current-control system was eliminated as the primary cause.

Sectioned a failed prototype at four locations and measured the internal channel position relative to both sidewalls. The channel was displaced approximately **0.3–0.4 mm** from the CAD centerline.

Redesigned and reprinted the mold to improve core support and alignment. Recasting and repeated section measurements reduced channel offset to **less than 0.1 mm**, producing more symmetric in-plane bending.

### Tendon-Anchor Improvement

Investigated tearing and anchor movement produced by repeated actuation. Added a filleted transition that distributed the tendon load across a larger silicone volume, reducing localized stress and improving assembly durability.

### Surface Locomotion

Investigated locomotion as a friction-management problem rather than only an actuator-force problem. Compared smooth PLA contact surfaces, silicone-rubber pads, and fine-grit abrasive surfaces.

Smooth PLA allowed easy sliding but provided little traction. Silicone rubber increased grip but resisted motion in both directions. Fine-grit surfaces produced high traction but increased wear on the silicone.

Added angled silicone ribs at the finger base and tip to create directional friction. The ribs flexed during forward motion and resisted reverse sliding, producing more consistent net displacement per actuation cycle than symmetric flat contact surfaces.

Evaluated displacement per cycle, bending angle, actuation time, and cycle-to-cycle repeatability to compare locomotion configurations.

{% include image-gallery.html images="finger-cad.webp, mold-tooling.webp, silicone-prototype.webp" height="350" %}

---

## Engineering Insights

The project demonstrated that soft-robotic performance depends strongly on manufacturing accuracy. A channel offset of less than half a millimeter was sufficient to produce measurable lateral twisting.

Reliable surface locomotion also required friction asymmetry. Increasing actuator force alone improved bending but did not guarantee forward movement when the base and tip had similar friction in both directions.

---

## Project Outcome

Delivered an integrated silicone soft finger with SMA actuation, controlled tendon routing, improved anchor durability, and more symmetric bending. The project established a repeatable design-manufacture-test workflow for diagnosing geometric defects and improving soft-robotic motion.
