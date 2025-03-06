# experiment_03
# Differential amplifier 
This experiment shows the ac,dc and transient analysis of Differential amplifier

# introduction

A differential amplifier is a fundamental building block in analog circuit design, commonly used in applications like signal amplification, noise rejection, and operational amplifier configurations. In this experiment, we designed and analyzed a differential amplifier using LTspice based on specific design constraints, including power dissipation, supply voltage, and common-mode voltage.

The experiment involved performing DC analysis to determine the operating point, transient analysis to observe the amplifier’s time-domain response, and frequency response analysis to evaluate its gain and bandwidth. The simulation results were used to extract key parameters such as differential gain, common-mode rejection ratio (CMRR), and input/output characteristics.

By utilizing LTspice, we ensured accurate modeling of circuit behavior, and the final design, along with the simulation data, is documented.

Question : Design Differential amplifier for the following specifications vdd=2.5v ,P<=3mW,vicm=1.3v ,vocm=1.4v, vp=0.5v. Perform Dc analysis, transient analysis, frequency response and extract the required parameters.

![1000089962](https://github.com/user-attachments/assets/4290f1d2-7d93-4c66-af3a-a4055d69cb02)

# Theory 
A MOSFET differential amplifier amplifies the difference between two input signals while rejecting common-mode noise, making it essential in precision applications. It consists of two matched MOSFETs with a common current source, ensuring balanced operation. When differential signals are applied, the transistors conduct differently, producing an amplified output. The experiment involves DC analysis to determine the operating point (voltages and currents), transient analysis to observe its response to time-varying signals, frequency response analysis to evaluate its gain over different frequencies, and parameter extraction to measure critical characteristics like gain, bandwidth, input/output swing, and common-mode rejection ratio (CMRR). The design must ensure proper biasing and stability to achieve optimal amplification performance within the given specifications.






