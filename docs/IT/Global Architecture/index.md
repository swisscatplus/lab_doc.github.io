---
title: Global Architecture
layout: default
parent: IT
---

This is the Global Architecture doc for IT.

The full architecture is pyramidal.
At the top there is the HCI, which converts the chemist input into workflows for samples.

The HCI then sends the corresponding workflows to the laboratory scheduler.
The laboratory scheduler then orchestrates the workflows according to the instruments state.
It is the responsibility of the scheduler to send the workflows to the appropriate instruments at the right time and with the righ parameters.

The scheduler is developed in Swiss CAT+ with the help of Coteries and is available here: [Scheduler](https://github.com/swisscatplus/scheduler){: .btn .btn-green }