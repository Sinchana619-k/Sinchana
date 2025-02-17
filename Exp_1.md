# experiment-01 
DC,AC and transcient analysis of common source Amplifier experiment 
# introduction

A Common-Source (CS) amplifier is a fundamental circuit used for voltage amplification in analog electronics. It is widely utilized in signal processing applications due to its high gain and moderate input impedance. In this experiment, a TSMC 180nm NMOS transistor is used to design and analyze a CS amplifier operating at VDD = 1.8V with a power budget of 50µW.

The objective of this experiment is to study the amplifier’s behavior by performing DC analysis, AC analysis, and transient analysis using LTspice. The DC analysis helps determine the operating point of the transistor, ensuring it operates in the saturation region for proper amplification. The AC analysis is conducted to evaluate the voltage gain and bandwidth, which are crucial for signal processing applications. Lastly, the transient analysis examines the amplifier’s response to time-varying input signals.

Through these analyses, key performance parameters such as gain, bandwidth, power dissipation, and operating conditions are extracted. This experiment provides insights into optimizing low-power amplifier designs for real-world applications.


# components used 

1. Power Supply (V1 = 1.8V) – Provides the DC operating voltage.


2. Input Voltage Source (V2 = SINE(-0.9 50m 1k)) – AC signal source with:

Offset: 0.9V

Amplitude: 50mV

Frequency: 1kHz

3. NMOS Transistor (M??, Model: CMOSN) – The active amplifying component.
4. Drain Resistor (R1 = 1KΩ) – Defines gain and sets the DC operating point.
5. SPICE Commands:
.dc V2 0 1.8 0.1 → DC sweep analysis from 0V to 1.8V with 0.1V steps.
.tran 1m → Transient analysis for 1ms.
.ac dec 20 1k 1T → AC analysis (20 points per decade, from 1kHz to 1THz).
.libtsmc018.lib → TSMC 180nm model library.
This setup is used to determine DC operating point, voltage gain, bandwidth, and transient response of the amplifier.

# circuit diagram 
# circuit 1

![1000086513](https://github.com/user-attachments/assets/65689cb2-3d74-4747-aec1-55fd172eb593)

#simulation

DC analysis 
![1000086502](https://github.com/user-attachments/assets/89517c7f-2d95-4ef2-9ee6-343e9c7e976e)

calculation 

1 DC Operating Point (from LTspice results)

• V(n002) (Gate Voltage, V_G) = 0.9V

• V(n003) (Drain Voltage, V_D) = 1.77233V

• V(n001) (VDD) = 1.8V

• Drain Current (I_D) = 2.76742 x 10-5 A = 27.67 μΑ

2. Power Dissipation

Power dissipation in the MOSFET:

PMOS IDX (VDD - VD)

P_MOS = (27.67 × 10^{-6})× (1.8 - 1.77233) 

PMOS ≈ 0.76μW

Total power consumption:

PTotal IDX VDD

P_Total= (27.67 × 10^{-6}) × 1.8]

PTotal ≈ 49.8µW

Q point ( 1.77 V ,27.76×10^-6A)

Voltage Gain Calculation

The small-signal gain of the CS amplifier is given by:

Av = -gmRD

• Transconductance (g_m) ≈ Vov VGS-Vth 2ID 

• Drain Resistor (R_D) = 1ΚΩ

Using approximate values (assuming Vth≈ 0.4V and VGs ≈ 0.9V):

g_m =2 × 27.67 × 10^{-6}} {0.5} = 0.11
Av = -(0.11 × 10-3) × (1 × 10³)
gain is approximately -11 dB


Bandwidth Calculation:

fc = 2π(103) (5×10-15)

fc 1/2π×5×10-12

1 fc = 3.14×10-11

fc ≈ 31.8 GHz


AC analysis 
![IMG-20250217-WA0018](https://github.com/user-attachments/assets/1a54421d-ce1d-43d7-b3f6-7380b9e462a0)

transient 
![IMG-20250217-WA0017](https://github.com/user-attachments/assets/79ab637a-e409-4d58-af90-9f3e80ed3923)

# circuit 2
 ![1000086495](https://github.com/user-attachments/assets/c449d331-ad59-486b-8e4d-95606bd1f0f9)

DC analysis 
![1000086337](https://github.com/user-attachments/assets/593a5821-66fb-4d6a-9a35-57e3ad91e218)


AC analysis 
![1000086504](https://github.com/user-attachments/assets/2eafa119-aa7e-4c85-89f9-e968277a6001)

transient analysis 
![1000086503](https://github.com/user-attachments/assets/8d7ae470-29e5-4635-88c0-bb02f618141a)








