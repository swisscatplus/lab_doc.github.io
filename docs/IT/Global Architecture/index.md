---
title: Global Architecture
layout: default
parent: IT
---

This is the Global Architecture doc for IT.

![](..../assets/images/it_structure.png)


The full architecture is pyramidal.
At the top is the HCI (IN COLLABORATION WITH MESTRELAB RESEARCH), which converts the chemist input into workflows for samples.
The HCI includes specific features for our laboratory. Digital laboratories with high degree of automation require specific interfaces in order to capture experimental data and metadata in a structured form. Researchers should be able to contextualize as much as possible their requests and orchestrate their hardware according to their desired plan. Such interfaces do not exist as these tasks were at best done by populating ELN which are not suited for efficient database creation and limits greatly the exploitation of data using machine learning algorithms. To correct this, we develop a Human Computer Interface (HCI) designed to convert chemist inputs into scheduler and database language.

The documents are here : [Nextcloud/SwissCat-share/1_Projects/P9 - HCI](https://swisscatsrv1.epfl.ch/index.php/apps/files/files/101533?dir=/SwissCat-share/1_Projects/P9%20-%20HCI){: .btn .btn-blue }

The HCI then sends the corresponding workflows to the laboratory scheduler.
The laboratory scheduler then orchestrates the workflows according to the instruments state.
It is the responsibility of the scheduler to send the workflows to the appropriate instruments at the right time and with the right parameters.

The scheduler is developed in Swiss CAT+ with the help of Coteries and is available here: [Scheduler](https://github.com/swisscatplus/scheduler){: .btn .btn-blue }

Then, each machine answers the relevant orders from the scheduler. 
Depending on the machine, the way of communication and the possible actions are different. 
Each type of communication and actions is defined in the different subparts of this section.