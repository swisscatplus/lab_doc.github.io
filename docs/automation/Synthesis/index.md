---
title: Synthesis Area
layout: default
parent: Automation
---

# Synthesis Area  

The synthesis section is arranged in an **H-shaped layout with seven gloveboxes**, connected in series and designed to handle different stages of experiment preparation.  
All gloveboxes are sealed and filled with a **nitrogen atmosphere** to ensure inert conditions.  

- 5 gloveboxes are developed and supplied by DEC (Dietrich Engineering Consultants S.A.), who gas purification systems from Jacomex.
- 2 gloveboxes are part of the Chemspeed (Bruker) systems, which integrate glovebox hardware from MBraun.
More details are available in the extended synthesis documentation.  

*Image to insert here (H-shaped layout)*  

---

## Layout and Workflow  

- Chemicals are introduced into the system through the **Standardization Box**.  
- Standardized materials are transferred into a central **Storage Box**.  
- When an experiment is designed, powders are prepared in the **Microsampling Box** and then combined in the **Recombination Box**.  
- Experiments are executed in the **Chemspeed systems**.  

This modular design ensures that each step—entry, storage, sampling, recombination, and synthesis—is performed under controlled and reproducible conditions.  

---

## Control and Infrastructure  

- **5 DEC gloveboxes** are controlled and maintained by **five Beckhoff PLCs**, all located in a centralized electrical armory.  
- **Standardization Box PLC** also controls the **doors, airlocks and lights** of all DEC gloveboxes.  
- One PLC is dedicated to each of the following:  
  - Microsampling  
  - Storage  
  - Recombination  
  - SynthBox (not the Chemspeed units, but the linking box)  
- **2 Chemspeed gloveboxes** are controlled independently by their own controllers.  

This distributed control architecture ensures independent reliability for each glovebox, while centralizing safety and monitoring functions.  

---

## Gloveboxes in Detail  

### 1. Standardization Box  
*Image to insert here*  

- **Purpose:** Entry point for all chemicals.  
- **Design:** Internal structure developed by DEC.  
- **Process:**  
  - Operator loads liquids and solids through an airlock following an HMI instructions.  
  - Chemicals are transferred into standardized vials of **4, 20, or 30 mL** using specialized tools.  
  - Vials are grouped on SBS-format plates.  
  - Transfer to the Storage Box occurs via a cylindrical pass-throughs door.  
- **Automation:**  
  - Equipped with **2 Universal Robots (UR)** and a range of custom tools.  
  - Capabilities include:  
    - Pick-and-place of plates, containers, and vials.  
    - Loading/unloading chariots in the airlock.  
    - Transferring liquids and solids from bulk containers into standardized vials.  
- **Sealing:**  
  - Doors controlled by pneumatic actuators to ensure tight sealing.  

**Outcome:** Provides a reproducible and safe entry process, ensuring that all incoming chemicals conform to standard formats.  

---

### 2. Storage Box  
- **Purpose:** Central repository for all standardized vials and capsules.  
- **Features:**  
  - Temperature- and atmosphere-controlled.  
  - Acts as a buffer zone between gloveboxes.  
- **Outcome:** Reliable intermediate storage to support uninterrupted workflows.  

---

### 3. Microsampling Box  
- **Purpose:** Precise preparation of small-scale samples.  
- **Process:**  
  - Powders are weighed into **glass capsules (0.1–10 mg)**.  
  - Capsules are returned to the Storage Box until needed.  
- **Outcome:** Enables accurate microscale preparation for high-throughput experiments.  

---

### 4. Recombination Box  
- **Purpose:** Preparation of experiment-ready plates.  
- **Process:**  
  - Capsules are opened.  
  - Powders are dispensed into **48- or 96-well metallic SBS plates**.  
- **Outcome:** Converts individual samples into experiment-ready formats suitable for automation.  

---

### 5. Synthesis Box & Chemspeed Systems  
- **Purpose:** Final execution of designed experiments.  
- **Process:**  
  - Capsules and SBS plates are transferred into the **Chemspeed automated synthesis machines**.  
  - Machines perform automated dispensing, mixing, heating, and synthesis operations.  
- **Note:** The **Synthesis Box** is not the Chemspeed glovebox itself, but an intermediate unit linking the Recombination Box and the two Chemspeed systems.  
- **Outcome:** Automated execution of experiments, producing samples ready for analysis.  

---

## Integration with Automation  

- **Capsule Workflow** → capsules are the standardized unit for powder handling.  
- **Plate Workflow** → SBS plates bridge recombination and synthesis, enabling parallelized experiments.  
- **Chemspeed Systems** → serve as the synthesis engines, automating reaction execution.  
- **Transfer Mechanisms** → airlocks, robotic arms, and pneumatic-sealed pass-throughs ensure safe and contamination-free transfers between gloveboxes.  

---

## Summary  

The synthesis area provides a **modular, highly automated workflow**:  
1. Chemicals are introduced and standardized.  
2. Stored securely under nitrogen.  
3. Microsampled into precise capsules.  
4. Recombined into experiment plates.  
5. Processed automatically by Chemspeed systems.  

This ensures that every experiment begins from reproducible, standardized conditions and transitions seamlessly to the analytical area.  
