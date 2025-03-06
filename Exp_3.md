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

# circuit 1

![1000089981](https://github.com/user-attachments/assets/0ccc86ad-c152-4abd-80bc-18f097793aa2)

In this circuit,
VG=1.3V
Vp=0.5=Vs
VGS=VG-VS
    1.3-0.5
   = 0.8V
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
(1.4,

![1000089924](https://github.com/user-attachments/assets/15ae99a3-27df-469a-a19a-fb3be33925d8)

 # transient analysis 
 ![1000089978](https://github.com/user-attachments/assets/9d3b00ec-17a8-48dd-91da-34e2a4f70af3)

Vinp-p= 1.35-1.26=0.09V
Voutp-p=1.476-1.33=0.14V
so,Av=1.55V

# AC analysis 
![1000089975](https://github.com/user-attachments/assets/3a9010fe-5247-433c-ba63-1182c2158522)

Av=3.2dB

# Circuit 2

