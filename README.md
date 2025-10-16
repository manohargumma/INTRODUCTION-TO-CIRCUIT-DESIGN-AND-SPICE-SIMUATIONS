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
**NMOS Transistor:** An N-type Metal-Oxide-Semiconductor that conducts when a positive voltage is applied to its gate, enabling current flow from drain to source.
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/12a6a2e72fd4a49e4dc2c94dbb4c4011f015b003/pics/Screenshot%20from%202025-10-16%2014-48-41.png)

**Threshold Voltage:** A key parameter that drives SPICE simulations, representing the voltage at which a transistor switches from off to on.

![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/12a6a2e72fd4a49e4dc2c94dbb4c4011f015b003/pics/Screenshot%20from%202025-10-16%2014-49-31.png)
**Strong Inversion:** The condition where the transistor channel is fully formed, allowing significant current flow.

**Threshold Voltage with Substrate Potential:** The threshold voltage varies with changes in substrate potential due to the body effect.
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/12a6a2e72fd4a49e4dc2c94dbb4c4011f015b003/pics/Screenshot%20from%202025-10-16%2014-49-48.png)
**Body Effect Coefficient and Fermi Potential:** Constants provided by the foundry that form the transistor model and are fed into SPICE simulations for various calculations.
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/fdf814f8fbf32443b619fdbd06ead3203ec73b3f/pics/Screenshot%20from%202025-10-16%2015-05-20.png)
## NMOS Resistive and Saturation Regions of Operation
Resistive region of operation with small drain-source voltage
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/fdf814f8fbf32443b619fdbd06ead3203ec73b3f/pics/Screenshot%20from%202025-10-16%2015-06-05.png)
**Drift Current:** Current caused by a potential difference across the material.
**Diffusion Current:** Current resulting from a difference in carrier concentration.
**Cox:** A constant value provided by the foundry, representing oxide capacitance.
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/fdf814f8fbf32443b619fdbd06ead3203ec73b3f/pics/Screenshot%20from%202025-10-16%2015-06-58.png)
## Drain current model for linear region of operation
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/fdf814f8fbf32443b619fdbd06ead3203ec73b3f/pics/Screenshot%20from%202025-10-16%2015-07-56.png)
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/fdf814f8fbf32443b619fdbd06ead3203ec73b3f/pics/Screenshot%20from%202025-10-16%2015-10-18.png)
