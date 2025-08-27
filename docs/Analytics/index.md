---
title: Analytics
layout: home
nav_order: 3
has_children: true
---
# Analytical platform
The analytical platform of the laboratory includes multiples instruments and is devided into 3 parts:

1. **Sreening step**
- 2 Analytical HPLC - DAD - MS (SQ) - Fraction collector/ELSD
- 1 SFC - DAD - MS (SQ) - ELSD
- 1 GC - MS 
2. **Sample preparation**
- Bravo
- Centrifuge
- Labeler
- Evaporator
3. **Characterization step**
- 1 Semi- Preparative HPLC
- 1 HR - UV
- 1 FTIR
- 1 NMR 300MHz
- 1 SFC - DAD - IM - QTOF

All the machines are purchased from Agilent, except NMR and FTIR are obtained from Brucker.
The series and models of all machines are found in the link below
........................
Insert an image here of analytical platform.


The analytical platform is used as a analytical service for different synthesis collaborator groups, 
external clients. Another objective is to develop a fully automnatic platform, hardware also 
software. Therefore, many projects are in progress. See more in automation.

## General analytical workflow
The general analytical workflow is found below.....
- Sample transferred by a Edy mobile from synthesis platform to Screening part.
- Analyzed by HPLC or GC to response the question: if there is a new molecule?
- If not, Yield calculation. 
- If yes, re-synthesized with higher concentration, 
- Purified by preparative LC, collected and characterized by NMR, FT-IR, UV and SFC-IM-QTOF.
- If there is chiral compound, collect from HPLC and transfer to SFC for enantiomer excess calculation.


The analytical platform is used as a service for analyzing synthesized samples 
from SwissCat+, EPFL collaborators and external clients. The second objective is to develop
a platform automated completely working including both hardware (e.g., machine - machine and 
machine - robot connection) as well as software part (e.g, automatical method selection and development,
data generation, treatment and management).

### Control and soflware
Instruments have different types of control. Their IT control is depicted in the IT section.
In general, OpenLab CDS is used for all chromatography machines (2 HPLC, 1 GC, SFC - MS (SQ)), 2 semi prep-LC),
Exceptionally, SFC - IM - QTOF is controled by MassHunter


**Purpose**: to screen and detect a wide range of compound as much as possible. 300 samples/day

**1. Analytical HPLC - DAD - MS (SQ) - Fraction collector/ELSD**

* Image to insert here (HPLC)
* Valve schema

**Software:** OpenLab CDS

**Purpose:** to screen all UV-absorption samples. For the non-UV-absorption compound, they must be non-volatile or possibly semi-volatile.

**Design:** 8 modules. They can be controlled and modified in method or directly in 
      instrument status screen.
    - Auto-sampler: sample injection, the loop is 120uL.
    - Column chamber: capacity of 4 columns installation.
    - LC pump (quartenary): Pressure maximum: 800 bar. 4 solvent tubes: A,B,C,D and be chosen by purpose.
    - DAD (diode array detector): UV and Vis lamp. wavelength: 200-800nm. 
    - MS (mass spectrometry): single-quad. No pump or make-up solvent necessary.
    - ELSD (evaporative light scattering detector)
    - Fraction collector: 
    - Cooling system for fraction collector.
  There is also a tray to put solvent bottles. 
  The outgoing fluid from column will be split passively to DAD and MS by a T-connector.
  The split ratio for instant is: 80% for DAD and 20% for MS. The ratio can be changed by 
  changing the capillary diameter and length. The longer and smaller capillary will decrease
  the flow.
  The flow from DAD will go to a valve. This valve allows us to choose which module is used next
  ELSD or fraction collector. If there is a chiral compound, fraction collector (position 6) 
  will be chosen to collect the sample into a metal tray of 96-well with 1.2mL insert. If not, 
  ELSD is chosen (position 2).

**Gas line**
    - ..............

**Automation and tools:**
    - 2 HPLC are connected together by a 6-axe robot. See more in Automation part.

**Process:**
    - Install/check column, solvent bottle level
    - Turn on all modules. Wait until it is ready (green color for each module)
    - Condition the column with acquisition method condition for at least 20 minutes.
    - Samples are put in auto-sampler by 6-axes.
    - Method running in acquisition mode. Run 1-2 blanks before samples
    - Data collection and treatment.
    - Wash the column following producer method.

**Outcome:**
    - Depending on screened molecules, there is DAD (UV-absorption sample), 
      ELSD (non-volatile sample), and MS signal (ionizable sample).
    - If the fraction collector is chosen, there is only DAD and MS signal. The position of 
      collecting samples and volume can be obtained.
    - All the acquisition method details can be found in acquisition setup.
    - Peak details can be found in Peak Details and Injection Results and extracted automatedly.
    - Calibration curve can also be done by Openlab.
    - To set a method for treatment data, going to processing method to setup. This method can be
      be saved and applied for all sequences or other sequences.

**2. SFC - DAD - MS (SQ) - ELSD**
* Image to insert here (HPLC)
* Valve schema

**Software:** OpenLab CDS

**Purpose:** to separate enantiomers with chiral columns for enantiomer calculation.

**Design:** 7 modules. They can be controlled and modified in method or directly in 
      instrument status screen.
    - Auto-sampler: sample injection, there is no loop here.
    - Column chamber: capacity of 7 columns installation.
    - SFC pump: Pressure maximum: 800 bar. 2 solvent tubes: B1, B2 and be chosen by purpose. A1 is use as CO2 line as default.
    - DAD (diode array detector): UV and Vis lamp. wavelength: 200-800nm. 
    - MS (mass spectrometry): single-quad. No pump or make-up solvent necessary.
    - ELSD (evaporative light scattering detector)
    - Isopump for MS: to transfer and mix the make up solvent with sample flow before going to MS. Also 2 solvent lines 
      can be chosen A1 and A2
  There is also a tray to put solvent bottles.  
  The outgoing fluid from column will go 100% to DAD before splitting into 2 for ELSD and MS by a T-connector.
  The split ratio for instant is: 80% for DAD and 20% for MS. The ratio can be changed by 
  changing the capillary diameter and length. The longer and smaller capillary will decrease
  the flow.

**Gas line:**
    - .........................

**Automation and tools:**
    - Between SFC and HPLC, there is a 6-axe robot to transfer the sample. See more in Automation part.

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
    - To set a method for treatment data, going to processing method to setup. This method can be
      be saved and applied for all sequences or other sequences.

**3. GC - MS**
* Image to insert here 
* Valve schema

**Software:** OpenLab CDS

**Purpose:** to screen all volatile and possibly semi-volatile samples without DAD signal from HPLC screen.

**Design:** 7 modules. They can be controlled and modified in method.

## Characterization steps
**Purpose**: to characterize in many dimension and give the information about new/unknow molecule as much as possible.
1. Semi- preparative LC - DAD - MS (SQ) 
*Image to insert here*
*Valve schema* 

**Purpose:** to separate and purify the target molecules, normally, they are the new/unknown molecules detected from screening part. 

**Design:** 7 modules. They can be controlled and modified in method or directly in 
      instrument status screen.
    - Auto-sampler: sample injection, the loop is ....uL. There is only 2 big sample tray of ... vials and can not 
      be modified by OpenLab.
    - Column chamber: capacity of 4 columns installation.
    - LC pump (quartenary): Pressure maximum: 800 bar. 4 solvent tubes: A,B,C,D and be chosen by purpose. The tube have big diameter of ....
    - DAD (diode array detector): UV and Vis lamp. wavelength: 200-800nm. 
    - MS (mass spectrometry): single-quad. No pump or make-up solvent necessary.
    - Isopump for MS: to transfer and mix the make up solvent with sample flow before going to MS. Also 2 solvent lines 
      can be chosen A1 and A2
    - Modulator: a valve to split actively a minority of flow from DAD to MS and mix the sample flow with make-up solvent.
      The split ratio can be chosen in openLab. The majority splited will go to trash.
  There is also a tray to put solvent bottles. There is no fraction collector for PrepLC. The out-going flow will be collected by OMNIFIRE.

**Gas line**
    - ..............

**Automation and tools:**
    - The sample will be installed in tray by a 6-axis, one by one due to the different size between the tray from synthesis and this one in auto-sampler.
    - The prep-LC is connected with OMNIFIRE to collect the target molecule into 96-well plate.

**Process:**
    - Install/check column, solvent bottle level, tuning mix solution. 
    - The 2L bottle should be use for mobile phase due to high flow rate of prep-LC.
    - Turn on all modules. Wait until it is ready (green color for each module).
    - Purge 4 solvent lines until all bubble air are pushed out. It can take time. Monitoring the solvent level during purge.
    - Condition the column with acquisition method condition for at least 45 minutes.
    - Samples are put in auto-sampler by 6-axis.
    - Method running in acquisition mode. Run 1-2 blanks before samples
    - Data collection and treatment.
    - Wash the column following producer method.

**Outcome:**
    - Depending on screened molecules, there is DAD (UV-absorption sample) and MS signal (ionizable sample).
    - If the MS signal is too low, the split ratio can be optimized.
    - All the acquisition method details can be found in acquisition setup.
    - Peak details can be found in Peak Details and Injection Results and extracted automatedly.
    - Calibration curve can also be done by Openlab.
    - To set a method for treatment data, going to processing method to setup. This method can be
      be saved and applied for all sequences or other sequences.

2. OMNIFIRE
3. NMR
4. FTIR
5. Multicells HR-UV
6. SFC - IM -QTOF
* Image to insert here
* Valve schema
* 
**Purpose:** one dimension of characterization. Give the information of m/z, CCS and drift time, retention time. 

**Design:** 7 modules. They can be controlled and modified in method.
    - Auto-sampler: sample injection, the loop is ....uL. There is only 2 big sample tray of ... vials and can not 
      be modified by OpenLab.
    - Column chamber: capacity of 4 columns installation.
    - LC pump (quartenary): Pressure maximum: 800 bar. 4 solvent tubes: A,B,C,D and be chosen by purpose. The tube have big diameter of ....
    - DAD (diode array detector): UV and Vis lamp. wavelength: 200-800nm. 
    - MS (mass spectrometry): single-quad. No pump or make-up solvent necessary.
    - Isopump for MS: to transfer and mix the make up solvent with sample flow before going to MS. Also 2 solvent lines 
      can be chosen A1 and A2
    - Modulator: a valve to split actively a minority of flow from DAD to MS and mix the sample flow with make-up solvent.
      The split ratio can be chosen in openLab. The majority splited will go to trash.
  There is also a tray to put solvent bottles. There is no fraction collector for PrepLC. The out-going flow will be collected by OMNIFIRE.

**Gas line**
    - ..............

**Automation and tools:**
    - The sample will be installed in tray by a 6-axis, one by one due to the different size between the tray from synthesis and this one in auto-sampler.
    - The prep-LC is connected with OMNIFIRE to collect the target molecule into 96-well plate.

**Process:**
    - Install/check column, solvent bottle level, tuning mix solution. 
    - The 2L bottle should be use for mobile phase due to high flow rate of prep-LC.
    - Turn on all modules. Wait until it is ready (green color for each module).
    - Purge 4 solvent lines until all bubble air are pushed out. It can take time. Monitoring the solvent level during purge.
    - Condition the column with acquisition method condition for at least 45 minutes.
    - Samples are put in auto-sampler by 6-axis.
    - Method running in acquisition mode. Run 1-2 blanks before samples
    - Data collection and treatment.
    - Wash the column following producer method.

**Outcome:**
    - Depending on screened molecules, there is DAD (UV-absorption sample) and MS signal (ionizable sample).
    - If the MS signal is too low, the split ratio can be optimized.
    - All the acquisition method details can be found in acquisition setup.
    - Peak details can be found in Peak Details and Injection Results and extracted automatedly.
    - Calibration curve can also be done by Openlab.
    - To set a method for treatment data, going to processing method to setup. This method can be
      be saved and applied for all sequences or other sequences.
....................................

## Sample preparation steps
1. Bravo
2. Centifuger
3. Labeler
4. Evaporator
