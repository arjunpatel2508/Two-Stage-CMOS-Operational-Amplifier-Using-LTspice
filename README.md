# Two-Stage-CMOS-Operational-Amplifier-Using-LTspice

DESCRIPTION


This project presents the design and simulation of a Two-Stage CMOS Operational Amplifier using LTspice. The amplifier is implemented at the transistor level using both NMOS and PMOS devices, replicating a standard analog IC design approach widely used in integrated circuits.

TOTAL COMPONENTS REQUIRED 

1. MOSFETs (Active Components)
PMOS Transistors
M1, M2, M3, M4, M5
👉 Total PMOS = 5
NMOS Transistors
M6, M7, M8, M9, M10
👉 Total NMOS = 5

✔️ Total MOSFETs = 10

2. Resistors
R1 = 20kΩ
R2 = 20kΩ

👉 Total Resistors = 2

3. Capacitors
C1 = 150 pF (likely compensation capacitor)
C2 = 200 pF (output/load capacitor)

👉 Total Capacitors = 2

4. Voltage Sources
V1 = 5V (supply / bias)
V2 = 5V (supply)
V3 = SINE(0 1 100k), AC 1 (input signal)

👉 Total Sources = 3

5. Ground
Common reference node (GND)
6. Simulation Command
.ac dec 10 1 10MEG
👉 Used for frequency response (Bode plot)
7. Inputs / Outputs
Vin+ (non-inverting input)
Vin- (inverting input)
Vout (output node)
Final Component Summary
MOSFETs: 10 (5 PMOS + 5 NMOS)
Resistors: 2
Capacitors: 2
Voltage Sources: 3
Ground: 1
Simulation Directive: 1

1.SCHEMATIC VIEW OF CIRCUIT 

<img width="1168" height="595" alt="Screenshot 2026-04-26 171531" src="https://github.com/user-attachments/assets/c62cb819-b28a-43a5-aefe-1d71ffb9ae5d" />



2. Frequency Response Analysis (Bode Plot)

   
The plot represents the AC frequency response of the designed Two-Stage CMOS Operational Amplifier obtained using LTspice.


At low frequencies, the amplifier shows a constant gain (~5–6 dB), indicating stable operation in the midband region.


The circuit exhibits a flat gain response initially, confirming proper biasing and functioning of both amplification stages.


A dominant pole is observed around the kHz range, after which the gain starts to decrease gradually.


The gain rolls off at approximately -20 dB/decade initially, indicating a single-pole response due to Miller compensation (C1).


At higher frequencies, the slope becomes steeper (approaching -40 dB/decade), suggesting the presence of a second pole, typical of a two-stage amplifier.


The phase response (dotted curve) shows a continuous drop, approaching -180° to -270°, which confirms multi-pole behavior.


The gradual phase shift indicates that the compensation capacitor effectively stabilizes the system, preventing abrupt phase transitions.


The gain-bandwidth trade-off is evident, where higher frequency operation results in reduced gain.


The amplifier remains stable without oscillations, indicating proper frequency compensation design.


The unity gain frequency (UGF) lies in the higher frequency range (approx. MHz region), showing the amplifier's usable bandwidth.

   <img width="1175" height="596" alt="image" src="https://github.com/user-attachments/assets/e6b20a84-7403-4336-92d4-cc84fb2effc9" />




