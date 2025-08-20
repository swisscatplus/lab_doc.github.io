---
title: Synthesis Area
layout: default
parent: Automation
---

# Synthesis Area  

The synthesis section is arranged in an **H-shaped layout with seven gloveboxes**, connected in series and designed to handle different stages of experiment preparation.  
All gloveboxes are sealed and filled with a **nitrogen atmosphere** to ensure inert conditions.  

- **5 gloveboxes** are developed and supplied by **DEC (Dietrich Engineering Consultants S.A.)**, which integrate **gas purification systems from Jacomex**.  
- **2 gloveboxes** are part of the **Chemspeed (Bruker) systems**, which integrate **glovesbox and gas purification systems from MBraun**.  
 

More details are available in the extended synthesis documentation.  

*Image to insert here (H-shaped layout)*  

---

## Layout and Workflow  

- Chemicals are introduced into the system through the **Standardization Box**.  
- Standardized materials are transferred into a central **Storage Box**.  
- When an experiment is designed, powders are prepared in the **Microsampling Box** and then combined in the **Recombination Box**.  
- Experiments are executed in the **Chemspeed systems**.  

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

## Gloveboxes in Detail  

### 1. Standardization Box  
*Image to insert here (Standardization Box)*  

- **Purpose:** Entry point for all chemicals.  
- **Design:** Internal structure developed by DEC.  
- **Process:**  
  - Operator loads liquids and solids through an airlock following HMI instructions.  
  - Chemicals are transferred into standardized vials of **4, 20, or 30 mL** using specialized tools.  
  - Vials are grouped on SBS-format plates.  
  - Transfer to the Storage Box occurs via a cylindrical pass-through door sized for SBS plates.  
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
*Image to insert here (Storage Box)*  

- **Purpose:** Central repository for all standardized vials, capsules and consumables.  
- **Design:**  
  - A **tall glovebox** with only one face equipped with gloves.  
  - The **three other faces** connect to:  
    - Standardization Box  
    - Microsampling Box  
    - Recombination Box  
  - Each connecting face includes a **pass-through door**.  
- **Interior Layout:**  
  - Three internal faces are equipped with **shelves** (storage cabinets) that contain slots for **SBS-format plates**.  
  - Provides a **large storage capacity** (**TODO: insert exact value** → **<span style="color:red">to be confirmed</span>**).  
- **Automation:**  
  - A **UR3e robot** is mounted at the center of the glovebox.  
  - Robot is placed on **two linear axes**:  
    - One for **Z movement** (vertical).  
    - One for **diagonal X movement** across the box.  
  - This configuration allows the UR3e to:  
    - Access all shelves positions.  
    - Operate each pass-through door to transfer SBS plates to neighboring gloveboxes.  
- **Electronics:**  
  - All electronics, drivers, and controllers are installed at the **bottom of the glovebox**, hidden under a protective plate cover.  

**Outcome:** Reliable, high-capacity storage and transfer hub for the sample prep workflow.  

---

### 3. Microsampling Box  
*Image to insert here (Microsampling Box)*  

- **Purpose:** Precise preparation of small-scale capsules from standardized powder vials.  
- **Design:**  
  - Same size and external form factor as the **Standardization Box**.  
  - Equipped with an **airlock** for consumables entry and exit.  
- **Automation:**  
  - Contains **two UR3e robotic arms**, each equipped with specialized end-effectors.  
  - Custom tools enable:  
    - Pick-and-place of standardized vials, microcapsules, SBS plates, and drawer.  
    - Handling of metallic capillaries used for powder transfer.  
    - Loading/unloading consumables through the airlock.  
  - Includes a **novel finger changer** developed in-house, allowing fast tool changes for different manipulation tasks.  
- **Process:**  
  1. **Input:** SBS plates containing standardized vials of powder arrive from the Storage Box.  
  2. **Sampling:**  
     - A **metallic capillary** is inserted into the powder inside a standard vial.  
     - Powder is drawn into the capillary via punching and controlled suction.  
     - The powder is deposited into a **one-way open glass capillary**.  
     - The glass capillary is cut by a **laser** to seal the microcapsule.  
  3. **Output:** Capsules (0.1–10 mg) are stored on **392-well plates**.  
  4. **Transfer:** Completed plates are returned to the Storage Box for later use.  
- **Supporting Features:**  
  - A **6-plate carousel** is positioned at the center of the box to facilitate high-throughput sampling and capsule storage.  

**Outcome:** Enables the **stochastic generation of thousands of capsules**, which are later recombined to achieve the required powder quantities for experiments. This modularized approach ensures precise dosing and reproducibility for high-throughput experimentation.  

---

### 4. Recombination Box  
*Image to insert here (Recombination Box)*  

- **Purpose:** Assembly of experiment-ready plates by recombining capsules into precise quantities of powder.  
- **Design:**  
  - The **smallest glovebox** in the synthesis area.  
  - Contains a single **UR3e robotic arm** located centrally.  
- **Automation & Tools:**  
  - The UR3e handles:  
    - Transferring SBS plates between the **Storage Box** and the **Synthesis Box**.  
    - Picking individual capsules from storage plates using a **suction gripper**.  
    - Releasing capsules directly into designated wells of metallic **48- or 96-well SBS-format plates**.  
  - A **fixed breaking tool** is installed inside the box for capsule opening.  
- **Process:**  
  1. **Input:** Plates containing capsules are received from the Storage Box.  
  2. **Placement:** The UR3e picks capsules from the capsule storage plate and releases them into the appropriate wells of the reaction plate.  
  3. **Breaking:** Once all capsules are positioned, the UR3e transfers the **entire reaction plate** into the breaking tool.  
     - The tool fractures the glass capsules inside the wells.  
     - Powder is released into the reaction vials, while the inert glass fragments remain inside without interfering with the chemistry.  
  4. **Output:** The prepared reaction plates are transferred to the Synthesis Box for further processing in the Chemspeed systems.  

**Outcome:** Provides a controlled and efficient way to recombine capsules into reaction-ready plates, ensuring reproducibility, throughput, and compatibility with downstream automated synthesis.  



---

### 5. SynthBox
*Image to insert here (SynthBox)*  

- **Purpose:** Acts as the **interface between the Recombination Box and the Chemspeed systems**, handling experiment plates before and after automated synthesis.  
- **Design:**  
  - Similar in size to the **Storage Box**, positioned on the opposite side of the H-bar.  
  - Only one face has glove ports for manual intervention.  
  - Equipped with three pass-through doors:  
    - One to the **Recombination Box**.  
    - One to each of the two **Chemspeed systems** (one per side).  
- **Automation & Tools:**  
  - A central robotic arm manipulates metallic SBS-format plates used for reactions.  
  - The arm is equipped with multiple interchangeable tools enabling:  
    - **Plate transfer** between Recombination, Chemspeed, and back.  
    - **Opening and closing reaction plate covers**, which are secured by **four screws**.  
    - **Replacing the protective plastic film** between experiments to prevent cross-contamination.  
    - **Replacing the plate seal** when it has been pierced or degraded by repeated operations.  
  - In addition, the arm can be fitted with **automated pipettes**, which can be mounted/dismounted as end-effectors, enabling liquid handling operations directly inside the box.  
- **Process:**  
  1. **Input:** Reaction plates arrive from the Recombination Box.  
  2. **Preparation:** The SynthBox robot:  
     - Opens the reaction plate covers (removing screws).  
     - Replaces seals or protective films if required.  
  3. **Transfer to Chemspeed:** Prepared plates are moved to one of the two Chemspeed gloveboxes for automated synthesis.  
  4. **Post-processing:** After synthesis, the plates return to the SynthBox, where the robot:  
     - Closes the covers with screws.  
     - Replaces films or seals as necessary.  
  5. **Output:** Plates are either returned to the workflow or prepared for transfer to analysis.  

**Outcome:** The SynthBox ensures reliable preparation, sealing, and maintenance of reaction plates, providing a seamless and contamination-free link between recombination and Chemspeed automated synthesis.  

---

## Summary  

The synthesis area provides a **modular, highly automated workflow**:  
1. Chemicals are introduced and standardized.  
2. Stored securely under nitrogen.  
3. Microsampled into precise capsules.  
4. Recombined into experiment plates.  
5. Processed automatically by Chemspeed systems.  

This ensures that every experiment begins from reproducible, standardized conditions and transitions seamlessly to the analytical area.  
