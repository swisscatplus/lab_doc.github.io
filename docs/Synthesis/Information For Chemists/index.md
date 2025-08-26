---
title: Information for Chemists
layout: home
nav_order: 1
parent: Synthesis
---

<img src="/assets/images/logo.png" alt="SwissCAT+ Logo" width="20%">

# Information for Chemists
The following is written for the general synthetic chemist who is interested in using SwissCAT+ for reaction screening and optimisation.

### Synthesis capabilities

**Small scale reactions for high-throughput screening**
- 48 or 96 well plates (up to 2 mL or 1 mL per reaction vial)
- Shaking or magnetic stirring
- Temperature control (–20 °C to +150 °C)
- Inert atmosphere (N<sub>2</sub> or Ar)

**Large scale reactions for optimisation and kinetics**
- Up to 3 simultaneous reactions of max. volume 240 mL
- Stirring rod
- Temperature control (–20 °C to +150 °C)
- Inert atmosphere (N<sub>2</sub> or Ar)
- Aliquot transfer to benchtop NMR
- Infrared probes

**Reactive gases (small and large scale)**
- Acetylene (max 5 bar)
- CO (max 5 bar)
- CO<sub>2</sub> (max 5 bar)
- H<sub>2</sub> (max 80 bar)
- O<sub>2</sub> (max 5 bar)

**Transfer and manipulation**
- Dispensing powders gravimetrically
- Dispensing volatile liquids and stock solutions volumetrically
- Dispensing viscous liquids gravimetrically
- Silica gel filtration
- Evaporating small volumes (< 2mL) of solvent

For more technical information of the dispensing tools and reactors, please see [Automation Tools](/docs/Synthesis/Automation%20Tools/).  

### Chemical library

We have a collection of common reagents and an expanding library of catalysts and ligands. For example, we have **40+ commercial chiral phosphoric acids and phosphoramides** that can be screened on demand in a variety of synthetic applications. 

### Automation limitations in synthesis

**Volatile solvents and reagents**

Limitation:
- The 48/96 well plates must be fully open while solids and liquids are being dispensed into it. During this period, volatile liquids in the reaction vials can evaporate.
- Once stock vials have been aspirated from with a needle, the pierced septa can leak volatile liquids, leading to increase in concentrations over time if left for long periods (> 24 h).

Compromise:
- Add volatile liquids just before sealing the 48/96 well plates.
- Use less volatile substitutes.
- Favour the use of volumetric transfer (by needle from closed vial) rather than gravimetric transfer (from open vial).

**Reaction workup**

Limitation:
- The platform is not capable of performing biphasic extractions.

Compromise:
- Use miscible solvents only.
- Use filtration to remove unwanted precipitates.

**Large-scale evaporation**

Limitation:
- Evaporating large quantities of solvent (> 2 mL) cannot be done feasibly on our workstation in a high-throughput context.

Compromise:
- Decrease scale and increase concentration of reactions.

**Large-scale purification**

Limitation:
- Purifying large quantities of compound cannot be done feasibly in high throughput.

Compromise:
- Use silica filtration only for the removal of insoluble impurities. Then, use robust analysis techniques of crude reaction mixtures such as HPLC or GC to determine yield.
- If necessary to isolate pure components for analysis, use fraction collection from preparatory HPLC or analytical HPLC.

### Automated analysis

The chromatographic techniques (HPLC, GC and SFC) are preferred for quantification of organic compounds. While humans routinely use quantitative NMR with internal standard, this technique cannot be easily applied in an automation context due to the extra manipulations of the sample required (evaporation, addition of deuterated solvent, homogenisation and transfer to NMR sample tube). Likewise, chromatographic purification for the sole purpose of determining product yield by weight is discouraged on our platform for similar reasons.

**Detection methods for quantification**
- **DAD** (HPLC/SFC). Requires a chromophore for good signal response. Analagous compounds with the same chromophore give approximately the same signal intensity.
- **ELSD** (HPLC/SFC). Requires a high enough molecular weight for good signal response. Analogous compounds with the same molecular weight give approximately the same signal intensity.
- **FID** (GC). Analogous compounds with the same molecular weight give approximately the same signal intensity.

**Internal standard**
To improve accuracy in quantification, we would typically use an internal standard, meaning that before screening, calibration with internal standard would be done at least once. Then, after the heating/stirring of a reaction is finished, the internal standard would be immediately added.

Compared to external standards, use of internal standards is preferred due to the possibility of solvent evaporation and material loss during the filtration process.

A good internal standard:
- has similar chemical properties to the product.
- is chemically inert to the reaction conditions and analysis method.
- is easily sourced in high purity.
- is easily measured.

**Quantification of a large product scope**
If many different substrates are being screened in a reaction study, then calibration of each possible product is impractical, especially if they are unreported. Instead, approximate quantification of the products using calibration on a single analogous compound will be done. This approach is valid, provided the detection technique is appropriate and the variation in the products does not significantly influence signal response.

For more detail on our analytical tools, see [Analytics](/docs/Analytics/).  

### Translating a human procedure to an automation workflow

A typical reaction procedure for a homogeneous catalysis reaction may be of the following:

"A suspension of substrate A (1 eq, soluble powder), substrate B (1 eq, oil), catalyst (5 mol%, soluble powder) and additive (10 mol%, insoluble powder) in degassed dry solvent (1 M) was heated to 60 °C with stirring for 16 h under a N<sub>2</sub> atmosphere. The reaction mixture was then concentrated in vacuo and subjected to column chromatography to yield the product as a colourless solid (X% yield, Y% ee)."

Suppose it is desired to screen solvents to optimise yield and enantioselectivity. We might use the following workflow to carry out this screening on our platform:

1. Prepare stock solutions of substrate A, substrate B and catalyst in DCM.
2. In each reaction vial, dispense volumetrically the required amount of each stock solution. Allow the DCM to fully evaporate on standing.
3. In each reaction vial, dispense the insoluble additive gravimetrically in powder form.
4. Dispense the unique solvents into each corresponding vial.
5. Seal the plate containing the reaction vials and shake with heating for the desired duration.
6. Cool and open plate.
7. In each reaction vial, dispense the internal standard as stock solution. Shake to homogenise.
8. Filter out insoluble impurities with a short silica plug, washing with HPLC-grade solvent three times.
9. Transfer collected filtrate to HPLC vials, diluting the sample to a concentration within calibration range.
10. Transfer to HPLC and determine yield from peak area comparison of product and internal standard.
11. Collect fractions corresponding to product peak and transfer to SFC for enantiomeric excess determination.

### Important Disclaimer
Yield is, more often than not, a defining factor of success in a chemical transformation. It is very important to acknowledge that there are differences in the way a reaction is set up and analysed on an automation platform compared to a human. 

SwissCAT+ aims to minimise both **systematic** and **random** errors without sacrificing throughput. However, in the context of reaction screening, the minimisation of **random** errors is most important.

We claim that the differences between the human procedure and the automation procedure has largely a **systematic** effect on quantitative results rather than a **random** effect.

In other words, for a series of multiple reaction trials, the **relative differences** between quantitative results (such as yield) is the most reliable interpretation, as opposed to the **absolute values** of the results.

### Consultation

If you would like to discuss further about how to set up your experiments on the SwissCAT+ automation platform, do not hesitate to contact [our team](/docs/Organisation/) for a consultation.

Written by Dr. Young Sebastian Ye, 2025.