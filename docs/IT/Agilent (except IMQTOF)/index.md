---
title:  Agilent(except IMQTOF)
layout: default
parent: IT
---

This is the  Agilent (except IMQTOF) doc for IT.

We use the Agilent Sample Scheduler to send commands to instruments.

The API to send commands to instruments are described in the repository : [API Agilent](https://github.com/swisscatplus/agilentapi){: .btn .btn-blue }

{: .important }
> Installed on srv3. 

{: .warning }
> srv3 contains also the Agilent DB. 

Instruments : LC, SFC, LC Prep, GC MS

Each instrument has an AIC (link between the instrument the network) : 5
Clients (to access the OpenLAb architecture) : 3 within the laboratory

For the central zone, one computer is used as an AIC for the GC and controls other instruments via VWORKS

We export the results in ASM format when ever possible: [ASM Modeling](https://www.allotrope.org/introduction-to-allotrope-simple-model){: .btn .btn-blue }

