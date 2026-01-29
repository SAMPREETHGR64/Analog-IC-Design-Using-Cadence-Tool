# Analog IC Design Hands-On using Cadence Virtuoso

## 29/01/26 THURSDAY
## Overview
This repository contains the work done during the hands-on sessions on **Analog IC Design and Layout Considerations** conducted in our college(**DAY 3**).

In these sessions, 
We designed and simulated different analog circuits in **Cadence Virtuoso** and performed **DC, and learned to use measurement tool and calculator in cadence**.

## Circuits Implemented

### 1. Bandgap Reference (BGR) basic Circuit Design

- Designed simple BGR circuit
- <img width="875" height="717" alt="Screenshot 2026-01-29 202311" src="https://github.com/user-attachments/assets/47cdfda7-d703-412b-908b-9477c38490ae" />

- Used measurement tool to view frequency spectrum
- <img width="1274" height="714" alt="image" src="https://github.com/user-attachments/assets/c5672da9-bfc2-4495-9235-8f358c637c3c" />

### 2. BGR

- designed BGR circuit
<img width="1276" height="718" alt="Screenshot 2026-01-29 202330" src="https://github.com/user-attachments/assets/232db09f-05c7-4397-aa55-317f9b464144" />

- Used calculator tool to:
  - Plot difference of two signals
  - Find derivative of signal
    <img width="1331" height="720" alt="image" src="https://github.com/user-attachments/assets/50e6dcfd-35cc-4e2b-a67e-3010a16a7126" />
    here the difference between R2 terminal is propotional to absolute temp (PTAT) = delta VBE which is PTC (positive temp coefficient).
    VBE2 is the complementary to absolute temp (CTAT) = (NTC) negetive temp coefficient

below is the results 
<img width="848" height="719" alt="image" src="https://github.com/user-attachments/assets/f7f50032-de32-4840-850a-63aaba80fde8" />
<img width="848" height="724" alt="image" src="https://github.com/user-attachments/assets/23c2865b-3588-469b-9f2d-6267667c969a" />

the below is the derivative of PTAT
<img width="614" height="720" alt="image" src="https://github.com/user-attachments/assets/13ec8d76-3c7c-413e-bf99-9375f1b4cf65" />

the below is the derivative of CTAT
<img width="604" height="718" alt="image" src="https://github.com/user-attachments/assets/4f2eb06b-13e1-440c-a181-619ebbc99487" />





