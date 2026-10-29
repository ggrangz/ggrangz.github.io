
---
layout: post
title: Two-DOF Vibration Platform for a Planetary Lander Footpad
description: >-
  Developing a mechanically supported, instrumented two-degree-of-freedom
  vibration platform to study the mechanical response of a scaled planetary
  lander footpad in soil simulant.
skills:
  - Mechanical Design
  - CAD and Kinematic Modeling
  - Prototype Development
  - Transducer Instrumentation
  - Experimental Data Collection
main-image: /22_23_09.png
---

## Situation

I am developing a scaled planetary-lander footpad test setup to study its mechanical response in planetary soil simulant. During design reviews, I identify that two separate one-axis mechanisms do not give one footpad two degrees of freedom. The approved proof of concept uses two stacked stages so both actuators contribute to the same footpad’s motion.

## Task

I am developing a mechanically supported, two-degree-of-freedom vibration platform for one scaled landing footpad. I am also preparing the apparatus for simulant preparation, transducer instrumentation, and mechanical data collection.

## Action: Step-by-Step Prototype Plan

### 1. Define the requirements

I document the intended footpad motions, travel limits, expected test loads, available space, soil-container dimensions, and required measurements. I define the coordinate system and confirm the motion axes and actuator orientation against the professor’s drawing before I finalize the layout.

**Checkpoint:** I complete a requirements list and mark up the reference drawing to identify both motion axes, their travel, and the footpad location.

### 2. Model the two-degree-of-freedom kinematics

I create a CAD assembly with a base, a first linear stage, a second stage mounted on the first, and one shared footpad plate. I constrain each stage to move along its intended axis. I check each axis separately, then move both stages together to verify that the same footpad receives both motions.

**Checkpoint:** I verify in the model that the shared footpad moves in two independent directions and that the stages work together as one nested system.

### 3. Place the actuators, rails, and moving plates

I place one actuator and rail set for each stage. I orient each actuator so it drives the intended stage motion. If I use a voice-coil actuator, I align its linear force axis with the stage direction. If I use a rotating vibration motor, I follow the professor’s guidance that its vibration direction is normal to its rotary axis. I check rail direction, clearances, stroke limits, fastener access, and interference over the full travel.

**Checkpoint:** I document each actuator’s type, force or vibration direction, rail direction, and the stage it drives in the assembly drawing.

### 4. Build a low-cost, non-powered motion prototype

I make a small-scale or full-size mock-up from simple plates, linear guides, and fasteners before I commit to the final frame. I assemble the base and lower stage first, then mount the upper stage and footpad plate. I move each stage by hand separately and together, checking for binding, unintended rotation, excessive play, and loss of alignment.

**Checkpoint:** I move each stage through its planned travel by hand and verify that the upper stage stays supported and aligned as the lower stage moves.

### 5. Add structural support

I design a rigid frame that supports the rails, captures their ends, and carries the expected moving loads. I include cross-bracing, mounting points, fasteners, and assembly access. I review unsupported spans, twisting, rail alignment, and likely stress concentrations before I select a fabrication method and material.

**Checkpoint:** I verify in CAD that every rail and carriage attaches to the supported frame and that the assembly fits its intended inverted orientation.

### 6. Assemble and check the mechanism without simulant

I mount the frame in its intended inverted orientation so the footpad can extend down into the soil container. I install the stages and actuators, then check the full travel without simulant. I begin with low-amplitude operation, verify each motion axis independently, and inspect for binding, loosened fasteners, frame movement, and contact with the container.

**Checkpoint:** I verify that both axes operate as intended and the footpad reaches its planned position in the container without contacting the frame or container.

### 7. Install and check the instrumentation

I select transducers for the measurements I need, such as footpad or frame acceleration, displacement, or force. I record each sensor’s location, orientation, units, calibration status, and sampling settings. I collect a short baseline recording and confirm that each channel responds as expected before I test with simulant.

**Checkpoint:** I document the sensor layout and data channels, then confirm that the baseline recording is usable for comparison.

### 8. Prepare the simulant and test container

I document the simulant material, preparation method, fill depth, and controlled conditions. I prepare the container consistently, position the inverted mechanism, and record the initial setup before each run. I keep the footpad placement and test procedure consistent between runs.

**Checkpoint:** I verify that I can reproduce the container and simulant setup from my written preparation procedure.

### 9. Run tests and collect mechanical data

I run the planned tests using documented actuator inputs and sensor settings. I label every dataset with the date, setup configuration, axis or axes tested, simulant conditions, and sensor configuration. I inspect recordings for missing channels, clipping, unexpected noise, and inconsistent initial conditions, then compare footpad response across axes and runs.

**Checkpoint:** I keep a traceable setup record for each test and review each dataset for suitability for analysis.

### 10. Iterate the prototype

I use the motion checks and test data to identify binding, vibration coupling, structural movement, alignment issues, and measurement problems. I update the CAD assembly, prototype, and test procedure to address those findings. I repeat the relevant checks after each change before I move toward a fabrication-ready build.

**Checkpoint:** I document each design change and its verification result so every prototype iteration has a clear basis.

## Design Images

The image files are stored alongside this `index.md` in the project folder shown in the gallery include paths.

### Initial rail and actuator layout

{% include image-gallery.html images="22_22_45.png" height="400" %}
### Two-stage concept iteration

{% include image-gallery.html images="22_22_56.png" height="400" %}
### Exploded assembly iteration

{% include image-gallery.html images="22_23_00.png" height="400" %}
### Separate one-degree-of-freedom layouts

{% include image-gallery.html images="22_23_05.png" height="400" %}
### Approved nested two-degree-of-freedom concept

{% include image-gallery.html images="22_23_09.png" height="400" %}
## Result

The current proof of concept shows how two stacked stages give one footpad two degrees of freedom, and the professor confirms that the arrangement is operationally equivalent to the meeting drawing. I am developing the concept into a structurally supported, instrumented prototype through the steps above. Fabrication and experimental results remain part of my ongoing work.




