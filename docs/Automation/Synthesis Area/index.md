---
title: Synthesis Area
layout: default
parent: Automation
---

# Synthesis Area  

The synthesis section is arranged in an **H-shaped layout with seven gloveboxes**, connected in series and designed to handle different stages of experiment preparation.  
All gloveboxes are sealed and filled with a **nitrogen atmosphere** to ensure inert conditions.  

The **H-shaped structure has four external airlocks**, located at the ends of each branch of the H.  
These airlocks provide controlled entry and exit points between the glovebox network and the outside environment, allowing the transfer of consumables, chemicals, and samples without breaking the inert atmosphere.  

- **Five gloveboxes** are developed and supplied by **DEC (Dietrich Engineering Consultants S.A.)**, which integrate **gas purification systems from Jacomex**.  
- **Two gloveboxes** are part of the **Chemspeed (Bruker) systems**, which integrate **gloveboxes and gas purification systems from MBraun**.  

More details on the chemical synthesis operations are available in the dedicated [ Synthesis documentation ](/synthesis/).  

*Image to insert here (H-shaped layout)*  

---

## Layout and Workflow  

- Chemicals are introduced into the system through the **Standardization Box**.
- Standardized materials are transferred into a central **Storage Box**.  
- When an experiment is designed, powders are prepared in the **Microsampling Box** and then combined in the **Recombination Box**.  
- Plates are conditioned in the **SynthBox** and then executed in the **Chemspeed systems**, where the synthesis occurs.  

This modular design ensures that each step — entry, storage, sampling, recombination, and synthesis — is performed under controlled and reproducible conditions.  

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

## General Characteristics of DEC Gloveboxes  

The five DEC gloveboxes (Standardization, Storage, Microsampling, Recombination, SynthBox) share a set of common features:  

- **Sealed Atmosphere:** Maintained under nitrogen to ensure inert conditions.  
- **Airlocks:** Two box are equipped with an airlock to transfer consumables, plates, or samples.  
- **Pass-through Doors:** Connections between gloveboxes use pneumatically actuated doors sized for SBS-format plates.  
- **Pneumatic Actuators:** All doors are pneumatically actuated to ensure tight sealing.  
- **Automation:** Each glovebox integrates collaborative **UR robotic arms** with custom tools, optimized for its specific task.  
- **Control:** Each box is operated by a **dedicated Beckhoff PLC**, with centralized monitoring in the armory.  

These shared features ensure modularity and reliability, while each glovebox adds unique functions.  

---

## Gloveboxes in Detail  

### 1. Standardization Box  
*Image to insert here (Standardization Box)*  

- **Purpose:** Entry point for all chemicals.  
- **Design:**  
  - Similar size to Microsampling Box.  
  - Equipped with an **airlock** for chemicals bottles and consumables entry/exit.  
  - Direct connection to the Storage Box via pass-through door.  
- **Automation & Tools:**  
  - Equipped with **2 Universal Robots (UR3e)** and a range of specialized tools.  
  - Capabilities:  
    - Pick-and-place of plates, bottles, and standardized vials.  
    - Loading/unloading drawer in the airlock.  
    - Transferring liquids and solids from bottles into standardized vials.  
- **Process:**  
  1. Operator introduces chemicals bottles through the airlock, guided by HMI instructions.  
  2. Chemicals are transferred into standardized vials of **4, 20, or 30 mL**.  
  3. Vials are grouped on SBS-format plates.  
  4. Plates are sent to the Storage Box.  
- **Outcome:** Provides a reproducible, automated entry workflow ensuring all chemicals are converted into standardized formats.  

---

### 2. Storage Box  
*Image to insert here (Storage Box)*  

- **Purpose:** Central repository for standardized vials, capsules and consumables.  
- **Design:**  
  - **Tall glovebox** with one glove face.  
  - Other three faces connect to: Standardization, Microsampling, and Recombination.  
  - Interior fitted with **shelves** for SBS-format plates.  
  - Large storage capacity (**<span style="color:red">size to be confirmed</span>**).  
- **Automation & Tools:**  
  - **UR3e robot** mounted on two linear axes: Z (vertical) + diagonal X (across box).  
  - Provides access to shelves and doors.  
- **Electronics:** Controllers and drivers located under a base plate cover.  
- **Process:**  
  1. Receives standardized vials or capsule plates.  
  2. Stores them until required.  
  3. Transfers plates to Microsampling or Recombination as needed.  
- **Outcome:** Acts as a high-capacity buffer, ensuring smooth flow of samples between preparation steps.  

---

### 3. Microsampling Box  
*Image to insert here (Microsampling Box)*  

- **Purpose:** Creation of microcapsules from standardized powder vials.  
- **Design:**  
  - Same size as Standardization Box.  
  - Equipped with an **airlock** for consumables.  
  - Contains a **6-plate carousel** for increase throughput.  
- **Automation & Tools:**  
  - Two **UR3e arms** with custom end-effectors.  
  - Tools allow:  
    - Handling of vials, capsules, SBS plates, and drawer.  
    - Metallic capillary sampling.  
    - Fast tool changes via a **custom finger changer** developed in-house.  
- **Process:**  
  1. Standardized vials arrive from Storage.  
  2. Metallic capillary inserted into powder; suction extracts material.  
  3. Powder transferred into a **one-way glass capillary**.  
  4. Laser cutting seals the capsule (0.1–10 mg).  
  5. Capsules stored on **392-well plates**.  
  6. Plates returned to Storage.  
- **Outcome:** Produces thousands of microcapsules, enabling reproducible recombination of powders for future experiments.  

---

### 4. Recombination Box  
*Image to insert here (Recombination Box)*  

- **Purpose:** Recombine microcapsules into reaction-ready plates.  
- **Design:**  
  - Smallest glovebox in the synthesis area.  
  - Contains one **UR3e robot**.  
- **Automation & Tools:**  
  - Suction gripper for capsule handling.  
  - **Fixed breaking tool** for capsule opening.  
- **Process:**  
  1. Capsule plates arrive from Storage.  
  2. UR3e places capsules into wells of metallic **48- or 96-well plates**.  
  3. Complete reaction plate transferred into breaking tool.  
  4. Capsules fractured simultaneously; powders released into wells.  
  5. Plates passed to SynthBox.  
- **Outcome:** Enables precise recombination of capsules into experiment-ready plates.  

---

### 5. SynthBox (not Chemspeed)  
*Image to insert here (SynthBox)*  

- **Purpose:** Interface between Recombination and Chemspeed systems.  
- **Design:**  
  - Similar size to Storage Box.  
  - One glove face, three pass-through doors (Recombination, Chemspeed left, Chemspeed right).  
- **Automation & Tools:**  
  - One **UR5e robot** with multiple tools:  
    - Plate transfer.  
    - Opening/closing covers (4 screws).  
    - Replacing protective films.  
    - Replacing plate seals.  
    - Mounting automated pipettes for liquid handling.  
- **Process:**  
  1. Plates arrive from Recombination.  
  2. UR5e prepares plates (opens, refreshes film/seal).  
  3. Plates transferred to Chemspeed.  
  4. After synthesis, UR5e reseals plates.  
  5. Plates exit to workflow/analysis.  
- **Outcome:** Ensures reaction plates are sealed, refreshed, and properly prepared for synthesis and beyond.  

---

### 6. Chemspeed Systems  
*Image to insert here (Chemspeed Systems)*  

- **Purpose:** Automated synthesis execution.  
- **Design:**  
  - Two Chemspeed systems, each integrated into MBraun gloveboxes.  
  - Connected directly to SynthBox.  
- **Automation & Tools:**  
  - Automated liquid handling, mixing, heating, and synthesis.  
  - Robotic control of reaction workflows.  
- **Process:**  
  - Plates arrive from SynthBox.  
  - Synthesis protocols executed automatically.  
  - Plates returned to SynthBox after completion.  
- **Outcome:** Core units where chemical synthesis is performed.  

👉 For chemical workflows, see [Synthesis documentation](../synthesis.md).  

---

## Summary  

The synthesis area provides a **modular, highly automated workflow**:  
1. Chemicals are introduced and standardized.  
2. Stored securely under nitrogen.  
3. Microsampled into precise capsules.  
4. Recombined into experiment plates.  
5. Prepared in SynthBox and executed in Chemspeed.  
6. Transitioned to the analytical area.  

This ensures every experiment starts from standardized, reproducible conditions.  
