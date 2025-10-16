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
**Drift Current:** Current caused by a potential difference across the material.<br>
**Diffusion Current:** Current resulting from a difference in carrier concentration.<br>
**Cox:** A constant value provided by the foundry, representing oxide capacitance.
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/fdf814f8fbf32443b619fdbd06ead3203ec73b3f/pics/Screenshot%20from%202025-10-16%2015-06-58.png)
## Drain current model for linear region of operation
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/fdf814f8fbf32443b619fdbd06ead3203ec73b3f/pics/Screenshot%20from%202025-10-16%2015-07-56.png)
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/fdf814f8fbf32443b619fdbd06ead3203ec73b3f/pics/Screenshot%20from%202025-10-16%2015-10-18.png)
### SPICE Conclusion to Resistive Operation:
SPICE simulations allow us to calculate the drain current (Id) for different Vgs values by sweeping Vds for each Vgs until Vgs - Vt is reached. This helps in generating accurate Id-Vds curves and understanding the transistor's behavior.

### Saturation Region/Pinch-off Region Condition:
In the saturation (or pinch-off) region, the drain current Id becomes independent of Vds and depends only on Vgs, as long as Vds ≥ Vgs - Vt. This is where the transistor is fully "on" and conducting.
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/77528146a0683120084893ccda1b50edaa12d5cf/pics/Screenshot%20from%202025-10-16%2015-13-16.png)
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/77528146a0683120084893ccda1b50edaa12d5cf/pics/Screenshot%20from%202025-10-16%2015-13-24.png)
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/77528146a0683120084893ccda1b50edaa12d5cf/pics/Screenshot%20from%202025-10-16%2015-13-35.png)
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/a6590f7b41f8a80a61ec1554158dd33047b1fda9/pics/Screenshot%20from%202025-10-16%2015-14-38.png)
## SPICE equations
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/a6590f7b41f8a80a61ec1554158dd33047b1fda9/pics/Screenshot%20from%202025-10-16%2015-15-00.png)
## spice parameters 

![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/a6590f7b41f8a80a61ec1554158dd33047b1fda9/pics/Screenshot%20from%202025-10-16%2015-15-11.png)
## Spice setup
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/a6590f7b41f8a80a61ec1554158dd33047b1fda9/pics/Screenshot%20from%202025-10-16%2015-15-18.png)
## Spice netlist 
***SPICE Netlist Example:*** <br>

->M1 vdd n1 0 0 nmos W=1.8u L=1.2u: Defines an NMOS transistor with gate width 1.8µ and length 1.2µ, connecting vdd (drain), n1 (gate), 0 (source and substrate).<bf>
->R1 in n1 55: Defines a resistor with value 55Ω between in and n1.<br>
->Vdd vdd 0 2.5: Defines a voltage source of 2.5V between vdd and ground (0).<br>
->Vin in 0 2.5: Defines an input voltage source of 2.5V between in and ground (0).
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/a6590f7b41f8a80a61ec1554158dd33047b1fda9/pics/Screenshot%20from%202025-10-16%2015-16-07.png)
## Spice Technologiefile 
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/d5a792ebdbd8f5cfa443a4e204bf8d461190b68d/pics/Screenshot%20from%202025-10-16%2015-16-46.png)
## Simulation Commands
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/d02388f50b45b9ee5c3b4c302f6cd112e409b6f6/pics/Screenshot%20from%202025-10-16%2015-17-22.png)
# LAB-1
## 1. Introduction to SPICE

SPICE (Simulation Program with Integrated Circuit Emphasis) is a powerful tool used for simulating the behavior of electronic circuits. It allows circuit designers to analyze and validate designs before fabrication by providing insights into performance metrics such as voltage, current, and power consumption.

## 2.SPICE Lab with Sky130 Models<br>

To use SPICE with Sky130 technology, you can clone the relevant GitHub repository containing Sky130 models and circuits for simulation.
**Clone the repo:**<br>
Clone the repository with the following command:

```bash
git clone https://github.com/kunalg123/sky130CircuitDesignWorkshop.git
```
## 3.Important Files in the Repo:

1./sky130CircuitDesignWorkshop/design/sky130_fd_pr/cells/nfet_01v8/sky130_fd_pr__nfet_01v8__tt.pm3.spice<br>
This file contains the SPICE model for the NFET (N-channel MOSFET) in the Sky130 process at typical (tt) conditions.<br><br>

2./sky130CircuitDesignWorkshop/design/sky130_fd_pr/cells/nfet_01v8/sky130_fd_pr__nfet_01v8__tt.corner.spice<br>
This file provides the corner model for the NFET, used for simulating different process variations.<br><br>

3./sky130CircuitDesignWorkshop/design/sky130_fd_pr/models/sky130.lib.pm3.spice<br>
This library file contains all the SPICE models for components in the Sky130 process node.<br><br>
## EXAMPLE

```bash
*Model Description
.param temp=27


*Including sky130 library files
.lib "sky130_fd_pr/models/sky130.lib.spice" tt


*Netlist Description



XM1 Vdd n1 0 0 sky130_fd_pr__nfet_01v8 w=5 l=2

R1 n1 in 55

Vdd vdd 0 1.8V
Vin in 0 1.8V

*simulation commands

.op
.dc Vdd 0 1.8 0.1 Vin 0 1.8 0.2

.control

run
display
setplot dc1
.endc

.end
```
## To plot the waveforms in ngspice

```bash
$cd /VLSI/sky130CircuitDesignWorkshop/design
$ ngspice day1_nfet_idvds_L2_W5.spice
--->plot -vdd#branch
```
## The plot of Ids vs Vds over constant Vgs:
![image](https://github.com/manohargumma/Post-Synthesis-GLS-STA-Fundamentals/blob/7e1e3a0769f7f19e38580a00c6c3442d4775182d/Screenshot%20from%202025-10-16%2016-05-03.png)
![image](https://github.com/manohargumma/Post-Synthesis-GLS-STA-Fundamentals/blob/7e1e3a0769f7f19e38580a00c6c3442d4775182d/Screenshot%20from%202025-10-16%2016-05-09.png)
