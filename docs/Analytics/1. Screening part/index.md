---
title: 1. Screening part
layout: default
parent: Analytics
---
## Purpose
- Screening all sample from synthesis with the objective of 300 samples/day.
- Detect a wide range of compound as much as possible. 

## 1. Analytical HPLC - DAD - MS (SQ) - Fraction collector (FC)/ELSD**

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

- If the fraction collector is chosen, there is no ELSD signal. The position of collecting samples and volume can be obtained from data processing in OpenLabs.
- All the acquisition method details can be found in acquisition setup.
- Peak details can be found in Peak Details and Injection Results and extracted automatedly.
- Calibration curve can also be done by Openlab.
- To set a method for treatment data, going to processing method to setup. This method can be saved and applied for all sequences or other sequences.

**2. SFC - DAD - MS (SQ) - ELSD**
* Image to insert here (HPLC)
* Valve schema

**Software:** OpenLab CDS

**Purpose:** to separate enantiomers with chiral columns for enantiomer calculation.

**Design:** 7 modules. They can be controlled and modified in method or directly in instrument status screen.

- Auto-sampler: sample injection, there is no loop here.

- Column chamber: capacity of 7 columns installation.
- SFC pump: Pressure maximum: 800 bar. 2 solvent tubes: B1, B2 and be chosen by purpose. A1 is use as CO2 line as default.
- DAD (diode array detector): UV and Vis lamp. wavelength: 200-800nm. 
- MS (mass spectrometry): single-quad. No pump or make-up solvent necessary.
- ELSD (evaporative light scattering detector)
- Isopump for MS: to transfer and mix the make up solvent with sample flow before going to MS. Also 2 solvent lines can be chosen A1 and A2.

There is also a tray to put solvent bottles.  
The outgoing fluid from column will go 100% to DAD before splitting into 2 for ELSD and MS by a T-connector. The split ratio for instant is: 80% for DAD and 20% for MS. The ratio can be changed by 
changing the capillary diameter and length. The longer and smaller capillary will decrease
the flow.

**Gas line:**
    - ..............

**Automation and tools:**

- Between SFC and HPLC, there is a 6-axe robot to transfer the sample. See more in Automation part.
- 
**Process:**

- Install/check column, solvent bottle level
- Turn on all modules. Wait until it is ready (green color for each module)
- Check if there is bubble air in SFC pump and Isopump. If yes, open the valve and purge the solvent tubes.
- Put the flow rate to maximum 5mL/min with 100% MeOH and purge in 3-5 minutes. For purging, the SFC should be turned off.
- Then, decrease the flow rate to normal, 1mL/min for SFC pump and 0.5mL/min for Isopump before closing the valve.
- Condition the column at least 20 minutes before using
- Samples are put in auto-sampler by 6-axes.
- Method running in acquisition mode. The column screening is necessary to find out the best column for chiral separation.
- Data collection and treatment.
- Wash the column following producer method.

**Outcome:**
- Depending on screened molecules, there is DAD (UV-absorption sample), ELSD (non-volatile sample), and MS signal (ionizable sample).
- All the acquisition method details can be found in acquisition setup.
- Peak details can be found in Peak Details and Injection Results and extracted automatedly.
- Calibration curve can also be done by Openlab.
- To set a method for treatment data, going to processing method to setup. This method can be saved and applied for all sequences or other sequences.
- 
**3. GC - MS**
* Image to insert here 
* Valve schema

**Software:** OpenLab CDS

**Purpose:** to screen all volatile and possibly semi-volatile samples without DAD signal from HPLC screen.

**Design:** 