# Ferrofluid Lubricated Ball Bearing for a Ceiling Fan Motor

Design and simulation of a modified deep groove ball bearing that uses a ferrofluid lubricant held in place by the motor's own magnetic field, so no permanent magnet ring is needed. Undergraduate design and fabrication project (course ME8682), B.E. Mechanical Engineering, Meenakshi Sundararajan Engineering College, Anna University, May 2021.

**Tools:** SolidWorks (2D and 3D models), Ansys Workbench 18.1 (static and transient structural analysis), PSG Design Data Book (bearing selection and life calculation)

## Problem

Ceiling fans use grease-lubricated deep groove ball bearings above and below a single-phase induction motor (SKF 6202 on top, 6201 below). Grease does not respond to magnetic fields and thins as the bearing heats up, so friction varies across operating conditions and bearing life suffers.

Conventional ferrofluid bearings hold the lubricant with permanent magnet rings. Near a motor, those rings can disturb the motor's own field. This project instead relies on the stator field, which the bearings already sit inside, to hold and thicken the ferrofluid around the balls and races.

## Approach

1. **Literature review.** Five papers on ferrofluid bearings, seals and motor applications. One of them identified the distance to the magnetic field source as a major factor, which led to the choice of ceiling fans, where the bearings sit close to the stator.
2. **Material selection.** AISI 52100 high-carbon chromium bearing steel, chosen against fatigue strength, seizure, wear, conformability, embeddability, corrosion and cavitation criteria (60–67 HRC, usable up to 120 °C).
3. **Analytical check.** Bearing life calculation for both bearings using the PSG Design Data Book.
4. **Design change.** Extra slots cut on both sides around the ball grooves of the standard 6201 and 6202 bearings, to increase the ferrofluid volume and the surface area available for dissipating friction heat.
5. **Simulation.** Static and transient structural analysis of both modified bearings in Ansys.
6. **Fabrication plan.** Process route for the races and balls (forging, turning, grinding, heading, lapping) and assembly layout, with a cost estimate.

## Design check

Running conditions assumed for an average ceiling fan: 315 rpm, 8,000 hours of life (about 2 years at 10 hours a day), service factor 1.1.

| | SKF 6202 (upper) | SKF 6201 (lower) |
|---|---|---|
| Radial load | 989.8 N | 886.4 N |
| Axial load | 435.5 N | 390.0 N |
| Equivalent load P | 1,088.8 N | 975.0 N |
| Required dynamic capacity | 5,792 N | 5,187 N |
| Rated dynamic capacity C | 6,100 N | 5,400 N |
| Result | Safe | Safe |

## Simulation

| Analysis | Setup |
|---|---|
| Static structural | Inner race fixed, 10 MPa pressure on the outer race to represent the centrifugal load from the fan blades. Checks structural integrity under worst-case external load. |
| Transient structural | Inner race fixed, revolute joints on balls and races, outer race driven to 400 rpm in 5 increasing sub-steps to represent start-up. |

The report finds that stresses and deformations while the bearing runs are larger than those from the external fan load, and that the added slots do not greatly affect structural integrity. The stress and deformation plots for both bearings are in the report. The report does not tabulate peak values.

## Cost estimate

About Rs 4,415 for a pair: Rs 955 of AISI 52100 bar, Rs 3,300 for 30 ml of ferrofluid, and Rs 80 per unit fabrication.

## Limitations

- The project covers design, analysis and a fabrication plan. The modified bearings were not built or tested in a running fan, so the lubrication, heat dissipation and sealing benefits listed in the conclusion are expected outcomes based on the literature, not measured results.
- The structural simulations do not model the magnetic field or the ferrofluid itself.
- The report assumes the axial load does not enter the equivalent load calculation (X = 1, Y = 0). Re-checking that assumption against the bearing tables is a worthwhile next step.

## Team

Abishek Sarvan N. A. S., Adharsh Rajasekar and Sriman Saii P. V. Supervisor: Mr. V. Meganathan, Assistant Professor, Department of Mechanical Engineering, Meenakshi Sundararajan Engineering College.
