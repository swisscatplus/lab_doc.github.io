---
title: Automation Tools
layout: home
parent: Synthesis
---
# Chemspeed Tools Overview

This page introduces the main **Chemspeed tools** integrated into the **Swing SP**, **CatScreen**, and **AutoPlant** platforms.  
Each section contains: description, key features, applications, technical specifications, and image placeholders.  
Reference videos with demonstrations can be found here: [Chemspeed Example Solutions](https://www.chemspeed.com/example-solutions/)

---

## 1. 4NH

**Description:**  
Automated liquid handling tool designed for accurate dispensing of solvents and reagents into vials or Paradox plates.

**Key Features:**  
- Four independent dispensing heads.  
- High repeatability and precision across multiple vials.  
- Supports both small and medium volume dispensing.  

**Applications:**  
- Parallel synthesis.  
- Distribution of solvents or stock solutions.  
- Integration into HTE workflows.  

**Technical Specifications (typical):**  
- Dispensing precision: ±1–2%.  
- Volume range: 100 µL to 25 mL (according to 1, 10 or 25 ml syringe volume).  

<!-- Image: 4NH dispensing head -->
![4NH](./../../../assets/images/4nh.png)

**Platforms:** Swing SP, CatScreen, AutoPlant  

---

## 2. GDU PfD (Gravimetric Dispensing Unit – Powder Fine Dosing)

**Description:**  
High-precision solid dispensing unit capable of handling powders using a **two-step principle**:  
- **Rough dosing:** delivers bulk material quickly.  
- **Fine dosing:** uses vibration or controlled feed to achieve precise target mass.

**Key Features:**  
- Accurate dosing of solid reagents without manual intervention.  
- Integrated balance for real-time feedback.  
- Ensures reproducibility across batches.  

**Applications:**  
- Catalyst or ligand screening.  
- Weighing powders for reaction plates.  
- Automated library preparation.  

**Technical Specifications (typical):**  
- Dosing accuracy: < 1 mg.  
- Capacity: from a few mg up to several grams.  

<!-- Image: GDU PFD unit -->
![GDU PFD](./../../../assets/images/gdupfd.png)

**Platforms:** Swing SP, CatScreen, AutoPlant  

---

## 3. GDU-V (Volumetric Dispensing Unit)

**Description:**  
Gravimetric dosing module optimized for viscous or liquid reagents where gravimetric control is not required.

**Key Features:**  
- High throughput liquid dispensing.  
- Suitable for non-volatile solvents and oils.  
- Compact and robust design.  

**Applications:**  
- Addition of solvents or liquid additives.  
- Screening workflows with repetitive dosing.  

**Technical Specifications (typical):**  
- Precision: ±2–3%.  
- Volume range: 10 µL – 5 mL.  

<!-- Image: GDU-V unit -->
![GDU-V](./../../../assets/images/gduv.png)

**Platforms:** Swing SP, CatScreen, AutoPlant  

---
# GDU – Principle of Operation

The **Gravimetric Dispensing Unit (GDU)** is an automated dosing system that combines a **dispensing mechanism**, an **analytical balance**, and a **real-time control algorithm** to achieve highly accurate additions of solids or liquids.

<!-- Image: GDU overview -->
![GDU Overview](./../../../assets/images/gdu_overview.png)

---

## Core Concept (Closed-Loop Control)

- **Dispensing element** (e.g., screw feeder, vibrating chute, syringe/piston);
- **Analytical balance** under the receiving vessel for continuous mass read-out;
- **Controller** that transitions from **rough dosing** to **fine dosing** near the target;
- Constant logging for **traceability** (target, actual, tolerance, timestamp).

---

## GDU PFD – Powder Fine Dosing

**Principle:**  
Two-stage gravimetric dosing:
1. **Rough dosing** – fast bulk transfer to approach the setpoint quickly.  
2. **Fine dosing** – reduced feed/vibration for milligram-level accuracy, stopping exactly at target mass via balance feedback.

- Stable, repeatable dosing of micro- to gram-scale solids;
- Minimized operator influence; fully automated cycles;


**Typical Performance:**
- Accuracy: **< 1 mg** (depending on material flowability and setup);
- Working range: **few mg → several g**.

---

## GDU-V / GDU-L – Volumetric & Liquid Dosing

**Principle:**  
Volumetric displacement (syringe/piston). Optional balance feedback can be used to correct for density or temperature effects when needed.

**Key Points (Liquids/Viscous):**
- High-throughput liquid additions with consistent volumes.
- Compatible with a wide viscosity range and many solvents.
- Integrates with plate/vial workflows for HTE.

**Typical Performance (indicative):**
- Precision: **±1–2%**.
- Volume range: **10 µL → several mL**.

---

## 4. PD Reactors and PD Module (240 mL)

**Description:**  
Large-volume **Process Development (PD) reactors** for optimization and kinetic studies. Integrated into the AutoPlant for scale-up.

**Key Features:**  
- Reactor volume: 240 mL.  
- Parallel operation in up to 3 PD reactors.  
- Integrated stirring, heating, cooling, and pressurization.  
- Direct coupling with analytical instruments.  

**Applications:**  
- Kinetic studies.  
- Reaction scale-up after screening.  
- Process optimization under controlled conditions.  

**Technical Specifications (typical):**  
- Volume range: up to 200 mL effective scale-up.  
- Temperature: –20 °C to +150 °C.  
- Pressure: up to 80 bar.  

<!-- Image: PD reactors -->
![PD Reactors](./../../../assets/images/pdreactor.png)

**Platforms:** AutoPlant (dedicated)  

---

## 5. Gripper MTP / Eccentric Gripper

**Description:**  
Robotic handling tools for manipulating Paradox plates, vials, or reaction blocks.

**Key Features:**  
- MTP gripper for Paradox and MTP plates.  
- Eccentric gripper for non-standard geometries.  
- Automated transfer between modules.  

**Applications:**  
- Plate handling in HTE workflows.  
- Loading/unloading blocks in synthesis systems.  

**Technical Specifications (typical):**  
- Handling capacity: up to several kg.  
- Repeatability: ±0.1 mm positioning.  

<!-- Image: Gripper MTP -->
![Gripper](./../../../assets/images/gripper.png)

**Platforms:** Swing SP, CatScreen, AutoPlant  

---

## 6. Heating Plate / Shaker

**Description:**  
Combined heating and agitation system for reaction plates and vials.  
Uses **electrical heating (Heether Shinko)** and **oil-based cooling (cryostat)**.

**Key Features:**  
- Independent control of temperature and shaking speed.  
- Uniform heating across all wells.  
- Cooling through integrated cryostat loop.  

**Applications:**  
- Parallel reactions requiring heating/cooling.  
- Mixing of viscous solutions.  
- Thermal control during catalysis experiments.  

**Technical Specifications (typical):**  
- Temperature range: –20 °C to +150 °C.  
- Shaking speed: 100–800 rpm.  


**Platforms:** Swing SP, CatScreen, AutoPlant  

---

## 7. MTP Pressure Block

**Description:**  
Specialized reactor block for parallel reactions under controlled pressure.  
Compatible with 48- and 96-well Paradox or MTP plates.

**Key Features:**  
- Allows gas pressurization of entire reaction plate.  
- Uniform distribution of pressure.  
- Safety interlocks for overpressure.  

**Applications:**  
- High-throughput catalysis under H₂ or other gases.  
- Screening of homogeneous catalytic reactions.  

**Technical Specifications (typical):**  
- Pressure: up to 80 bar.  
- Temperature: ambient to 150 °C (with heating plate).  

<!-- Image: MTP Pressure Block -->
![MTP Pressure Block](./../../../assets/images/pressure_block.png)

**Platforms:**  CatScreen  

---