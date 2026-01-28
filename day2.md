# Analog IC Design Hands-On using Cadence Virtuoso

## 28/01/26 WEDNESDAY
## Overview
This repository contains the work done during the hands-on sessions on **Analog IC Design and Layout Considerations** conducted in our college(**DAY 2**).

In these sessions, 
We designed and simulated different analog circuits in **Cadence Virtuoso** and performed **DC, Transient, and AC analysis**.

## Circuits Implemented

### 1. Common Source (CS) Amplifier
The CS amplifier is used to get voltage gain.  
The NMOS is biased in saturation region for proper amplification.

**Schematic**
<img width="1275" height="714" alt="Screenshot 2026-01-28 214254" src="https://github.com/user-attachments/assets/9ed8b8a8-cbdd-45c5-9c34-70244ff9d978" />


### 2. Current Mirror
The current mirror provides constant current for biasing other blocks.  
It is very important in analog IC design.

**Schematic**
<img width="1277" height="716" alt="Screenshot 2026-01-28 214314" src="https://github.com/user-attachments/assets/c667e7c3-02a3-4cfa-ba92-717f3b0bbf7e" />


### 3. Differential Pair
The differential pair is the input stage of op-amps and comparators.  
It amplifies the difference between two input signals.

**Schematic**
<img width="1272" height="711" alt="Screenshot 2026-01-28 214331" src="https://github.com/user-attachments/assets/a98b25d6-9fc5-47e8-82e0-b1e6c435f8c4" />


## DC Analysis
DC analysis was done to check operating points and make sure all MOSFETs are in saturation region.

**Common Source DC Result**
<img width="1275" height="721" alt="Screenshot 2026-01-27 194425" src="https://github.com/user-attachments/assets/640865b9-6012-4a54-95d6-f6b8e6550fc4" />


**Current Mirror DC Result**
we got same results as above 

**Differential Pair DC Result**


**for all the above DC analysis PMOS was in subthreshold region whhich was because we had only controlled current using width of PMOS**

## Transient Analysis
Transient analysis was done by applying sinusoidal input and observing output waveforms.

**CS Amplifier Transient Response**
<img width="1276" height="712" alt="Screenshot 2026-01-28 214700" src="https://github.com/user-attachments/assets/f3d8c542-239e-45da-aa0b-deb394c40c12" />

**Differential Pair Transient Response**
<img width="1273" height="708" alt="Screenshot 2026-01-28 214715" src="https://github.com/user-attachments/assets/ae585d5e-0391-40b4-a6cc-e018089df69d" />


**Multiple Outputs Transient**
<img width="1278" height="719" alt="Screenshot 2026-01-28 214624" src="https://github.com/user-attachments/assets/432fe71c-90f3-4a53-a58b-b5b74fae7cf1" />



## AC Analysis
AC analysis was done to study gain and bandwidth of the circuits.

**CS Amplifier AC Response**
<img width="1271" height="714" alt="Screenshot 2026-01-28 214726" src="https://github.com/user-attachments/assets/a4304631-cc5f-4ecf-b2df-3ece1c81ca13" />


**Differential Pair AC Response**
<img width="1272" height="716" alt="Screenshot 2026-01-28 214647" src="https://github.com/user-attachments/assets/1e7acfa0-9079-492b-9861-80d8dc4c2dcb" />


## Observations
- MOSFETs were properly biased in saturation region
- CS amplifier showed gain with 180° phase shift
- Differential pair responded to input difference
- Gain drops at high frequency due to parasitic capacitances
- DC, transient, and AC analysis helped understand real circuit behavior


## Symbol Creation and Usage in Cadence Virtuoso
we created a symbol for differential amplifier which we designed above


### Symbol Created

**Amplifier Symbol**  
- Inputs: `vinp`, `vinn`, `vb`  
- Output: `vout`  
- Power Pins: `vdd`, `vss`  
- Symbol labeled as "amplifier" with instance name placeholder  

**Symbol Editor Screenshot**  
<img width="1272" height="721" alt="Screenshot 2026-01-28 220552" src="https://github.com/user-attachments/assets/25369f14-6406-4bb4-ba13-09693b95149b" />

### Schematic Using Symbol

**Test Schematic**  
- Symbol instantiated as `I0`  
- Inputs driven by sinusoidal sources  
- Output observed across capacitor  
- Power and biasing provided via DC sources  

**Schematic Screenshot**  
<img width="1278" height="713" alt="Screenshot 2026-01-28 220958" src="https://github.com/user-attachments/assets/7d6dce2c-03e3-46e4-aa22-0b16ba18e440" />


### Simulation Results

#### DC Analysis  
- Verified operating points of MOSFETs  
- Ensured amplifier biasing is correct  
- Observed `id`, `vgs`, `vds`, and `gm` values  

#### Transient Analysis  
- Applied sinusoidal inputs to `vin1` and `vin2`  
- Observed output waveform at `vout`  
- Verified amplification and phase behavior  

**Transient Response Screenshot**  
<img width="1276" height="715" alt="Screenshot 2026-01-28 221025" src="https://github.com/user-attachments/assets/9dd33dd7-98f1-425e-ab26-d38981b37a06" />


#### AC Analysis  
- Studied frequency response of amplifier  
- Observed gain roll-off at high frequencies  
- Verified low-pass characteristics  

**AC Response Screenshot**  
<img width="1276" height="715" alt="Screenshot 2026-01-28 221025" src="https://github.com/user-attachments/assets/29ede494-1c91-43fb-b8da-46dc52033d42" />


### Observations
- Symbol creation simplifies schematic reuse  
- Amplifier symbol worked correctly in test setup  
- DC analysis confirmed proper biasing  
- Transient and AC analysis showed expected behavior  
- Hierarchical design improves modularity and clarity

## Conclusion
These sessions helped in understanding how basic analog blocks are designed and verified in industry tools like Cadence Virtuoso.  
It gave practical exposure to biasing, simulation, and analysis of analog IC circuits.

