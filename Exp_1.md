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
