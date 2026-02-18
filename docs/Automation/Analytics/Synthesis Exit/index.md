---
title: Synthesis Exit
layout: default
parent: Analytics
grand_parent: Automation
---


This station serves as the interface between the analytics and synthesis areas. Once an experiment is completed, the plates are inserted into the airlock chamber of the MBraun glovebox. Multiple vacuum cycles are performed to ensure that the samples are ready to be exposed to the laboratory atmosphere. The airlock doors then open, and a drawer is extended outward.
The Universal Robot picks and places the plate from the airlock drawer onto the Mobile Robot on the track.

The code for the Universal Robot can be found in the following repository:

The UR controller and the Chemspeed control system are connected via I/O signals, allowing both systems to interlock, as they are operated by separate schedulers.

To ensure operator safety, the Universal Robot safety system is connected to a proximity sensor that detects whether the protective door is open. If the door is opened, the robot immediately stops.

<span class="fs-2">[Universal Robot Programs](https://github.com/swisscatplus/Auto_Analytic_UR){: .btn .btn-purple }</span>

## List of Components

- MBraun Airlock Chamber
- Universal Robot UR5e & Controller
- Industrial Camera
- Aluminium Profile & Plexiglas Door with presence sensor
- Aluminium Profile table

![](./../../../../assets/images/auto_analytics_synthesisExit.jpg)

