# INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS
![Tool-Ngspice](https://img.shields.io/badge/Tool-Ngspice-blue)
![PDK-Sky130](https://img.shields.io/badge/PDK-Sky130-orange)
![Platform-RISC_V_SoC](https://img.shields.io/badge/Platform-RISC--V_SoC-green)
![License](https://img.shields.io/badge/License-GPLv3-red)
### Why do we need SPICE simulations?
In the RISC-V Reference SoC Tapeout Program, SPICE simulation plays a crucial role in understanding and verifying transistor-level behavior before fabrication. Using Ngspice with the Sky130 PDK, designers can analyze how individual devices and circuits respond to real electrical conditions. Through Week 4 tasks — from studying NMOS I-V characteristics and velocity saturation to exploring CMOS inverter behavior, switching thresholds, and noise/power robustness — SPICE helps visualize and measure the true performance of transistors and logic gates.
## ⚡ SPICE Simulation

SPICE simulations allow us to analyze and optimize circuits virtually before physical fabrication. By applying input waveforms to a circuit, SPICE produces corresponding output waveforms, helping us visualize how the circuit responds over time.

These simulations are essential for measuring key parameters such as delay, rise/fall time, and power consumption. By adjusting transistor dimensions like width (W) and length (L), we can control current flow and switching speed, directly impacting circuit performance. This process helps designers fine-tune and validate designs efficiently, ensuring reliable and optimized operation before committing to silicon fabrication.
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/7ff37809307194b728e8cbc5779436400d03279b/pics/Screenshot%20from%202025-10-15%2017-11-29.png)
### on considering the following example
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/ce41d03989a1e697d47850bb6eaf5944500a70cc/pics/Screenshot%20from%202025-10-15%2017-12-30.png)
The difference between CBUF1 and CBUF2 comes from their circuit design, which might have different drive strengths or W/L ratios (transistor width-to-length).

The delay table values are obtained from SPICE simulations, which are also used to verify delays for the circuit design.
## Introduction to Basic Element in Circuit Design - NMOS Transistor


- **Type:** N-channel MOSFET (uses electrons)  
- **Terminals:** Gate (G), Drain (D), Source (S), Body (B)  
- **Works when:** V<sub>GS</sub> > V<sub>th</sub>  
- **Regions:**  
  - Cutoff → OFF  
  - Linear → Acts as resistor  
  - Saturation → Acts as current source  
- **Key Equation:** I<sub>D</sub> = ½·k·(V<sub>GS</sub> − V<sub>th</sub>)²  
- **Applications:** Logic gates, switches, amplifiers  
- **Complementary Device:** PMOS  

---
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/ece5f17695fe52b2c1d9e7d118658401b966ffe4/pics/WhatsApp%20Image%202025-10-16%20at%2014.29.39.jpeg)

