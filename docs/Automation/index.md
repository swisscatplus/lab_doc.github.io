---
title: Automation
layout: home
nav_order: 2
has_children: true
---

# Laboratory Automation Overview  

The laboratory is designed with the long-term goal of achieving **full automation**.  
While most processes are automated, a few tasks remain manual, such as:  
- Solvent refilling  
- LC column changes  
- Maintenance  
- Consumable replenishment  

The laboratory is organized into **two main areas**:  
1. **Synthesis area** – where experiments are prepared and executed.  
2. **Analysis area** – where results are generated using advanced analytical instruments.  

---

## Synthesis Area  

The synthesis section is arranged in the form of an **H-shaped layout with seven gloveboxes**, each dedicated to a specific role.  
All gloveboxes are sealed and filled with nitrogen to ensure an inert atmosphere.  

Key gloveboxes include:  

- **Standardization Box**  
  - Entry point of the lab for the operator.  
  - Chemicals (liquids and solids) are introduced via an airlock.  
  - Transferred into standardized vials (4, 20, or 30 mL).  

- **Storage Box**  
  - Centralized repository for standardized vials and capsules.  

- **Microsampling Box**  
  - Weighs powders into small glass capsules (0.1–10 mg).  
  - Capsules are stored for later use.  

- **Recombination Box**  
  - Prepares 48- or 96-well metallic SBS plates.  
  - Dispenses the correct amount of powder from capsules.  

- **Synthesis Box & Chemspeed Systems**  
  - Capsules are opened and contents transferred into two **Chemspeed automated synthesis machines** via the Synthbox.  
  - Machines perform automated experiment execution.  

For more details, see [Synthesis](/docs/Automation/Synthesis/).  

---

Once samples leave synthesis through the **final airlock**, they enter the analysis area.  
This section is designed around **five dedicated analytical stations**, connected by a fleet of small (~20 cm) mobile robots.  

These mobile robots operate on a **transparent overhead track (2.3 m above ground)**, separated from human workflows. The track is organized into corridors linking all stations, enabling safe and autonomous sample transport.  

The **five stations** currently in operation are:  

1. **LC / SFC with MS and ELSD**  
   - First screening of all samples.  
   - Two Universal Robots (UR) arms connect three instruments.  

2. **PrepFire**  
   - Includes two Bravo liquid handlers (for concentration adjustments, evaporation, etc.), GC-MS, and a plate labeler.  
   - Linked by a KX2 SCARA robot.  

3. **OmniFire + LC-Prep**  
   - Higher-volume LC for sample preparation.  
   - OmniFire prepares plates for downstream stations or inserts them into UV or IR analyzers.  

4. **Synthesis Exit**  
   - Receives samples directly from the Chemspeed airlock.  
   - Acts as the entry point to the analysis section.  

5. **SFC-QToF + NMR**  
   - High-resolution measurements for selected samples.  
   - Two UR arms link the instruments.  

For more details, see [Analysis](/docs/Automation/Analytics/).  


---

## Sample Workflow  

The following steps illustrate the typical **life cycle of a sample** in the lab:  

1. **Entry & Standardization** – Operator introduces chemicals, standardized into vials, and stored.  
2. **Microsampling** – Powders are aliquoted into capsules and stored.  
3. **Experiment Preparation** – Capsules are opened and powders recombined into multi-well plates.  
4. **Synthesis** – Automated synthesis machines run the experiments.  
5. **Transfer** – Finished samples exit through the final airlock.  
6. **Analysis** – Mobile robots distribute samples across analytical stations. Robotic arms feed instruments.  
7. **Data Output** – Analytical results are collected and linked back to experiment design.  

