# Analog-IC-Design-Using-Cadence-Tool

## 27/01/2026 TUESDAY
##  Overview
This repository documents the hands-on session conducted in our college on **Analog IC Design and Layout Considerations**.

The session introduced the fundamentals of **MOSFET operation**, **mixed-signal IC design**, and **Bandgap References, LDOs, and PLLs** in integrated circuits.

As part of the practical work, a **Common Source (CS) Amplifier** was designed and simulated using **Cadence Virtuoso (Spectre)**.  
DC, Transient, and AC analyses were performed to study circuit behavior.

###  Basics of MOSFET
- MOSFET as a voltage-controlled device
- Regions of operation:
  - Cutoff
  - Triode
  - Saturation
- Key parameters:
  - Gate-Source Voltage (VGS)
  - Drain-Source Voltage (VDS)
  - Drain Current (ID)
  - Transconductance (gm)


### Mixed Signal IC Design
Mixed-signal ICs integrate both **analog and digital circuits** on the same chip.

- Digital blocks 
- Analog blocks
- Proper biasing and layout 


### Fundamental Problem in Every Mixed Signal Chip
- Noise between blocks
- Power supply variations
- Process, Voltage, and Temperature (PVT) variations

These issues make voltage reference and regulation blocks vital for IC design.


### Bandgap Reference
- Generates a temperature-independent reference voltage
- Used to bias analog circuits
- Stable across supply variations

### LDO (Low Dropout Regulator)
- Provides clean and stable supply voltage
- Reduces ripple and noise
- Protects sensitive analog blocks

### PLL (Phase Locked Loop)
- Generates accurate clock frequencies
- Maintains synchronization
- Used in processors and communication systems


##  Experiment: Common Source (CS) Amplifier

###  aim
To design and analyze a **Common Source NMOS amplifier** using Cadence Virtuoso and study its DC, transient, and AC responses.
<img width="1275" height="714" alt="Screenshot 2026-01-27 194402" src="https://github.com/user-attachments/assets/0eb41628-a50b-4ddc-8a97-9f7f81574c4a" />


##  Circuit Description
- NMOS transistor used as amplifying element
- Drain resistor connected to VDD
- Gate driven using DC bias and AC signal
- Source connected to ground

The transistor is biased in the **saturation region** for proper amplification.


##  Simulations and Results

### DC Analysis
- Verified operating region of MOSFET
- Observed parameters:
  - VGS ≈ 600 mV
  - VDS ≈ 996 mV
- Ensured stable Q-point operation
<img width="1275" height="721" alt="Screenshot 2026-01-27 194425" src="https://github.com/user-attachments/assets/87785f66-2fee-4581-b08e-1485969170ac" />

**Purpose:**
- Proper biasing
- Confirm saturation region



### Transient Analysis
- Applied sinusoidal input signal
- Output waveform observed

**Observations:**
- Output is amplified
- Output is inverted (180° phase shift), characteristic of CS amplifier

<img width="1274" height="717" alt="Screenshot 2026-01-27 194341" src="https://github.com/user-attachments/assets/22d54a9a-cdcc-44b8-8ee3-5b1bd66b9040" />


### AC Analysis
- Frequency response obtained
- Studied:
  - Voltage gain
  - Bandwidth
  - Gain roll-off at high frequencies



## Result Summary

| Parameter | Observation |
|---------|------------|
| Operating Region | Saturation |
| Phase Shift | 180° |
| Voltage Gain | Negative |
| Bias Stability | Stable |



## Learnings
- Importance of MOSFET biasing
- Role of saturation region in amplification
- Practical understanding of DC, AC, and transient analysis
- Need for bandgap, LDO, and PLL in IC design
- Hands-on experience with Cadence Virtuoso

###  Conclusion
This hands-on session provided a strong foundation in **analog IC design concepts**.  
The Common Source amplifier experiment helped bridge theory with practical simulation and highlighted the importance of essential analog blocks in mixed-signal ICs.

