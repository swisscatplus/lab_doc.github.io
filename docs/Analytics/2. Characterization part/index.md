---
title: 2. Characterization part
layout: default
parent: Analytics
---
**Purpose**: to characterize in diverse dimensions and give the information about new/unknown molecule as much as possible.
**1. Semi- preparative LC - DAD - MS (SQ)**

*Image to insert here*

*Valve schema* 

**Purpose:** to separate and purify the target molecules, normally, they are the new/unknown molecules detected from screening part. The sample is synthesized second time in high concentration.
The capacity of semi-prepLC is : ....

**Design:** 7 modules. They can be controlled and modified in method or directly in instrument status screen.

- Auto-sampler: sample injection, the loop is ....uL. There is 2 big sample trays of 66 vials in default and can not be modified by OpenLab CDS.

- Column chamber: capacity of 6 columns installation (3 on left side and 3 on right side). But only 2 - 4 columns can be installed at same time since the column is too big for the support. 

- LC pump (quartenary): Pressure maximum: 800 bar. 4 solvent tubes: A,B,C,D and be chosen by purpose. The tube have big diameter of ....

- DAD (diode array detector): UV and Vis lamp. wavelength: 200-800nm. 

- MS (mass spectrometry): single-quad.

- Isopump for MS: to transfer and mix the make - up solvent with sample flow before going to MS. 2 solvent lines can be chosen A1 and A2. Small tube: ...mm

- Flow modulator: a valve to split actively a minority of flow from DAD to MS and mix the sample flow with make-up solvent. The split ratio can be selected in openLab. The majority of splited flow will go to trash.

There is also a tray to put solvent bottles. There is no fraction collector for PrepLC. The out-going flow will be collected by OMNIFIRE.

**Gas line**
- ..............

**Automation and tools:**

- The sample will be installed in tray by a 6-axis, one by one due to the different size between the tray from synthesis and this one in auto-sampler.

- The prep-LC is connected with OMNIFIRE to collect the target molecule into 96-well plate.

**Mobile phase and column**
- Mobile phase: A. 1L H2O + 0.05% acetic acid ; B. 900mL ACN + 100mL H2O + 0.05% acetic acid
- Make-up solvent: 950mL MeOH + 50mL H2O + 0.05% acetic acid
- Column size: 150 mm x 10 mm, particle size: 5 um 

**Process:**
- Install/check column, solvent bottle level, tuning mix solution.
- The 2L bottle should be used for mobile phase due to high flow rate of prep-LC (normally 4 mL/min - 10 mL/min)
- Turn on all modules. Wait until it is ready (green color for each module).
- Purge 4 solvent lines until all bubble air are pushed out. It can take much more time than in analytical LC since the solvent lines are bigger. Monitoring the solvent level during purge.
- To purge, open the LC-pump valve, then choose the line to purge at set the flowrate maximum at 50mL/min. 
- Condition the column with acquisition method condition for at least 45 minutes.
- Samples are put in auto-sampler by 6-axis.
- Create a sequence and run. Inject 1-2 blanks before samples
- Data collection and treatment.
- Wash the column following producer method.

**Outcome:**
- Depending on screened molecules, there is DAD (UV-absorption sample) and MS signal (ionizable sample).
- If the MS signal is too low, the split ratio can be optimized.
- All the acquisition method details can be found in acquisition setup.
- Peak details can be found in Peak Details and Injection Results and extracted automatedly.
- Calibration curve can also be done by Openlab.
- To set a method for treatment data, going to processing method to setup. This method can be saved and applied for all sequences or other sequences.

2. OMNIFIRE
3. NMR
4. FTIR
5. Multicells HR-UV
6. SFC - DAD - IM -QTOF

* Image to insert here
* Valve schema

**Purpose:** one dimension of characterization. Give the information of m/z, CCS and drift time, retention time. 

**Design:** modules. They can be controlled and modified in method.
- Auto-sampler: sample injection.
- Column chamber: capacity installation : 7 columns
- SFC pump: Pressure maximum: 800 bar. 4 solvent tubes: A1 (CO2 as default), A2 (not utilized, in MeOH), B1, B2 are the mobile phase and be chosen by purpose.
- DAD (diode array detector): UV and Vis lamps. Wavelength: 200-800nm.
- Isopump for MS: to transfer and mix the make - up solvent with sample flow before going to MS. 2 solvent lines can be chosen A1 and A2
- IM (ion mobility): second separation dimension. Separate by mobility of ions, depending on size and charge.
- QTOF (quadrupole time of fly): High resolution MS/MS
- 
  There is also a tray to put solvent bottles. There is no fraction collector for PrepLC. The out-going flow will be collected by OMNIFIRE.
* 

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
