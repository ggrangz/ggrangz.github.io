# Two-DOF Vibration Platform for a Planetary Lander Footpad

## Situation

I am developing a scaled planetary-lander footpad test setup to study its mechanical response in planetary soil simulant. During design reviews, I identify that two separate one-axis mechanisms do not give one footpad two degrees of freedom. The approved proof of concept uses two stacked stages so both motors contribute to the same footpad’s motion.

## Task

I am developing a mechanically supported, two-degree-of-freedom vibration platform for one scaled landing footpad. I am also preparing the apparatus for simulant preparation, transducer instrumentation, and mechanical data collection.

## Action: step-by-step prototype plan

### 1. Define the requirements

I document the intended footpad motions, travel limits, expected test loads, available space, soil-container dimensions, and measurements. I define the coordinate system and confirm the motion axes and actuator orientation against the professor’s drawing before fixing the layout.

**Checkpoint:** I have a requirements list and a marked-up reference drawing that identify both motion axes, their travel, and the footpad location.

### 2. Model the two-degree-of-freedom kinematics

I create a CAD assembly with a base, a first linear stage, a second stage mounted on the first, and one shared footpad plate. I constrain each stage to move along its intended axis. I check each axis separately, then move both stages together to verify that the footpad receives both motions.

**Checkpoint:** The model shows one shared footpad moving in two independent directions, with no stage behaving as a separate one-degree-of-freedom system.

### 3. Place the motors, rails, and moving plates

I place one motor and rail set for each stage. I orient each motor using the vibration direction specified for the selected motor and the professor’s guidance that vibration is normal to the motor’s rotary axis. I check that each stage constrains the intended motion, then review clearances, stroke limits, fastener access, and interference over the full travel.

**Checkpoint:** The assembly drawing identifies each motor, its rotary axis, its intended excitation direction, its rail direction, and the stage it drives.

### 4. Build a low-cost, non-powered motion prototype

I make a small-scale or full-size mock-up from simple plates, linear guides, and fasteners before committing to the final frame. I assemble the base and lower stage first, then mount the upper stage and footpad plate. I move each stage by hand separately and together, checking for binding, unintended rotation, excessive play, and loss of alignment.

**Checkpoint:** Each stage moves through its planned travel by hand, and the upper stage remains supported and aligned while the lower stage moves.

### 5. Add structural support

I design a rigid frame that supports the rails, captures their ends, and carries the expected moving loads. I include cross-bracing, mounting points, fasteners, and access for assembly. I review unsupported spans, twisting, rail alignment, and likely stress concentrations before selecting a fabrication method and material.

**Checkpoint:** The supported CAD assembly has no floating subsystems, and the frame holds the rails in alignment in the intended inverted orientation.

### 6. Assemble and test the mechanism without simulant

I mount the frame in its intended inverted orientation so the footpad can extend down into the soil container. I install the stages and motors, then check the full travel without simulant. I begin with low-amplitude operation, verify each motion axis independently, and inspect for binding, loosened fasteners, frame movement, and contact with the container.

**Checkpoint:** Both axes operate as intended, the footpad reaches the planned position above the container, and the frame and rails remain aligned during the check.

### 7. Install and check the instrumentation

I select transducers for the measurements I need, such as footpad or frame acceleration, displacement, or force. I record each sensor’s location, orientation, units, calibration status, and sampling settings. I collect a short baseline recording and confirm that each channel responds as expected before testing with simulant.

**Checkpoint:** The sensor layout and data channels are documented, and the baseline recording is usable for comparison.

### 8. Prepare the simulant and test container

I document the simulant material, preparation method, fill depth, and controlled conditions. I prepare the container consistently, position the inverted mechanism, and record the initial setup before each run. I keep the footpad placement and test procedure consistent between runs.

**Checkpoint:** I can reproduce the container and simulant setup using the written preparation procedure.

### 9. Run tests and collect mechanical data

I run the planned tests using documented actuator inputs and sensor settings. I label every dataset with the date, setup configuration, axis or axes tested, simulant conditions, and sensor configuration. I inspect recordings for missing channels, clipping, unexpected noise, and inconsistent initial conditions, then compare footpad response across axes and runs.

**Checkpoint:** Each test has a traceable setup record and a reviewed dataset suitable for analysis.

### 10. Iterate the prototype

I use the motion checks and test data to identify binding, vibration coupling, structural movement, alignment issues, and measurement problems. I update the CAD assembly, prototype, and test procedure to address those findings. I repeat the relevant checks after each change before moving toward a fabrication-ready build.

**Checkpoint:** I document each design change and its verification result so the next prototype iteration has a clear basis.

## Result

The current proof of concept shows how two stacked stages give one footpad two degrees of freedom, and the professor confirms that the arrangement is operationally equivalent to the meeting drawing. I am developing the concept into a structurally supported, instrumented prototype through the steps above. Fabrication and experimental results remain part of my ongoing work.

