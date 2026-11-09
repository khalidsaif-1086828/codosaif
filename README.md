# codosaif
# Falcon-Inspired Robotic Claw

## Smart Robotic Claw Inspired by Falcon Talons

**Abu Dhabi University — College of Engineering**  
**Course:** MEC 482 — Introduction to Mechatronics  
**Project:** Mechatronics Mega Project  
**Project Status:** Initial Research and Design Stage

---

## Home

### Team Members

| Name | University Email |
|------|------------------|
| khaled alhameli | 1086828 |
| saad Shahid | 1089255 |
| Saad Mulla | 1085412 |
| Sazzad Hosain Sayeed | 1093153 |

**Institution:** Abu Dhabi University, United Arab Emirates

---

## 1. Project Overview

Our project aims to design and develop a robotic claw inspired by the natural gripping mechanism of a falcon.

Falcons have strong and curved talons that allow them to catch and hold objects securely. We want to study this natural mechanism and apply a similar idea to a robotic system.

The robotic claw will be built from soft fingers, electronic sensors, and an Arduino microcontroller.

Our main goal is to develop a claw that can grip different objects while controlling the gripping force.

Since we are still in the early stage of the project, we are researching different claw mechanisms and selecting the most suitable design.

---

## 2. Project Objectives

The main objectives of our project are:

1. Design a robotic claw inspired by falcon talons.
2. Develop soft fingers that bend in a curved shape similar to falcon talons.
3. Use Arduino to control the opening and closing of the claw.
4. Use air pressure to bend the fingers and grip objects.
5. Integrate a force sensor to measure the gripping force.
6. Design the parts and molds in AutoCAD and manufacture them using 3D printing.
7. Test the gripping performance with different objects.

---

## 3. Inspiration From Nature

### Why Did We Choose a Falcon Claw?

Falcons have powerful claws that help them capture and hold their prey.

Their talons have several important characteristics:

- Curved shape for effective gripping.
- Strong gripping ability.
- Flexible finger movement.
- Natural tendon-based movement.
- Ability to hold objects securely.

We want to apply some of these characteristics to our robotic claw design.

---

## 4. Initial Design Research

During our initial research, we found several robotic claw designs that could help us develop our project.

We noticed that different designs use different mechanisms.

Some designs divide each finger into several sections connected by joints.

Other designs use a single curved finger without multiple sections.

We compared these designs to find the mechanism that is easiest to manufacture and control.

### Design Concept 1: Tendon-Driven Robotic Gripper

This design uses tendon wires to move the robotic fingers.

A motor pulls the tendon, causing the fingers to bend and grip an object.

This mechanism is interesting because it is similar to the movement of natural tendons.

**Main Components:**

- Motor
- Pulley
- Tendon wire
- Finger joints
- Rigid links
- Base structure

**Reference:**

https://doi.org/10.1177/0278364920907697

### Design Concept 2: Bio-Inspired Claw Mechanism

The second design uses curved claw structures inspired by animal gripping mechanisms.

This design is useful because it provides ideas for the shape and movement of our robotic claw.

**Reference:**

https://www.preprints.org/manuscript/202508.0109

### Design Concept 3: Soft Fiber-Reinforced Fingers (Selected Design)

After further research, we found the soft finger designs on the Soft Robotics Toolkit, and we chose the **Fiber-Reinforced Bending Actuator** as the gripping fingers of our claw.

Each finger is a soft silicone tube (bladder) wrapped with a strong thread that does not stretch. One side of the finger also has a flat layer that does not stretch.

**How the finger works:**

- When air is pumped into the finger, the silicone tries to expand.
- The thread wrapped around the finger stops it from expanding outward, so the finger can only get longer.
- The flat layer on one side stops that side from getting longer.
- Only the other side gets longer, so the finger **bends inward** in a curved shape and wraps around the object.
- When the air is released, the silicone returns to its original straight shape by itself.

**Why we chose this design:**

- The curved bending shape is very similar to how a falcon's talons close around prey.
- The soft silicone adapts to the shape of the object and grips gently, so fragile objects are less likely to be damaged.
- The fingers return to their original position by themselves, without springs.
- The finger has only a small seam at its end caps, so it is less likely to tear or leak than other soft fingers.
- The motion can be changed by changing how the thread is wrapped (bending, extending, or twisting).
- The molds can be designed in AutoCAD and 3D printed.

**Challenge:**

This finger takes longer to manufacture than other soft fingers. Casting can take up to five days, so we need to plan the fabrication time early.

**Reference:**

https://softroboticstoolkit.com/book/fiber-reinforced-bending-actuators

---

## 5. Proposed Components

The following components are currently being considered for our project.

| Component | Function |
|-----------|----------|
| Arduino Uno | Controls the robotic claw |
| Silicone Rubber | Forms the soft fingers |
| Inextensible Thread | Wraps the fingers so they bend instead of expanding |
| Inextensible Flat Layer (fabric or paper) | Makes one side of the finger stiff so the finger bends |
| 3D Printed Molds | Used to cast the silicone fingers |
| 3D Printed Base | Holds the fingers and the electronic parts |
| Air Pump | Supplies air to the fingers |
| Solenoid Valves | Let air into the fingers and release it |
| Air Tubes and Connectors | Carry air from the pump to the fingers |
| Pressure Sensor | Measures the air pressure inside the fingers |
| Force Sensor | Measures the gripping force |
| Relay / MOSFET Driver | Lets the Arduino switch the pump and valves |
| Power Supply | Provides electrical power |
| Connecting Wires | Connect electronic components |

The final components may change depending on our design and testing results.

---

## 6. Proposed Working Principle

The robotic claw is expected to operate using the following steps:

**Step 1:** Arduino turns on the air pump and opens the inlet solenoid valve.

**Step 2:** Air flows through the tubes into the soft fingers.

**Step 3:** The fingers bend inward because of their thread wrapping and stiff layer.

**Step 4:** The claw closes around an object.

**Step 5:** The force sensor measures the gripping force, and the pressure sensor measures the air pressure.

**Step 6:** When the required gripping force is reached, Arduino closes the valve and stops adding air.

**Step 7:** To release the object, Arduino opens the exhaust valve, the air leaves the fingers, and they return to their original straight shape.

This is our proposed working mechanism and will be evaluated during the design stage.

---

## 7. Mechanical Design

We plan to design the robotic claw using AutoCAD.

The design will include:

- Main supporting base.
- Molds for the soft fingers.
- Finger mounting points on the base.
- Air tube routing.
- Pump and valve mounting location.
- Force sensor mounting position.

After completing the design, we plan to manufacture the base and molds using a 3D printer.

### Finger Manufacturing Steps

1. Design the finger molds in AutoCAD and export them as STL files.
2. 3D print the mold pieces.
3. Cast the first silicone layer and add the flat inextensible layer on one side.
4. Wrap the thread around the finger.
5. Cast an outer silicone layer to cover and hold the thread.
6. Seal the end caps and connect the air tube.
7. Test the finger for leaks and bending.

---

## 8. Arduino Control System

Arduino will act as the main controller of our robotic claw.

It will be responsible for:

- Turning the air pump on and off.
- Opening and closing the solenoid valves.
- Controlling the opening and closing of the claw.
- Reading the pressure sensor and the force sensor.
- Monitoring the gripping force.
- Helping prevent excessive gripping force and pressure.

The Arduino program will be developed after selecting the final electronic components.

---

## 9. Expected Applications

Our robotic claw could potentially be used in:

1. Robotic gripping systems.
2. Handling small and fragile objects.
3. Educational robotics.
4. Bio-inspired robotic research.
5. Automated pick-and-place applications.

These are possible applications that we will explore as the project develops.

---

## 10. Current Project Progress

### Completed

- Selected the initial project idea.
- Identified the falcon claw as our inspiration.
- Researched existing robotic claw designs.
- Selected the soft fiber-reinforced finger as our finger design.
- Identified possible components.
- Developed an initial working concept.

### In Progress

- Planning the mechanical structure.
- Researching air pumps, solenoid valves, and pressure sensors.
- Researching force sensors.

### Not Started Yet

- Final AutoCAD design.
- 3D printing of the molds and base.
- Casting the silicone fingers.
- Arduino programming.
- Physical assembly.
- Experimental testing.
- Final performance evaluation.

---

## 11. Next Steps

Our next steps are:

1. Design the finger molds and the base in AutoCAD.
2. Determine the required gripping force.
3. Select a suitable air pump and solenoid valves.
4. Choose the pressure sensor and force sensor.
5. 3D print the molds and cast the fingers.
6. Develop the Arduino control system.
7. Assemble the prototype.
8. Test the gripping performance.

---

## 12. Expected Results

At the end of this project, we aim to develop a functional robotic claw capable of opening, closing, and gripping objects.

We also aim to measure the gripping force using a sensor and control the claw using Arduino.

The final performance will depend on the finger design, the air pressure, and experimental results.

---

## 13. References

**Reference 1:**

Tendon-driven robotic gripper design research.

https://doi.org/10.1177/0278364920907697

**Reference 2:**

Bio-inspired claw mechanism research.

https://www.preprints.org/manuscript/202508.0109

**Reference 3:**

Soft Robotics Toolkit — Fiber-reinforced soft bending actuators.

https://softroboticstoolkit.com/book/fiber-reinforced-bending-actuators

