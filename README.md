# High-speed-dynamic-comparator-28nm-process
This repository presents a high-speed dynamic comparator which could optimize the basically differential amplifier and class AB latch circuit, designed and verified in 28nm CMOS process with Synopsys Custom Compiler tool. The proposed design is powered by 1.05V supply
# Table of Contents

- [Abstract](#abstract)
- [Tools Used](#tools-used)
- [Proposed Comparator Design](#proposed-comparator-design)
- [Pre Amplifier Circuits](#pre-amplifier-circuits)
- [Pre Amplifier Stage 1](#pre-amplifier-stage-1)
- [Pre Amplifier Stage 2](#pre-amplifier-stage-2)
- [CMOS Latch Circuit](#cmos-latch-circuit)
- [SR Latch Circuit](#sr-latch-circuit)
- [Dynamic Comparator Schematic and Testbench](#dynamic-comparator-schematic-and-testbench)
- [Simulation Result](#simulation-result)
- [Netlist](#netlist)
- [Author](#author)
- [Acknowedgements](#acknowledgements)
- [References](#references)


# Abstract

Here is presented an  high-speed dynamic comparator which could optimize the basically differential amplifier and class AB latch circuit, designed and verified in  28nm CMOS process with Synopsys tools. The proposed design is powered by 1.05V supply and the output signal only exhibits 0.2mV/0.8mV offset voltage when the clock signal at the 1 GHz. The proposed circuit is useful for the electronic industries, highspeed ADCs and SerDes.

# Tools Used

- Synopsys Custom Compiler:  The Synopsys Custom Compiler™ design environment is a modern solution for full-custom analog, custom digital, and mixed-signal IC design. As the heart of the Synopsys Custom Design Platform, Custom Compiler provides design entry, simulation management and analysis, and custom layout editing features. This tool was used to design the circuit on a transistor level.
- Synopsys Primewave:  PrimeWave™ Design Environment is a comprehensive and flexible environment for simulation setup and analysis of analog, RF, mixed-signal design, custom-digital and memory designs within the Synopsys Custom Design Platform. This tool helped in various types of simulations of the above designed circuit.
- Synopsys 28nm PDK:  The Synopsys 28nm Process Design Kit(PDK) was used in creation and simulation of the above designed circuit.

# Proposed Comparator Design

The figure shows the overall basic diagram of the proposed comparator. The comparator consists of pre-amplifier circuit, CMOS latch circuit and SR latch circuit. The preamplifier circuit is used to amplify the input signal and the latch circuit is controlled by clock signal. When the clock signal is high, the circuit enters the regenerative stage and the circuit enters the comparative stage when the clock signal is low.

<p align="center">
  <img src="/Images/proposed_Design.png"> <br>
Fig. 1 Proposed Dynamic Comparator Block Diagram
</p>


## Pre Amplifier Circuits


The offset voltage is more important indicator of the comparator, which usually decides the quality of the circuit. The proposed circuit needs two stages amplifier to obtain high resolution, high gain and high bandwidth. In addition, the long channel length of transistors are used at the input. Thus, the mismatch of differential input pairs can be reduced and the transconductance can be enhanced.

### Pre Amplifier Stage 1

<p align="center">
  <img src="/Images/Fast_comparator_pre_amplifierS1_schematic.png"> <br>
 Fig. 2 Pre Amplifier Stage 1
</p>

The pre-amplifier circuit consists of two-stage preamplifier circuit. The first stage is shown in Fig. 2, which is a basically differential amplifier circuit. In order to reduce the offset, the channel length of the transistors for the input should be increased slightly, which reduce the mismatch of the circuit.

### Pre Amplifier Stage 2

<p align="center">
  <img src="/Images/Fast_comparator_pre_amplifierS2_schematic.png"> <br>
 Fig. 3 Pre Amplifier Stage 2
</p>

The second stage pre-amplifier circuit as shown in Fig. 3. The gate of M4 is controlled by the clock signal clk. Then, the static power consumption of the circuit can be reduced due to there no current flows when the transistor M4 is off.

## CMOS Latch Circuit

The CMOS latch circuit reduces the static power consumption, and makes the input remain condition of equilibrium when the next stage SR latch stays the regenerate stage. Similarly, it can reduce hysteresis, the charge-storage effect of the CMOS latch circuit, and offset voltage of comparator. In addition, the delay of circuit reduced by optimizing the recovery time of overdrive voltage.

<p align="center">
  <img src="/Images/Fast_comparator_cmoslatch_schematic.png"> <br>
 Fig. 4 CMOS Latch Circuit
</p>

## SR Latch Circuit

<p align="center">
  <img src="/Images/Fast_comparator_sr_latch_schematic.png"> <br>
 Fig. 5 SR Latch Circuit
</p>

# Dynamic Comparator Schematic and Testbench

<p align="center">
  <img src="/Images/Fast_comparator_Dynamic_Comparator_schematic.png"> <br>
 Fig. 6 Dynamic Comparator Circuit
</p>


# Simulation Result

<p align="center">
  <img src="/Simulation/TranAnalysisComparator.png"> <br>
 Fig. 7 Waveform Result
</p>

# Netlist

Netlist of the Dynamic Comparator can be found [here](/Netlist/netlist_DynamicComparator)

# Author

- [Vaibhav Mishra, M.TECH VLSI DESIGN, Vellore Institute of Technology, Vellore ](https://www.linkedin.com/in/vaibhav-mishra-33487612a)

# Acknowledgements

- [Kunal Ghosh, Co-founder, VSD Corp. Pvt. Ltd.](https://www.linkedin.com/in/kunal-ghosh-vlsisystemdesign-com-28084836/)
- [Synopsys Inc](https://www.synopsys.com/)
- [IIT Hyderabad](https://iith.ac.in/)
- [Analog IC Design Hackathon](https://www.iith.ac.in/events/2022/02/15/Cloud-Based-Analog-IC-Design-Hackathon/)
- [Sameer Durgoji, NIT Karnataka](https://www.linkedin.com/in/sameer-s-durgoji-340b26180/)
- [Chinmay Panda, IIT Hyderabad](https://www.iith.ac.in/events/2022/02/15/Cloud-Based-Analog-IC-Design-Hackathon/)

# References

[1] Xuqiang Zheng, Zhijun Wang, Fule Li, Feng Zhao, Shigang Yue,Chun Zhang, et al, “A 14-bit 250 MS/s IF Sampling Pipelined ADC in 180 nm CMOS Process.” IEEE Transactions on Circuits & Systems I Regular Papers 63.9(2016):1381-1392.

[2] B. B. A. Fouzy, M. B. I. Reaz, M. A. S. Bhuiyan, M. T. I. Badal, F. H.Hashim, “Design of a low-power high-speed comparator in 0.13μm CMOS.” International Conference on Advances in Electrical, Electronic and Systems Engineering IEEE, 2017:289-292. 

[3] Ahmadi Muhammad, and W. Namgoong, “Comparator Power Minimization Analysis for SAR ADC Using Multiple Comparators.”  IEEE Transactions on Circuits & Systems I Regular Papers62.10(2015):2369-2379. 

[4] Chun C. Lee, and Micheal P. Flynn, “A SAR-Assisted Two-Stage Pipeline ADC. ” IEEE Journal of Solid-State Circuits 46.4(2011):859-869.  

[5] Aida Varzaghani, Athos Kasapi, Dimitri N. Loizos, Song-Hee Paik, Shwetabh Verma, Sotirios Zogopoulos, et al, “A 10.3-GS/s, 6-Bit Flash ADC for 10G Ethernet Applications.” IEEE Journal of Solid- State Circuits 48.12(2013):3038-3048.
