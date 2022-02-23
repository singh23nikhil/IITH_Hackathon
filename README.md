# IITH_Hackathon

                  Design of Schmitt Trigger Using Domino Logic in 28nm

This repository consists of the project which was designed and simulated using synopsys custom compiler


ABSTRACT:

Hysteresis, Noise margin and Power consumption are the primary parameters that determine how robust a Schmitt trigger is. These are essentially a bi-stable multi vibrator that produces a stable output i.e. logic 1 or logic 0 whenever a noisy input is being fed into it. Due to this property, it finds its application in both analog as well as digital domain. When these circuits are formed using the dynamic logic, they exhibit better hysteresis, higher noise margin and reduced power consumption as compare to the ones formed by the static CMOS. Also the speed of operation is more as compared to the static counterparts. In this project we design Schmitt trigger using domino logic which aims at enhancing the hysteresis as well as noise margin. The analysis and simulations of the circuits are performed using industrystandard full-suite Synopsys® tools using a 28 nm technology library.

REFERENCE CIRCUIT DETAILS:

Static CMOS circuits are slower in operation, consume more area and have short circuit power dissipation. On the other hand dynamic counter parts require less number of transistors, have faster switching speed and negligible static power dissipation. Since the power consumption and hysteresis are primary factors in designing the Schmitt trigger, a approach in which clock is involved is followed. Due to this clocked type approach the static component of power is absent as it makes use of sequence of phase namely the pre-charge and evaluation phase.
    In this type of logic style, a problem comes into the picture when cascading of the gates takes place. The precharge state of first stage may cause the second stage to discharge prematurely even before the first stage has reached it correct state. This makes use of the pre-charge of the second stage which cannot be restored until the next clock cycle, hence no recovery from this error. One of the solutions to this problem can be the domino logic. Domino logic is a modification of dynamic logic. From the Fig. 1 we can see that it introduces a static inverter between two stages. The static inverter reduces the logical effort as there is no fan-out to multiple pfet’s resulting in the reduced input capacitance. Since it connects to only n-block of next stage, it makes the speed of operation faster. The width of NMOS and PMOS of the inverter is adjusted so as to improve the operating speed.
    In this domino cascade structure of multiple stages, the evaluation phase of each stage ripples the next stage resulting in an operation similar to that of falling dominoes. Although the domino logic provides a solution to the cascade structure it in turn incorporates problems like contention, charge leakage, charge sharing, and increased number of transistors, increased delay and power consumption
    
REFERENCE CIRCUIT DESIGN:

![image](https://user-images.githubusercontent.com/67039315/155268390-86a18182-5d4e-4b87-b891-e248eae0385e.png)

REFERENCE WAVEFORM:

![image](https://user-images.githubusercontent.com/67039315/155268485-2815fd02-a582-41ad-b441-bff87cfb3a8a.png)

ACTUAL SCHEMATIC:


