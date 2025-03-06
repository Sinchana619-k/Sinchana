# experiment_03
# Differential amplifier 
This experiment shows the ac,dc and transient analysis of Differential amplifier

# introduction

A differential amplifier is a fundamental building block in analog circuit design, commonly used in applications like signal amplification, noise rejection, and operational amplifier configurations. In this experiment, we designed and analyzed a differential amplifier using LTspice based on specific design constraints, including power dissipation, supply voltage, and common-mode voltage.

The experiment involved performing DC analysis to determine the operating point, transient analysis to observe the amplifier’s time-domain response, and frequency response analysis to evaluate its gain and bandwidth. The simulation results were used to extract key parameters such as differential gain, common-mode rejection ratio (CMRR), and input/output characteristics.

By utilizing LTspice, we ensured accurate modeling of circuit behavior, and the final design, along with the simulation data, is documented.

# objective 
Design Differential amplifier for the following specifications vdd=2.5v ,P<=3mW,vicm=1.3v ,vocm=1.4v, vp=0.5v. Perform Dc analysis, transient analysis, frequency response and extract the required parameters.

![1000089963](https://github.com/user-attachments/assets/2920a8b3-e58f-4ae3-bc56-65e65855456c)


# Theory 
A MOSFET differential amplifier amplifies the difference between two input signals while rejecting common-mode noise, making it essential in precision applications. It consists of two matched MOSFETs with a common current source, ensuring balanced operation. When differential signals are applied, the transistors conduct differently, producing an amplified output. The experiment involves DC analysis to determine the operating point (voltages and currents), transient analysis to observe its response to time-varying signals, frequency response analysis to evaluate its gain over different frequencies, and parameter extraction to measure critical characteristics like gain, bandwidth, input/output swing, and common-mode rejection ratio (CMRR). The design must ensure proper biasing and stability to achieve optimal amplification performance within the given specifications.

# circuit 1
Key Components used here:
1.Voltage source(DC): use is to provide a DC bias voltage to the gate of the MOSFET.

2.AC input: Controls drain current and enables amplification.

3.Resistor: The resistor acts as a pull-up resistor for the output node.

# procedure:
Steps to Perform DC, Transient, and AC Analysis in LTspice

1. Setting Up LTspice and Importing the Library

Open LTspice and load the necessary MOSFET model library to ensure accurate simulations.

Merge the tsmc018.lib file (or another relevant library) to include NMOS specifications.


2. Selecting and Placing Components

Choose required components from the LTspice library:

Resistors: 1.833kΩ (×2), 0.416kΩ (for Circuit 1).

MOSFETs: 2 × CMOSN transistors.

Voltage Sources:

VDD = 2.5V (Power supply).

VICM = 1.3V (Common-mode voltage).


Ground (GND) to complete the circuit.


Arrange and connect the components properly as per the circuit schematic.


3. Setting MOSFET Parameters

Specify MOSFET properties such as:

Threshold voltage (Vth)

Temperature

Process variations


Ensure both MOSFETs operate in the saturation region, satisfying:


V_DS > V_GS - V_th

4. Performing DC Analysis

Choose .op (Operating Point Analysis) to check the biasing conditions.

Run the simulation to obtain voltages and currents at different nodes.

Verify that the MOSFETs are in saturation and check the common-mode voltage (VOCM).


5. Performing Transient Analysis

Apply a time-varying input signal (e.g., SINE(1.3V, 50mV, 1kHz)).

Configure transient simulation settings for a 5ms time window.

Run the simulation to observe input and output waveforms for multiple cycles.

Compare individual and combined waveforms to evaluate the amplifier response.


6. Performing AC Analysis

Modify the input voltage source to an AC sinusoidal waveform:

SINE(1.3V, 50mV, 1T)

Use parameters:

Type: Decade

Start Frequency: 0.1 Hz

Stop Frequency: 1 THz

Points per decade: 20


Run the simulation and plot gain (Vout/Vin) vs frequency to analyze frequency response.



 


![1000089981](https://github.com/user-attachments/assets/0ccc86ad-c152-4abd-80bc-18f097793aa2)

In this circuit,
VG=1.3V

Vp=0.5=Vs

VGS=VG-VS

1.3-0.5 = 0.8V

Vt=4.95V

Vov=VGS-Vt

0.8-0.45

0.305V

VDS=VDD-IdRd-Vp

 =2.5-1.8k×0.6m-0.5
 
 =0.92V
 
 VDS>=Vov
 
 so circuit is in saturation region 

 # DC analysis 
 ![1000089993](https://github.com/user-attachments/assets/6581198c-eeec-4b95-bffc-4cbfeb726d36)
 
![1000089979](https://github.com/user-attachments/assets/2e0ab2af-643e-459c-8ca3-1600b8763a3c)
from this we got Qpoint(operating point)
(1.4,0.6m)

![1000089924](https://github.com/user-attachments/assets/15ae99a3-27df-469a-a19a-fb3be33925d8)

 # transient analysis 
 This analysis reveals how the circuit might distort the signal, introduce unwanted DC offsets between input and output, or cause timing issues like phase distortion. Such information is vital for identifying and correcting problems within the circuit.
 
Av=(1.4718-1.3287/1.3481-1.2504)V/V 

=1.4646V/V

 ![1000089978](https://github.com/user-attachments/assets/9d3b00ec-17a8-48dd-91da-34e2a4f70af3)



# AC analysis 
![1000089975](https://github.com/user-attachments/assets/3a9010fe-5247-433c-ba63-1182c2158522)

Av=3.2dB

# Circuit 2

# DC analysis 
![1000090052](https://github.com/user-attachments/assets/7e055a5c-5c09-480c-b0a7-1ea6f8b90283)


# transient analysis 
![1000090027](https://github.com/user-attachments/assets/f9e96bae-af66-43e9-930a-0a0bdd9fea92)

Voltage gain= vout/vin =(1.6287-1.1744)/(1.3982-1.2503) 

=4.533V/V

# ac analysis 
![1000090026](https://github.com/user-attachments/assets/92fdc81a-1a12-4a37-904c-dedf5b2d3f70)

# Circuit 3
Here we are replacing the current source to the mosfet(M3) where we need to keep current Id3 as our desired value And to keep the mosfet(M1,M2,M3) in saturation region so that voltage gain will be maintained.In this ciruit MMOSFETis connected to drain to source terminal and to other ground.

![1000090019](https://github.com/user-attachments/assets/fb28e4af-b503-46e1-b2bb-ee1c1640e921)

# DC analysis 
![1000090053](https://github.com/user-attachments/assets/dea181fb-c8e3-46e5-9fb5-99475acb5f1a)


# Transient Analysis 
![1000090047](https://github.com/user-attachments/assets/0df1125b-184e-4124-87ed-bf01ed1a5840)


# AC analysis 
![1000090048](https://github.com/user-attachments/assets/5c2a3fa5-c8c4-460e-bae5-980f78e595d4)


# Inference 
The MOSFET differential amplifier functions correctly, with proper biasing ensuring operation in the saturation region and achieving the desired VICM = 1.3V and VOCM = 1.4V. The transient analysis confirms differential signal amplification with minimal distortion, while the frequency response suggests an appropriate gain with a well-defined bandwidth, though exact verification of the -3dB cutoff is recommended. The circuit meets design specifications, but fine-tuning W/L ratios or bias currents may optimize gain and bandwidth. Overall, the amplifier is stable, functional, and effective, with minor adjustments potentially enhancing performance.

# conclusion 
The MOSFET differential amplifier successfully meets the design requirements, achieving the expected common-mode and output voltages while maintaining stable operation. The transient and frequency response analyses confirm proper amplification with a reasonable bandwidth. The circuit is functionally correct and stable, with potential for optimization in gain and bandwidth through W/L ratio adjustments and bias tuning.
