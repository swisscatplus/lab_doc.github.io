---
title: Station Chemspeed
layout: default
parent: Analytics
grand_parent: Automation
---

# Station Chemspeed

## General Purpose

The **Chemspeed Station** serves as the interface between the analytics and synthesis areas.

Once an experiment plate is completed in the Chemspeed systems, it is transferred to the **MBraun glovebox airlock chamber**.  
Several vacuum cycles are performed to prepare the samples for safe exposure to the laboratory atmosphere.

After the airlock sequence is completed:

1. The airlock doors open  
2. The drawer extends outward  
3. The Universal Robot (UR) retrieves the plate  
4. The plate is placed onto the Mobile Robot positioned on the track  

---

## Interlock

The **Universal Robot controller** and the **Chemspeed Autosuite control software** are connected via I/O signals.

This allows both systems to operate under an interlock mechanism, ensuring synchronized operation despite being managed by separate schedulers.

---

## Safety

To ensure operator safety:

- The Universal Robot safety system is connected to a proximity sensor.
- The sensor detects whether the protective door is open.
- If the door is opened, the robot immediately stops.

This guarantees safe human-robot interaction during operation.

---

## Code Repository

The Universal Robot programs are available in the following repository:

<span class="fs-2">[Universal Robot Programs](https://github.com/swisscatplus/Auto_Analytic_UR){: .btn .btn-purple }</span>

---

## Station Overview

<img src="../../../../assets/images/Automation/station_chemspeed.jpg" 
     alt="Overview of the Chemspeed station including airlock and Universal Robot" 
     width="50%">

---

## Components

### MBraun Airlock Chamber

<img src="../../../../assets/images/Automation/station_chemspeed_airlock.jpg" 
     alt="MBraun glovebox airlock chamber used for sample transfer" 
     width="50%">

---

### Universal Robot UR5e & Controller

<img src="../../../../assets/images/Automation/station_chemspeed_UR.jpg" 
     alt="Universal Robot UR5e arm and controller cabinet" 
     width="50%">

---

### Robot Gripper

<img src="../../../../assets/images/Automation/station_chemspeed_gripper.jpg" 
     alt="Robot gripper used for handling experiment plates" 
     width="50%">

---

### Industrial Camera

<img src="../../../../assets/images/Automation/station_chemspeed_camera.jpg" 
     alt="Industrial camera mounted on the station for monitoring or detection" 
     width="50%">

---

### Aluminium Profile & Plexiglas Door with Presence Sensor

<img src="../../../../assets/images/Automation/station_chemspeed_door_sensor.jpg" 
     alt="Protective Plexiglas door with presence sensor for safety interlock" 
     width="50%">

---

### Aluminium Profile Table

<img src="../../../../assets/images/Automation/station_chemspeed_structure.jpg" 
     alt="Aluminium profile structural table supporting the station components" 
     width="50%">