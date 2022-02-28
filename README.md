# IITH_Hackathon

#                  Design of Schmitt Trigger Using Domino Logic in 28nm

This repository consists of the project which was designed and simulated using synopsys custom compiler


## ABSTRACT:

Hysteresis, Noise margin and Power consumption are the primary parameters that determine how robust a Schmitt trigger is. These are essentially a bi-stable multi vibrator that produces a stable output i.e. logic 1 or logic 0 whenever a noisy input is being fed into it. Due to this property, it finds its application in both analog as well as digital domain. When these circuits are formed using the dynamic logic, they exhibit better hysteresis, higher noise margin and reduced power consumption as compare to the ones formed by the static CMOS. Also the speed of operation is more as compared to the static counterparts. In this project we design Schmitt trigger using domino logic which aims at enhancing the hysteresis as well as noise margin. The analysis and simulations of the circuits are performed using industrystandard full-suite Synopsys® tools using a 28 nm technology library.

## REFERENCE CIRCUIT DETAILS:

Static CMOS circuits are slower in operation, consume more area and have short circuit power dissipation. On the other hand dynamic counter parts require less number of transistors, have faster switching speed and negligible static power dissipation. Since the power consumption and hysteresis are primary factors in designing the Schmitt trigger, a approach in which clock is involved is followed. Due to this clocked type approach the static component of power is absent as it makes use of sequence of phase namely the pre-charge and evaluation phase.
    In this type of logic style, a problem comes into the picture when cascading of the gates takes place. The precharge state of first stage may cause the second stage to discharge prematurely even before the first stage has reached it correct state. This makes use of the pre-charge of the second stage which cannot be restored until the next clock cycle, hence no recovery from this error. One of the solutions to this problem can be the domino logic. Domino logic is a modification of dynamic logic. From the Fig. 1 we can see that it introduces a static inverter between two stages. The static inverter reduces the logical effort as there is no fan-out to multiple pfet’s resulting in the reduced input capacitance. Since it connects to only n-block of next stage, it makes the speed of operation faster. The width of NMOS and PMOS of the inverter is adjusted so as to improve the operating speed.
    In this domino cascade structure of multiple stages, the evaluation phase of each stage ripples the next stage resulting in an operation similar to that of falling dominoes. Although the domino logic provides a solution to the cascade structure it in turn incorporates problems like contention, charge leakage, charge sharing, and increased number of transistors, increased delay and power consumption
    
## REFERENCE CIRCUIT DESIGN:

![image](https://user-images.githubusercontent.com/67039315/155268390-86a18182-5d4e-4b87-b891-e248eae0385e.png)

## REFERENCE WAVEFORM:

![image](https://user-images.githubusercontent.com/67039315/155268485-2815fd02-a582-41ad-b441-bff87cfb3a8a.png)

## ACTUAL SCHEMATIC:

![domino_circuit](https://user-images.githubusercontent.com/67039315/155269926-2729ec79-521c-4888-922a-a854247589bc.jpeg)

## ACTUAL SYMBOL:

![domino_symbol](https://user-images.githubusercontent.com/67039315/155270012-6e3e7972-766b-4203-a8a8-0fdb3ace1d8f.jpeg)

## TESTBENCH SCHEMATIC:

![domino_TB](https://user-images.githubusercontent.com/67039315/155270073-cb0d4bea-27cf-45a1-ae5a-7d8ee522b90a.jpeg)

## PARAMETERS FOR INPUT PIN CLK:

![parameter clk](https://user-images.githubusercontent.com/67039315/155271219-d6a04303-b348-4a6b-b408-90a1fc5a48b8.PNG)

## PARAMETERS FOR INPUT VIN:

![parameter vin](https://user-images.githubusercontent.com/67039315/155271246-ec4e9752-5af2-4a7f-8484-04549f87dffa.PNG)

## TRANSIENT ANALYSIS:

![tran](https://user-images.githubusercontent.com/67039315/155271420-aee7be65-cae2-4952-9dd1-ab67beccef2f.PNG)

## PRIMEWAVE SETUP:

![primewave setup](https://user-images.githubusercontent.com/67039315/155271472-0563ca07-1832-4259-9c8f-2c0934ee2449.PNG)

## NETLIST:

![image](https://user-images.githubusercontent.com/67039315/155271921-88c7b909-809c-48a9-bd44-a9112af604f2.png)
![image](https://user-images.githubusercontent.com/67039315/155271963-c9660cd3-47c2-4c77-b45b-8a83c76164cc.png)
![image](https://user-images.githubusercontent.com/67039315/155272006-2e56ccec-316e-4a1c-b802-72ee10e0ee10.png)

## WAVEFORMS:

![waveform](https://user-images.githubusercontent.com/67039315/155272080-aa8c00e3-389e-4b80-b6a6-fda778770cca.PNG)
Transient analysis of Domino Schmitt trigger

![cmos_st_waveform](https://user-images.githubusercontent.com/67039315/155841612-58d5290e-0f7f-4d91-aeb6-24264a8b156d.PNG)
Transient analysis of CMOS Schmitt trigger

![domino_st_response](https://user-images.githubusercontent.com/67039315/155981260-a555bc28-8143-40e6-9e34-506d89ffe8e8.PNG)
Response of domino Schmitt trigger for sinusoidal input

![cmos_st_response](https://user-images.githubusercontent.com/67039315/155981379-430471b4-27ee-4dc8-acd5-0d0af75f89b6.PNG)
Response of cmos Schmitt trigger for sinusoidal input

## COMPARISON OF AVERAGE POWER AND PROPAGATION DELAY WITH CMOS SCHMITT TRIGGER:

![image](https://user-images.githubusercontent.com/67039315/155967014-20236246-5365-4707-b920-6bcc790c5805.png)

## CONCLUSION:

From the waveform we can observe that the domino schmitt trigger is 33.6% better in terms of average power dissipation while the propagation delay is almost same to that of cmos schmitt trigger. Also the transient analysis similar to that of cmos schmitt trigger. Due to the inverter present at output we are getting a inverted waveform. Hence the schmitt trigger can be used is various applications for eg. ADC, Comparators etc.

## AUTHOR:
Nikhil Singh, VIT Chennai

## ACKWOLEDGEMENT:

Kunal Ghosh, Co-founder, VSD Corp. Pvt Ltd.

Chinmay Panda, IIT Hyderabad

Synopsis Company

IIT Hyderabad

## REFERENCES:
[1] Ramakrishna, Balaji & Madhusudhan, S. & Nikshep, B. & Naveen, B. & Teerthaprasad, H.. (2020). Power and delay optimization of domino Schmitt trigger configurations with enhanced hysteresis voltage. Analog Integrated Circuits and Signal Processing. 102. 10.1007/s10470-019-01541-8.

[2] Bhaaskaran, V s kanchana & Angeline, Anita. (2019). Design Impacts of Delay Invariant High Speed Clock Delayed Dual Keeper Domino Circuit. IET Circuits, Devices & Systems. 13. 10.1049/iet-cds.2018.5410.

[3] https://www.iosrjournals.org/iosr-jvlsi/papers/vol11- issue3/A1103010117.pdf
