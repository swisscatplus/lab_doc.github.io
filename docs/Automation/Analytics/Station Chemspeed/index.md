---
title: Station Chemspeed
layout: default
parent: Analytics
grand_parent: Automation
---

This station serves as the interface between the analytics and synthesis areas. Once an experiment plate is completed 
in the Chemspeed systems, it is placed into the airlock chamber of the MBraun glovebox. 
Multiple vacuum cycles are performed to ensure 
that the samples are ready to be exposed to the laboratory atmosphere. The airlock doors then open, and a drawer is 
extended outward.  The Universal Robot picks and places the plate from the airlock drawer onto the Mobile Robot on the track.

The UR controller and the Chemspeed control softare Autosuite are connected via I/O signals, allowing both systems to 
interlock, as they are operated by separate schedulers.

To ensure operator safety, the Universal Robot safety system is connected to a proximity sensor that detects whether 
the protective door is open. If the door is opened, the robot immediately stops.

The code for the Universal Robot can be found in the following repository:

<span class="fs-2">[Universal Robot Programs](https://github.com/swisscatplus/Auto_Analytic_UR){: .btn .btn-purple }</span>

## Picture of the Station

![](../../../../assets/images/Automation/station_chemspeed.jpg)


## List of Components

- MBraun Airlock Chamber

![](../../../../assets/images/Automation/station_chemspeed_airlock.jpg)

- Universal Robot UR5e & Controller

![](../../../../assets/images/Automation/station_chemspeed_UR.jpg)

- Robot Gripper
![](../../../../assets/images/Automation/station_chemspeed_gripper.jpg)

- Industrial Camera

![](../../../../assets/images/Automation/station_chemspeed_camera.jpg)

- Aluminium Profile & Plexiglas Door with presence sensor

![](../../../../assets/images/Automation/station_chemspeed_door_sensor.jpg)

- Aluminium Profile table

![](../../../../assets/images/Automation/station_chemspeed_structure.jpg)


