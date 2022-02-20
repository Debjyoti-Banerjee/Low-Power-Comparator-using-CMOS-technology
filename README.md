# Low-Power-Comparator-using-CMOS-technology
--This comparator design was simulated using Synopsys custom compiler as apart of hackathon organised jointly by Synopsys India ,VLSI System Design and IIT Hyderabad

-- The paper or the report submitted for this hackathon can be found ["My Paper"](https://github.com/Debjyoti-Banerjee/Low-Power-Comparator-using-CMOS-technology/blob/main/Debjyoti_comparator_hackathon.pdf)  and the .cir file for simulation can be viewed [here](https://github.com/Debjyoti-Banerjee/Low-Power-Comparator-using-CMOS-technology/blob/main/netlist.cir.pdf) as well.


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

-[METHODOLOGY](#METHODOLOGY)

-[REPRODUCE_WAVEFORMS](#REPRODUCE_WAVEFORMS)

-[LIMITATION](#LIMITATION)

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

First test or draft rough test of the circuit was done using [esim](https://esim.fossee.in/home) and also using Cadence Virtuoso before implementing it in Synopsys design compiler.

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


