---
title: 2. Characterization part
layout: default
parent: Analytics
---
**Purpose**: to characterize in many dimension and give the information about new/unknown molecule as much as possible.
1. Semi- preparative LC - DAD - MS (SQ) 

*Image to insert here*

*Valve schema* 

**Purpose:** to separate and purify the target molecules, normally, they are the new/unknown molecules detected from screening part. 
$
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
