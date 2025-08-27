---
title: 3. Sample preparation
layout: default
parent: Analytics
---

### Bravo

Put a picture of them 

**Purpose:** To prepare samples coming from the synthesis part to inject them in the analytical machines.

- Bravo 1 is focused on microplates changements by aspiration steps, on agitation and on dilutions with different solvents (D2 or not).

- Bravo 2 is focused on the SPE part (5uL and 25uL cartridges) for volatiles molecules.

They work with the VWorks software

They move depending on four different axes:
- X = length movement
- Y = width movement
- Z = height movement
- W = liquid volume in tips

There are two ways of using them so two different processes. It can be used independently or with the KX2 robot. The KX2 enables to move microplates from a bravo to another or from a device to another such as the microplate labeler, the centrifuge or the evaporator. 

**Process:** (to use it alone)

- Initialize all devices on VWorks and check if there are errors
- Open the protocol file wanted
- Check tasks parameters such as "distance from well bottom" and the "labware configuration" -> avoid to do it during the protocol is running 
- Click on "compile" to check if the software detects errors that will happen during the protocol
- Run protocol
- Collect the final microplate tu use it forward

**Process:** (to use it combined with the KX2)

- 