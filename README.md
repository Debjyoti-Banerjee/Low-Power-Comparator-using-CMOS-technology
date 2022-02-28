# Low-Power-Comparator-using-CMOS-technology
--This comparator design was simulated using Synopsys custom compiler as apart of hackathon organised jointly by Synopsys India ,VLSI System Design and IIT Hyderabad

-- The paper or the report submitted for this hackathon can be found ["My Paper"](https://github.com/Debjyoti-Banerjee/Low-Power-Comparator-using-CMOS-technology/blob/main/Debjyoti_comparator_hackathon.pdf)  and the netlist file for simulation can be viewed [here](https://github.com/Debjyoti-Banerjee/Low-Power-Comparator-using-CMOS-technology/blob/main/netlist.cir.pdf) as well.


--This paper reports or portrays the low power and
high speed comparator design using CMOS technology of 28nm
and evaluated using synopsis tools.Design based on two stage
CMOS opamp technique with 1.05 volt Vdd as the corresponding supply voltage.Finally comparing the proposed results with
earlier work done


## CONTENTS

-[INTRODUCTION](#INTRODUCTION)

-[REFERENCE_CIRCUIT](#REFERENCE_CIRCUIT)

-[IMPLEMENTATION](#IMPLEMENTATION)

-[SCHEMATIC](#SCHEMATIC)

-[NETLIST](#NETLIST)


-[SIMULATION_RESULTS](#SIMULATION_RESULTS)

-[METHODOLOGY](#METHODOLOGY)



-[RESULTS](#RESULTS)

-[REFERENCE](#REFERENCE)

-[ACKNOWLEDGEMENT](#ACKNOWLEDGEMENT)

-[AUTHOR](#AUTHOR)


## INTRODUCTION

Comparator is an important device widely used in Analog
to Digital Converters used in large number of application
using low power and audio solutions.Power consumption and
speed are key factors considered while designing comparators.Comparators are classified into open loop and regenrative
comparators using positive feedback.

The comparator idea needs to be researched and popularised more and more and this is because in digital circuits its either "YES" or "NO" and comparing the given voltage to  a known reference is the most sort of feasible thing that helps in digital circuit and has huge applications in the present circuit systems 

First test or draft rough test of the circuit was done using [esim](https://esim.fossee.in/home) and also using Cadence Virtuoso before implementing it in [Synopsys](https://www.synopsys.com/) design compiler.

A comparator behaves as quantizer in the ADC. As the
comparator is of 1-bit it has two levels either a ‘1’ and
‘0’. ‘1’ implies that VDD = +1.05V and a ‘0’ implies that
VSS = -1.05V. If the input of the comparator is greater
than the reference voltage it gives an output of ‘1’ and if
the comparator input is less than reference voltage then the
output of the comparator is ‘0’. A simple comparator performs
the required function as desired. Given a reference level, a
comparator gives an output of VDD when the signal is greater
than the reference level and an output of VSS when signal
is less than reference level. In this design the Vref =0V.
The operational amplifier can be used as a comparator. In
this comparator design we have used the two stage CMOS
OPAMP topology and power consumption amplifier .design technique to achieve highspeed amp; low
power usage. Eliminated the compensation capacitor which
will be used for designing a high gain two stage CMOS
increase speed in the described design. Additional capacitor
is used in two stage CMOS OPAMP for providing stability
in the design,but compromising with stability to obtain the
high performance as low power consumptionwith high speed.
Present CMOS comparator design is shown in paper This
comparator consists by using current mirrors, current sinks,
active load amp; constant current source. width/length ratios
are as selected which gives necessary results. Parasitic effects
that influences in the comparators performance is reduced in
this design. This help to get the desired output for a high speed


## REFERENCE_CIRCUIT


<img width="921" alt="hk_2" src="https://user-images.githubusercontent.com/100065544/154854566-9389d916-bd28-4ba9-8a75-ca6e95ad6a82.png">

The reference circuit diagram has been extracted and recreated from the [paper](https://www.researchgate.net/figure/Proposed-design-of-a-CMOS-comparator_fig4_253237765)


## IMPLEMENTATION

-  ALL the nmos and pmos used in this circuit are designed uding 30nm technology

-  (W/L) used in these nmos and pmos used are  (0.1/0.03) um   except for the last phase nmos and pmos

-  ^ fingers have been used in the last pmos to increase the faster charging of the capacitor when the input signal is above the reference voltage


-  Total  4 pmos  and   5 nmos  have been used in the circuit


-  Capacitor of  100f F has been used


-  Since it is a 30nm technology so the maximum value of Vdd used in the circuit is 1.05 V

-  Synopsys 28nm  technology  library   has been used

-  In2  is the input  signal terminal of the comparator and In1 is the  reference terminal of the comparator

-  Test voltage  of  1kHz frequency has been implemented

-  Maximum magnitude of the input signal and the Vdd value value has been kept different to show that the comparator takes the Vdd value depending on th reference but not dependent on the maximum amplitude of the input signal


## SCHEMATIC


<img width="951" alt="hk_circuit" src="https://user-images.githubusercontent.com/100065544/154856529-42c3be5a-afea-4bf7-96f5-421f8a240b1b.PNG">

### Implementing with symbol

<img width="954" alt="hk_symbol" src="https://user-images.githubusercontent.com/100065544/154858848-4799fded-baae-41d2-8993-fd378e7013fd.PNG">




###  NETLIST

```
*  Generated for: PrimeSim 

*  Design library name: deb_lib1 

*  Design cell name: comparator 

*  Design view name: schematic 

.lib '/PDK/SAED_PDK32nm/hspice/saed32nm.lib' TT 

  

*Custom Compiler Version S-2021.09 

*Sun Feb 20 08:44:45 2022 

  

.global gnd! 

******************************************************************************** 

* Library          : deb_lib1 

* Cell             : comparator 

* View             : schematic 

* View Search List : hspice hspiceD schematic spice veriloga 

* View Stop List   : hspice hspiceD 

******************************************************************************** 

xm3 net30 net30 net57 net57 p105 w=0.1u l=0.03u nf=1 m=1 

xm20 vout net18 net57 net57 p105 w=0.5u l=0.03u nf=5 m=1 

xm9 net37 net37 net57 net57 p105 w=0.1u l=0.03u nf=1 m=1 

xm0 net18 net37 net57 net57 p105 w=0.1u l=0.03u nf=1 m=1 

xm8 net23 net30 net32 net32 n105 w=0.1u l=0.03u nf=1 m=1 

xm7 net30 net30 net32 net32 n105 w=0.1u l=0.03u nf=1 m=1 

xm6 vout net30 net32 net32 n105 w=0.1u l=0.03u nf=1 m=1 

xm5 net37 gnd! net23 net23 n105 w=0.1u l=0.03u nf=1 m=1 

xm4 net18 net53 net23 net23 n105 w=0.1u l=0.03u nf=1 m=1 

c12 vout gnd! c=100f 

v18 net32 gnd! dc=-1.05 

v15 net57 gnd! dc=1.05 

v17 net53 gnd! dc=0 ac=1.05 sin ( 0 600m 1k 0 0 0 ) 

   

  

.tran '0.1u' '5m' name=tran 

  

.option primesim_remove_probe_prefix = 0 

.probe v(*) i(*) level=1 

.probe tran v(vout) v(gnd!) v(net53) 

  

.temp 25 

  

 .option primesim_output=wdf 

  

.option parhier = LOCAL 

 

   

.end 

 ```
 
 ##  SIMULATION_RESULTS
 
 
 <img width="960" alt="hk_final_2" src="https://user-images.githubusercontent.com/100065544/154859950-9d51c0d4-8a29-4caf-b7b4-e7f791640081.png">



- Here we have used reference as the ground or zero voltage, whenever the input signal is crossing the grond voltage a transistion in the output voltage is also taking place.



## METHODOLOGY

- There were approximately five and more number of reference designs for designing comparator however this design was chosen since the pmos combined with the arrangement of the five other nmos used far less power compared to the other designs,moreover from the simulation result it is clearly visible that the transition is very fast when the input crosses the reference voltage.

- The W/L ratio of the transistors were chosen so as to minimise the delay between the input transition above and below the reference voltages,(zero in this case),five finger pmos was used in the last pmos from yhe right since it is directly connected to the capacitor so its speed was most important to  charge the capacitor to the vdd value.

- The first pmos transistor was used initially with a greater number of fingers then to adjust the resistance value since its source and gate are sorted it was again redesigned to one finger.


## RESULTS

- Here is a comparison between the results derived earlier and the results obtained through this simulation 

<img width="563" alt="Capture" src="https://user-images.githubusercontent.com/100065544/154958125-25b3f709-f73f-4943-b94c-56f0900cb822.PNG">


## REFERENCE

- • [International Journal of Electronic Engineering
Research ISSN 0975 - 6450 Volume 2 Number
1 (2010) pp. 29–34© Research India Publications
http://www.ripublication.com/ijeer.htm](https://www.researchgate.net/publication/253237765_Design_of_a_CMOS_Comparator_for_Low_Power_and_High_Speed)

- • https://ieeexplore.ieee.org/document/7888054
- • https://ieeexplore.ieee.org/abstract/document/7873613
- • https://www.academia.edu/Documents/in/ComparatorDesign



##  ACKNOWLEDGEMENT

- [IIT HYDERABAD](https://iith.ac.in/)

- [SYNOPSYS INDIA](https://www.synopsys.com/)

-  [KUNAL GHOSH](https://github.com/kunalg123)   ,  FOUNDER VLSI System DESIGN CORPORATION PRIVATE LIMITED

-  [CHINMAYA PANDA](https://www.researchgate.net/profile/Chinmaya-Panda-6)  , PROFESSOR IIT HYDERABAD  DEPARTMENT OF ELECTRICAL ENGINEERING

-  SAMEER S DURGOJI  NIT KARNATAKA



## AUTHOR

[DEBJYOTI  BANERJEE](https://www.linkedin.com/in/debjyoti-banerjee-9385a4192)

- MTECH VLSI NIT DURGAPUR

- BTECH KALYANI GOVERNMENT ENGINEERING COLLEGE


