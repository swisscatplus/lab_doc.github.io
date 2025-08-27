---
title: Information for Chemists
layout: home
nav_order: 1
parent: Synthesis
---

# Information for Chemists

This page is written for the **synthetic chemist** interested in using **SwissCAT+** for reaction screening and optimisation.  
It outlines synthesis capabilities, chemical library, limitations, analytical methods, and how to translate human procedures into automation workflows.

---

## Synthesis Capabilities

### Small-scale reactions (HTE)
- 48 or 96 well plates (2 mL or 1 mL vials)
- Shaking or magnetic stirring
- Temperature control (–20 °C to +150 °C)
- Inert atmosphere (N₂ or Ar)

### Large-scale reactions (optimisation & kinetics)
- Up to 3 simultaneous reactions (max 240 mL each)
- Stirring rod
- Temperature control (–20 °C to +150 °C)
- Inert atmosphere (N₂ or Ar)
- Aliquot transfer to benchtop NMR
- Infrared probes

### Reactive gases
- Acetylene, CO, CO₂, O₂ (≤ 5 bar)
- H₂ (≤ 80 bar)

### Transfer & manipulation
- Gravimetric powder dispensing
- Volumetric dispensing of volatile liquids and stock solutions
- Gravimetric dispensing of viscous liquids
- Silica gel filtration
- Small-scale evaporation (< 2 mL solvent)

---

## Chemical Library

- Collection of common reagents.  
- Expanding library of catalysts & ligands.  
- 40+ commercial **chiral phosphoric acids and phosphoramides** available for screening.  

---

## Automation Limitations in Synthesis

### Volatile solvents & reagents
- Limitation: open wells during dispensing → evaporation.  
- Compromise: add volatile liquids just before sealing; use substitutes; prefer volumetric transfer.  

### Reaction workup
- Limitation: biphasic extractions not possible.  
- Compromise: use miscible solvents; filtration only.  

### Large-scale evaporation
- Limitation: > 2 mL not feasible in high-throughput.  
- Compromise: decrease scale & increase concentration.  

### Large-scale purification
- Limitation: purification not feasible at scale.  
- Compromise: silica plug + HPLC/GC analysis; preparative HPLC for isolation if required.  

---

## Automated Analysis

Preferred: **HPLC, GC, SFC**.  
- Quantitative NMR discouraged (requires complex prep).  
- Chromatographic purification for weighing discouraged.  

### Detection methods
- **DAD (HPLC/SFC):** requires chromophore; analogues comparable.  
- **ELSD (HPLC/SFC):** requires sufficient MW; analogues comparable.  
- **FID (GC):** analogues comparable by MW.  

### Internal Standards
- Improves accuracy; calibration before screening.  
- Add internal standard immediately after reaction.  
- Preferred over external standards (avoids evaporation errors).  

A good internal standard:  
- Similar chemical properties to product.  
- Inert to conditions and analysis.  
- High purity, easy to source.  
- Easy to quantify.

### Large product scope
- Full calibration impractical.  
- Approximate quantification using **analogous calibration compound** acceptable.  

---

## Translating Human Procedures to Automation

**Example reaction (homogeneous catalysis):**  
Substrate A (powder), Substrate B (oil), Catalyst (5 mol%), Additive (10 mol%, insoluble powder) in dry solvent, stirred at 60 °C under N₂ for 16 h. Workup by evaporation + column chromatography.

**Automated workflow equivalent:**  
1. Prepare stock solutions of A, B, Catalyst in DCM.  
2. Dispense solutions volumetrically into vials; evaporate DCM.  
3. Add insoluble additive gravimetrically.  
4. Dispense solvents into vials.  
5. Seal plate → shake with heating.  
6. Cool & open plate.  
7. Add internal standard (solution) → shake to homogenise.  
8. Filter with silica plug; wash 3×.  
9. Collect filtrate, dilute to calibration range.  
10. Analyse by HPLC for yield.  
11. Collect fractions; use SFC for ee determination.  

---

## Disclaimer

- Yields differ between manual and automated procedures.  
- SwissCAT+ minimises random errors, but systematic deviations remain.  
- **Relative results (e.g., yield trends across experiments) are reliable.**  
- **Absolute yield values** may differ from conventional manual experiments.  

### Consultation

If you would like to discuss further about how to set up your experiments on the SwissCAT+ automation platform, do not hesitate to contact [our team](/docs/Organisation/) for a consultation.
