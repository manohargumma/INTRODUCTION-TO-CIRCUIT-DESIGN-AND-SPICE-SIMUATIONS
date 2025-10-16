#  Voltage Transfer Characteristics: SPICE Simulations 
For a **CMOS inverter**, the **SPICE deck** includes:

- **Component Connectivity:** Define connections between components like **PMOS**, **NMOS**, **Vdd**, **Vss**, and **Vin/Vout**. 
- **Component Values:** Specify values for components such as **threshold voltages (Vth)**, **transistor sizes**, and **supply voltages**.
- **Identify Nodes:** Identify all electrical nodes like **Vin**, **Vout**, **source**, **drain**, and **bulk** for both transistors.
- **Name Nodes:** Assign names to each node, ensuring clear identification during simulations (e.g., **Vout** for the output node).
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/931a2bdce0f0a3debb588666d832a32fe13c7fdb/DAY3/day3pics/Screenshot%20from%202025-10-16%2021-39-24.png)
### SPICE simulation for CMOS inverter
SPICE Netlist for CMOS Inverter 
A **SPICE netlist** for a CMOS inverter includes transistor models, power supply connections, input voltage source, transistor specifications (PMOS and NMOS), and simulation commands (e.g., `.tran` for transient analysis).
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/931a2bdce0f0a3debb588666d832a32fe13c7fdb/DAY3/day3pics/Screenshot%20from%202025-10-16%2021-39-58.png)
Same Wn/Ln = Wp/Lp = 1.5. Plot out vs in:
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/931a2bdce0f0a3debb588666d832a32fe13c7fdb/DAY3/day3pics/Screenshot%20from%202025-10-16%2021-43-20.png)

## **Static Behavior Evaluation: CMOS Inverter Robustness and Switching Threshold (Vm)**  
The **switching threshold (Vm)** is the point where **Vin = Vout**, and both transistors are in saturation (since **Vds = Vgs**). At **Vm**, maximum power is drawn due to large current, and it can be graphically found at the intersection of the **VTC** with the **Vin = Vout** line. The analytical expression for **Vm** is obtained by equating the drain currents of PMOS and NMOS (**IDSn = IDSp**).

![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/931a2bdce0f0a3debb588666d832a32fe13c7fdb/DAY3/day3pics/Screenshot%20from%202025-10-16%2021-44-19.png)
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/931a2bdce0f0a3debb588666d832a32fe13c7fdb/DAY3/day3pics/Screenshot%20from%202025-10-16%2021-44-45.png)

In the **velocity-saturated** case, the **switching threshold (Vm)** is the point where both **NMOS** and **PMOS** transistors are in saturation, and the drain currents are equal. This occurs when the **VDS** of both devices is less than the saturation voltage, i.e., **VDSAT < (Vm − VT)**. The threshold voltage **Vm** can be derived by equating the drain currents of both transistors, with the device widths and lengths (W/L ratios) playing a key role in determining the point where both transistors conduct equally.

![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/931a2bdce0f0a3debb588666d832a32fe13c7fdb/DAY3/day3pics/Screenshot%20from%202025-10-16%2021-45-51.png)
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/931a2bdce0f0a3debb588666d832a32fe13c7fdb/DAY3/day3pics/Screenshot%20from%202025-10-16%2021-46-19.png)
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/931a2bdce0f0a3debb588666d832a32fe13c7fdb/DAY3/day3pics/Screenshot%20from%202025-10-16%2021-48-04.png)
---

## Velocity Saturation and Switching Threshold (Vm) Analysis

- **Case 1: Velocity Saturation Occurs**  
  - Happens in short-channel devices or high supply voltage.  
  - Switching threshold **Vm** occurs when currents of PMOS and NMOS transistors are equal.  
  - The ratio **r** (PMOS to NMOS strength) influences **Vm**.  
  - For **Vm ≈ VDD/2**, **r ≈ 1**.  
  - **Vm** can be adjusted by changing the PMOS or NMOS width:  
    - Increase PMOS width → shift **Vm** upwards.  
    - Increase NMOS width → shift **Vm** downwards.  

- **Case 2: Velocity Saturation Does Not Occur**  
  - Applies to long-channel devices or low supply voltage.  
  - The switching threshold **Vm** is still affected by **r** but with a simpler formula.  
  - If **r ≈ 1**, **Vm** is near **VDD/2**.

- **PMOS Width Effect on VTC**  
  - Increasing PMOS width shifts **Vm** upwards.  
  - Increasing NMOS width shifts **Vm** downwards.  
  - **Vm** is relatively stable with small variations in transistor ratios.

![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/1007403bf643e51b75e9906e83a9e1f0188b6369/DAY3/day3pics/Screenshot%20from%202025-10-16%2021-54-58.png)
### Applications of CMOS inverter in clock network and STA
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/1007403bf643e51b75e9906e83a9e1f0188b6369/DAY3/day3pics/Screenshot%20from%202025-10-16%2021-55-45.png)
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/1007403bf643e51b75e9906e83a9e1f0188b6369/DAY3/day3pics/Screenshot%20from%202025-10-16%2021-56-15.png)
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/1007403bf643e51b75e9906e83a9e1f0188b6369/DAY3/day3pics/Screenshot%20from%202025-10-16%2021-56-38.png)
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/1007403bf643e51b75e9906e83a9e1f0188b6369/DAY3/day3pics/Screenshot%20from%202025-10-16%2021-56-44.png)
# LABS-3
## 1. Voltage transfer characteristics: SPICE simulations
#### Sky130 SPICE simulation for CMOS - VTC

```bash



     
.param temp=27


*Including sky130 library files
.lib "sky130_fd_pr/models/sky130.lib.spice" tt


*Netlist Description


XM1 out in vdd vdd sky130_fd_pr__pfet_01v8 w=0.84 l=0.15
XM2 out in 0 0 sky130_fd_pr__nfet_01v8 w=0.36 l=0.15


Cload out 0 50fF

Vdd vdd 0 1.8V
Vin in 0 1.8V

*simulation commands

.op

.dc Vin 0 1.8 0.01

.control
run
setplot dc1
display
.endc

.end

 ```       
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/adf92648afa74771e56fa76a69d2d8d43c95923c/DAY3/day3pics/Screenshot%20from%202025-10-16%2022-21-12.png)
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/adf92648afa74771e56fa76a69d2d8d43c95923c/DAY3/day3pics/Screenshot%20from%202025-10-16%2022-21-32.png)
- **Switching Threshold (VM):**  
  The input voltage (**Vin**) at which the output voltage (**Vout**) equals the input voltage.  
  - It is the intersection point on the Voltage Transfer Curve (VTC).  
  - Also referred to as the **midpoint voltage** of the CMOS inverter.

  ### Sky130 SPICE simulation for CMOS - Transient Analysis
```bash

*Model Description
.param temp=27


*Including sky130 library files
.lib "sky130_fd_pr/models/sky130.lib.spice" tt


*Netlist Description


XM1 out in vdd vdd sky130_fd_pr__pfet_01v8 w=0.84 l=0.15
XM2 out in 0 0 sky130_fd_pr__nfet_01v8 w=0.36 l=0.15


Cload out 0 50fF

Vdd vdd 0 1.8V
Vin in 0 PULSE(0V 1.8V 0 0.1ns 0.1ns 2ns 4ns)

*simulation commands

.tran 1n 10n

.control
run
.endc

.end


     

 ```   
  ![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/0b4d5b25ac94c10d92a98653432af855bafa745f/DAY3/day3pics/Screenshot%20from%202025-10-16%2012-20-46.png)
  ![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/0b4d5b25ac94c10d92a98653432af855bafa745f/DAY3/day3pics/Screenshot%20from%202025-10-16%2012-23-47.png)
  ![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/0b4d5b25ac94c10d92a98653432af855bafa745f/DAY3/day3pics/Screenshot%20from%202025-10-16%2012-25-03.png)
- **Propagation Delay:**  
  The time difference (measured at 50% of input-output transition) between the input signal change and the corresponding output signal switch in a logic gate (e.g., inverter).
