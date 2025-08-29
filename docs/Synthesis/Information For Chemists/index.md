---
title: Information for Chemists
layout: home
nav_order: 1
parent: Synthesis
---

# Information for Chemists

This page is written for the **synthetic chemist** interested in using **SwissCAT+** for reaction screening and optimisation.

It outlines what **SwissCAT+** can and can't do, and how to translate human procedures into automation workflows.

---

## Synthesis Capabilities

### Small-scale reactions (HTE)
- 48 or 96 well plates (2 mL or 1 mL vials)
- Shaking or magnetic stirring
- Temperature control (–20 °C to +150 °C)
- Inert atmosphere (N₂)

### Large-scale reactions (optimisation & kinetics)
- Up to 3 simultaneous reactions (max 240 mL each)
- Stirring rod
- Temperature control (–20 °C to +150 °C)
- Inert atmosphere (N₂ or Ar)
- Aliquot transfer to benchtop NMR
- IR probes

### Reactive gases (PD Reactors and Pressure Block)
- Acetylene, CO, CO₂, O₂ (max pressure: 5 bar)
- H₂ (max pressure: 80 bar)

### Transfer & manipulation
- Gravimetric powder dispensing
- Volumetric dispensing of volatile liquids and stock solutions
- Gravimetric dispensing of viscous liquids
- Silica gel filtration
- Small-scale evaporation (< 2 mL solvent)

---

## Chemical Library

- Collection of common reagents and solvents.  
- Expanding library of catalysts & ligands.  For example, **40+ commercial chiral phosphoric acids and phosphoramides** are currently available.  

---

## Automation Limitations in Synthesis

### Volatile solvents & reagents
- Limitation: open wells during dispensing leads to evaporation.  
- Compromise: add volatile liquids just before sealing; use less volatile substitutes; prefer volumetric transfer (from sealed vials) over gravimetric transfer (from open vials).  

### Reaction workup
- Limitation: biphasic extractions are not possible.  
- Compromise: use miscible solvents; use filtration only for workup.  

### Large-scale evaporation
- Limitation: evaporation of > 2 mL of solvent is not feasible in high-throughput (unless very volatile).  
- Compromise: decrease scale & increase concentration.  

### Large-scale purification
- Limitation: large-scale purification by chromatography or recrystallisation not feasible in high-throughput context.  
- Compromise: silica plug + HPLC/GC analysis for yield determination; preparative HPLC for isolation also possible for small quantities.  

---

## Automated Analysis

Preferred quantification methods for high-throughput: **HPLC, GC, SFC**.  
- Quantitative NMR (automated sample preparation: evaporation, addition of deuterated solvent, homogenisation, transfer to NMR sample tube). Only for characterization after preparatory HPLC.
- Yield determination by weight after batch purification.  

### Detection methods
- **DAD (HPLC/SFC):** Requires **chromophore** for good signal response. Analagous compounds with same chromophore give approximately the same signal intensity.
- **ELSD (HPLC/SFC):** Requires **high enough MW** for good signal response. Analagous compounds with similar MW give approximately the same signal intensity.
- **FID (GC):** Generally very flexible but limited by **volatility** of compound for GC elution. Analogous compounds with the same MW give approximately the same signal intensity.

### Internal Standards
- Improves accuracy in quantification.
- Calibration with internal standard must be done at least once prior to reaction screening.  
- The automation workflow would be modified by adding internal standard immediately after the reaction and before filtration.
- Preferred over external standards (avoids evaporation-related errors).

Properties of a good internal standard:  
- Similar chemical properties to product.  
- Inert to reaction conditions and analysis.  
- High purity and easy to source.  
- Easy to measure.

### Large product scope
- If many different substrates are being screened in a reaction study, then calibration of each possible product is impractical, especially if they are unreported. 
- Instead, approximate quantification of the products using calibration on a single representative product will be done. This approach is acceptable if variation in the products does not significantly influence signal response.

---

## Translating Human Procedures to Automation

**Example reaction procedure (homogeneous catalysis):**  
"A suspension of substrate A (1 eq, soluble powder), substrate B (1 eq, oil), catalyst (5 mol%, soluble powder) and additive (10 mol%, insoluble powder) in degassed dry solvent (1 M) was heated to 60 °C with stirring for 16 h under a N₂ atmosphere. The reaction mixture was then concentrated in vacuo and subjected to column chromatography to yield the product as a colourless solid (X% yield, Y% ee)."

**Automated workflow equivalent (e.g. solvent screening):**  

1. Prepare separate stock solutions of A, B and catalyst in DCM.  
2. Dispense solutions volumetrically into reaction vials; evaporate DCM from open vials.  
3. Add insoluble additive (powder) gravimetrically.  
4. Dispense unique solvents into vials.  
5. Seal plate and shake with heating.  
6. Cool & open plate.  
7. Add internal standard (solution) into vials; shake to homogenise.  
8. Filter precipitates with silica plug; wash 3× with HPLC solvent.  
9. Collect filtrate and dilute to calibration range.  
10. Analyse by HPLC for yield.  
11. Collect fractions corresponding to product peak; use SFC for ee determination.  

---

## Disclaimer

- Yield is, more often than not, a defining factor of success in a chemical transformation. It is very important to acknowledge that there are differences in the way a reaction is set up and analysed on an automation platform compared to a human.
- SwissCAT+ aims to minimise both **systematic** and **random** errors without sacrificing throughput. However, in the context of reaction screening, the minimisation of **random** errors is most important.
- We claim that the differences between the human procedure and the automation procedure has largely a **systematic effect** on quantitative results rather than a **random effect**.
- For a series of multiple reaction trials, the **relative differences** between quantitative results (such as yield) is the most reliable interpretation, as opposed to the **absolute values** of the results.

---

### Consultation
If you would like to discuss further about how to set up your experiments on the SwissCAT+ automation platform, do not hesitate to contact [our team](https://www.epfl.ch/research/facilities/swisscat/team/) for a consultation.
