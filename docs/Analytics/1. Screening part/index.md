---
title: 1. Screening part
layout: default
parent: Analytics
---
## Purpose
- Screening all sample from synthesis with the objective of 300 samples/day.
- Detect a wide range of compound as much as possible. 

## 1. Analytical HPLC - DAD - MS (SQ) - Fraction collector (FC)/ELSD

* Image to insert here (HPLC)


**Software:** OpenLab CDS

**Purpose:** to screen all UV and non UV absorption molecules and samples. For the non-UV-absorption compound, they must be non-volatile or possibly semi-volatile.

**Design:** 8 modules. 
- Auto-sampler: sample injection, the loop is 120uL.

- Column chamber: capacity of 4 columns installation.

- LC pump (quartenary): Pressure maximum: 800 bar. 4 solvent tubes: A,B,C,D and be chosen by purpose.

- DAD (diode array detector): UV and Vis lamp. wavelength: 200-800nm. 

- MS (mass spectrometry): single-quad. No pump or make-up solvent necessary.

- ELSD (evaporative light scattering detector)

- Fraction collector: collect the interesting peak of frament based on time or volume

- Cooling system for fraction collector: can keep the temperature at 5 C in fraction collector
- Spliting valve : Valve schema and instructions are found in the link below:
.......


**Gas line**
    - ..............

**Automation and tools:**

- 2 HPLC are connected together by a 6-axe robot. See more in Automation part.

**Process:**
- The analytical process are found in the link below:.......

**Outcome:**
- Depending on screened molecules, there is DAD (UV-absorption sample), ELSD (non-volatile sample), and MS signal (ionizable sample).
- If the fraction collector is chosen, there is no ELSD signal. 
- The synthesized samples are analyzed and all compounds are separated.
- The peak detail with area, retention time and asymmetry can be found and extracted to calculate reaction yield.

## 2. SFC - DAD - MS (SQ) - ELSD
* Image to insert here (SFC)

**Software:** OpenLab CDS

**Purpose:** to separate enantiomers with chiral columns for enantiomer excess calculation.

**Design:** 7 modules

- Auto-sampler: sample injection, there is no loop here.
- Column chamber: capacity of 7 columns installation.
- SFC pump: pressure maximum: 800 bar. 2 solvent tubes: B1, B2 and be chosen by purpose. A1 is use as CO2 line as default.
- DAD (diode array detector): UV and Vis lamp. Wavelength: 200-800nm. 
- MS (mass spectrometry): single-quadrupole. No pump or make-up solvent necessary.
- ELSD (evaporative light scattering detector)
- Isopump for MS: to transfer and mix the make up solvent with sample flow before going to MS. Also 2 solvent lines can be chosen A1 and A2.
- Splitting valve: Valve schema and instruction are found in the link below ...

**Gas line:**
    - ..............

**Automation and tools:**

- Between SFC and HPLC, there is a 6-axe robot to transfer the sample. See more in Automation part.

**Process:**
- The analytical process are found in the link below:.......

**Outcome:**
- Depending on screened molecules, there is DAD (UV-absorption sample), ELSD (non-volatile sample), and MS signal (ionizable sample).
- The enantiomers are separated 100% and the enantiomer excess can be calculated based on their area peak.
- 
**3. GC - MS**
* Image to insert here

**Software:** OpenLab CDS

**Purpose:** to screen all volatile and possibly semi-volatile samples without DAD signal from HPLC screen.

**Design:** 