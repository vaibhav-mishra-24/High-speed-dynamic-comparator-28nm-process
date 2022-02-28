# High-speed-dynamic-comparator-28nm-process
This repository presents a high-speed dynamic comparator which could optimize the basically differential amplifier and class AB latch circuit, designed and verified in 28nm CMOS process with Synopsys Custom Compiler tool. The proposed design is powered by 1.05V supply
# Table of Contents

# Abstract

Here is presented an  high-speed dynamic comparator which could optimize the basically differential amplifier and class AB latch circuit, designed and verified in  28nm CMOS process with Synopsys tools. The proposed design is powered by 1.05V supply and the output signal only exhibits 0.2mV/0.8mV offset voltage when the clock signal at the 1 GHz. The proposed circuit is useful for the electronic industries, highspeed ADCs and SerDes.

# Tools Used

- Synopsys Custom Compiler:  The Synopsys Custom Compiler™ design environment is a modern solution for full-custom analog, custom digital, and mixed-signal IC design. As the heart of the Synopsys Custom Design Platform, Custom Compiler provides design entry, simulation management and analysis, and custom layout editing features. This tool was used to design the circuit on a transistor level.
- Synopsys Primewave:  PrimeWave™ Design Environment is a comprehensive and flexible environment for simulation setup and analysis of analog, RF, mixed-signal design, custom-digital and memory designs within the Synopsys Custom Design Platform. This tool helped in various types of simulations of the above designed circuit.
- Synopsys 28nm PDK:  The Synopsys 28nm Process Design Kit(PDK) was used in creation and simulation of the above designed circuit.

# Proposed Comparator Design

The figure shows the overall basic diagram of the proposed comparator. The comparator consists of pre-amplifier circuit, CMOS latch circuit and SR latch circuit. The preamplifier circuit is used to amplify the input signal and the latch circuit is controlled by clock signal. When the clock signal is high, the circuit enters the regenerative stage and the circuit enters the comparative stage when the clock signal is low.

<p align="center">
  <img src="https://user-images.githubusercontent.com/54439300/155850948-68074f04-f1e6-4336-9c42-93fbfa1b2100.png"> <br>
</p>

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

[1] Rishu  Yadav,  Manish  Kumar,  “Implementation  of  4X4  Fast  Vedic Multiplier  using  GDI  Method”,  2020  International  Conference  on Electrical and Electronics
Engineering (ICE3-2020) 

[2] Malti  Bansal,  Jasmeet  Singh, “Comparative  Analysis  of 4-bit  CMOS Vedic  Multiplier  and  GDI  Vedic  Multiplier  using  18nm  FinFET Technology”, International
Conference on Smart Electronics and Communication (ICOSEC 2020). 

[3] G.R.Mahendra Babu, S.Bhavani, “Primitive Cells using Gate Diffusion  Input  Technique:  a  Low  Power  Approach”, International Journal of Recent Technology and Engineering
(IJRTE), June 

[4] K.Anirudh Kumar Maurya, Y.Rama Lakshmanna,K.Bala Sindhuri, N. Udaya Kumar, “Design and Implementation of 32-bit  adders  using various  Full  Adders”,  International
Conference  on  Innovations  in Power and Advanced computing Technologies[i-PACT2017].

[5] Mehedi Hasan, Hasan U. Zaman, Mainul Hossain, Parag Biswas, Sharnali Islam, "Gate Diffusion Input technique based full swing and scalable 1-bit hybrid Full Adder for high
performance applications", Engineering Science and Technology, an International Journal, 2020.
