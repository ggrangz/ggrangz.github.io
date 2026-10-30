---
layout: post
title: Mechanized C2 Base Station Antenna Mount
description: Preliminary design of a portable, motorized pan mount for steering a directional C2 base-station antenna toward a rover.
skills:
  - Mechanical design
  - CAD
  - Prototyping
  - Requirements analysis
  - Structural design
  - System integration
  - Controls
main-image: /pan_mount_layout_comparison.png
---

## Project status

**Stage:** Preliminary design / prototyping  
**Concept:** Tripod, sectional mast, motorized pan head  
**Antenna:** Ubiquiti AM-5AC21-60  
**Design status:** Proposed layout and estimates; not yet built or validated

> The dimensions, wind loads, torque values, and ballast values on this page are preliminary design estimates. They need to be checked against the final hardware, CAD model, and field tests.

## Situation

During the prototyping stage, our team needed a way to steer the C2 base station’s directional sector antenna toward the rover. The antenna cannot be manually steered to follow the rover, and the URC guidelines do not allow the communications system to rely on the team watching and tracking the rover first-hand.

The guidelines allow an outside, mechanized directional antenna controlled by an electronic signal from the C2 station. Antenna direction can be determined using signal strength, relayed GNSS data, or another strategy, but a camera cannot be mounted on top of the antenna for visual feedback.

The guidelines also set deployment limits:

- The base-station antenna height is limited to **3 m**.
- The antenna base must be within **5 m** of the C2 station.
- Stability ropes or wires must be anchored within **10 m** of the C2 station.

## Task

I was asked to develop a preliminary mount concept that could:

- Steer the antenna **±180°** from its standard orientation, for **360° total travel**.
- Be portable or easy to deploy in the field.
- Place its base within 5 m of the C2 station.
- Anchor stability lines within 10 m of the C2 station.
- Remain below the 3 m antenna-height limit.
- Receive steering commands electronically from the C2 station.
- Determine antenna direction without camera-based visual tracking.

{% include image-gallery.html images="requirements.webp" height="400" %}

## Action

### Proposed architecture

I proposed a tripod with a sectional, collapsible mast and a motorized **pan-only** head at the top. The antenna rotates horizontally to follow the rover; the design has no elevation axis. A three-leg tripod, ground stakes, and guy lines provide field stability.

The mount breaks down into four main parts:

1. Tripod
2. Sectional mast
3. Motorized pan head
4. Stake and guy-line bag

The intended setup is portable and manageable by one person. The mast base would be placed within 5 m of the C2 station. The three guy-line stakes would be placed roughly 2–4 m from the mast, with their final locations checked to keep them within 10 m of the C2 station.

{% include image-gallery.html images="pan_mount_elevation_concept.png" height="400" %}

### Antenna and sourced dimensions

The antenna is the [Ubiquiti AM-5AC21-60](https://store.ui.com/us/en/category/wireless-antennas/products/am-5ac21-60)

{% include image-gallery.html images="sensor.webp" height="400" %}
{% include image-gallery.html images="sensor.webp" height="400" %}

The listed antenna dimensions are **750 × 173 × 78 mm** (29.5 × 6.8 × 3 in). It is rectangular and has no cylindrical diameter. Its top end cap measures **173 × 78 mm**.

The listed weight is **4.8 kg**, including the supplied pole mount but excluding the radio. The radio and additional brackets will add weight and need to be included in the final design.

The sector antenna has a stated **60° beamwidth**. This suggests that a pointing error of around ±10° may be tolerable, but the acceptable error needs to be confirmed against the link requirements.

### Preliminary height and layout options

The antenna consumes a substantial part of the 3 m height budget. The initial on-top layout places the antenna’s upper end at about **2.76 m**, leaving about **240 mm** below the limit. A second layout places the antenna beside the mast and also remains below 3 m.

| Dimension | A: Antenna on top | B: Antenna beside mast |
|---|---:|---:|
| Mast tube | Ø50 × 3 mm wall | Ø50 × 3 mm wall |
| Mast length | 1,800 mm | 2,550 mm |
| Antenna vertical range | 2,010–2,760 mm | 1,920–2,670 mm |
| Highest point | 2,760 mm | 2,722 mm (arm top) |
| Margin below 3,000 mm | 240 mm | 278 mm |
| Tripod leg tube | Ø30 × 2 mm wall | Ø30 × 2 mm wall |
| Tripod leg length | 1,000 mm | 1,150 mm |
| Leg angle | 35° from vertical / 55° from ground | 35° from vertical / 55° from ground |
| Leg-end circle diameter | 1,227 mm | 1,399 mm |
| Tripod collar height | 825 mm | 948 mm |
| Guy-line collar height | 1,500 mm | 1,750 mm |
| Preliminary steel ballast | 3 × Ø200 × 60 mm, 14.8 kg each | 3 × Ø190 × 50 mm, 11.1 kg each |

These are preliminary layout dimensions. The height rule should be checked to confirm whether it is measured to the antenna tip or another component, and which ground reference applies.

{% include image-gallery.html images="pan_mount_layout_comparison.png" height="400" %}

### Pan head and antenna attachment

The proposed pan head uses a housing of approximately **Ø180 × 130 mm**. A slewing bearing of approximately **130 mm OD × 80 mm ID × 20 mm** provides the rotating interface. Its 80 mm center bore leaves a route for the cable. A **Ø160 × 10 mm** top plate brings the total head height to about **160 mm**.

The motor and worm gear would sit inside the housing; their internal geometry has not been designed yet.

For layout A, a **Ø50 mm stub tube** mounts on the pan axis and carries the antenna using its two supplied U-brackets. The stub is about **700 mm long** and attaches to the top plate through an Ø80 mm flange. Its axis is placed about **90 mm behind the antenna’s rear surface** to leave room for the radio.

The Ø50 mm tube is an assumption. The supplied bracket’s supported pole-diameter range needs to be confirmed before selecting or cutting the tube.

### Rotation clearance

The antenna and its attached hardware need clearance through the full ±180° rotation.

With the pan axis through the center of the antenna’s cross-section, the antenna alone sweeps an estimated circle about **378 mm across** in layout A and **621 mm across** in layout B. These estimates include the antenna’s rectangular envelope and mounting offset; they do not include confirmed radio geometry.

A placeholder radio block of **162 × 84 × 37 mm** was estimated from a retailer listing. Its dimensions need to be checked against the actual radio. Cable routing and guy-line attachment points must also stay clear of the swept envelope.

If the axis is placed at the antenna’s back plate instead of through the cross-section, the swept radius grows to the full **173 mm antenna width**, before adding the radio and brackets.

{% include image-gallery.html images="pan_mount_top_view_footprint.png" height="400" %}

### Steering, position feedback, and cabling

The preliminary control concept uses:

- A stepper motor to drive the pan head.
- A worm gear to hold position against wind loads when the motor is unpowered.
- An absolute encoder to report the pan angle.
- A home switch to establish a reference position.
- Electronic pan commands from the C2 station.

The rover’s relayed GNSS position and a heading reference could provide an initial target direction. Peak signal-strength search could serve as a backup or refinement method. No camera is used for antenna feedback.

A single shielded Ethernet cable would run up the mast to the radio. For 360° total travel, a cable service loop with software limits and a rear hard stop is the initial approach. A slip ring is optional and would be considered if the cable arrangement proves unsuitable.

The current layout assumes the radio rides on the rear of the antenna, as intended by the manufacturer. Whether the radio should instead sit at the base with RF jumpers remains an open design question.

### Preliminary wind and torque estimates

The antenna listing gives a wind load of **391 N at 200 km/h**. Scaling that value with the square of wind speed gives approximate antenna loads of:

- **25 N at 50 km/h**
- **48 N at 70 km/h**

These are scaled estimates based on the antenna figure; they do not include confirmed loads from the radio, brackets, mast, or tripod.

An earlier estimate used a 0.1 m center-of-pressure offset. After accounting for the antenna bracket and radio clearance, the estimated offset is closer to:

- **0.13 m** for layout A
- **0.26 m** for layout B

At about 70 km/h, those offsets imply an estimated static wind moment of roughly **6 N·m** for layout A and **12–13 N·m** for layout B. This makes the bearing and holding capacity important, especially for the beside-the-mast arrangement. The pan inertia is estimated to be small, on the order of **0.05 kg·m²**, including the mounting offset. These estimates need to be checked using the final mass properties and geometry.

### Preliminary stability and ballast estimate

The ballast figures in the table come from a preliminary **no-guy tipping check** at about 70 km/h, using the scaled antenna wind load and a 1.5 safety factor. The estimate assumes a structure mass of roughly **17–19 kg**, which has not yet been weighed or analyzed.

Guy lines and stakes should reduce the ballast requirement. Sand or water bags may be more practical to transport than steel ballast. The final ballast and anchoring approach depend on the completed structural and field stability checks.

## Result

The preliminary concept defines a portable, motorized pan mount and two candidate antenna layouts. Both layouts are estimated to fit below the 3 m height limit, with the base and stability anchors placeable within the stated URC distances. The control concept uses electronic commands and non-visual feedback, with a cable plan for the required 360° total travel.

The work is still at the design and prototyping stage. No claim is made that the mount has been built, tested, or validated.

{% include image-gallery.html images="antenna.png" height="400" %}

## Open items and next steps

1. Confirm how the URC measures the 3 m height limit, including the relevant ground reference and whether the antenna tip is the measurement point.
2. Confirm the actual radio weight, dimensions, and mounting arrangement.
3. Measure the supplied U-bracket’s supported pole diameter before finalizing the stub tube.
4. Build the full antenna, radio, bracket, and cable geometry into CAD and check the complete rotation envelope.
5. Compare the on-top and beside-the-mast layouts, including bearing loads and center-of-gravity effects.
6. Analyze mast and tripod stiffness at the proposed height, including the guy lines; consider FEA.
7. Recalculate wind loads and holding torque using the final assembly geometry and mass properties.
8. Validate the tripod, stakes, guy lines, and any ballast in field conditions.
9. Detail the motor, worm gear, encoder, home switch, controls, software limits, hard stop, and cable service loop.
10. Confirm whether the radio rides on the antenna or sits at the base with RF jumpers.
