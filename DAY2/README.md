# SPICE SIMULATION FOR LOWER NODES AND VELOCITY SATURATION EFFECT 
## SPICE simulation for lower nodes
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/085b8ac49709be6198dfbf45c04ad9e796a6bf14/DAY2/picslab2/Screenshot%20from%202025-10-16%2016-18-49.png)
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/085b8ac49709be6198dfbf45c04ad9e796a6bf14/DAY2/picslab2/Screenshot%20from%202025-10-16%2016-22-07.png)
For ***long-channel devices,*** drain current shows a quadratic dependence on gate voltage.
For ***short-channel devices***, it is quadratic at low gate voltage but becomes ***linear at higher voltages***due to velocity saturation.
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/085b8ac49709be6198dfbf45c04ad9e796a6bf14/DAY2/picslab2/Screenshot%20from%202025-10-16%2017-16-48.png)
At ***lower electric fields***, carrier velocity increases ***linearly*** with the electric field.<br>
At ***higher electric fields***, velocity ***saturates*** and becomes ***constant*** due to ***velocity saturation***
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/085b8ac49709be6198dfbf45c04ad9e796a6bf14/DAY2/picslab2/Screenshot%20from%202025-10-16%2017-17-03.png)
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/085b8ac49709be6198dfbf45c04ad9e796a6bf14/DAY2/picslab2/Screenshot%20from%202025-10-16%2017-17-15.png)
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/085b8ac49709be6198dfbf45c04ad9e796a6bf14/DAY2/picslab2/Screenshot%20from%202025-10-16%2017-17-33.png)
### Velocity Saturation Drain Current Model:

1.***Technology Parameter: ***Saturation voltage (Vdsat) – the voltage at which carrier velocity saturates, independent of ***Vgs*** or ***Vds***.<br>
2.***Vgt*** is minimum → FET is in ***saturation region*** (both long and short channel).<br>
3.***Vds*** is minimum → FET is in ***linear region***(both long and short channel).<br>
4.***Vdsat*** is minimum → FET ***velocity saturates***(only for short channel)<br>
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/085b8ac49709be6198dfbf45c04ad9e796a6bf14/DAY2/picslab2/Screenshot%20from%202025-10-16%2017-18-14.png)
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/085b8ac49709be6198dfbf45c04ad9e796a6bf14/DAY2/picslab2/Screenshot%20from%202025-10-16%2019-51-30.png)
### OBSERVATIONS:
**Observation 1:** For short-channel devices, at higher electric fields, the device enters velocity saturation, causing Ids to remain constant as ***Vds*** increases. Here, Ids becomes a linear function of ***Vgs***, unlike the quadratic dependence in long-channel devices.<br>

**Observation 2:**  ***Velocity saturation*** causes the device to ***saturate earlier.***
## CMOS Voltage Transfer Characteristics (VTC):
1.Vout is ***high*** when Vin is ***low***, and Vout is ***low*** when Vin is ***high***.<br>
2. The ***transition region*** shows a steep drop where both NMOS and PMOS conduct, defining the switching threshold.<br>
### MOSFET as a switch
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/26a49b000ed74f5bb71d578b56a816e01cf15925/DAY2/picslab2/Screenshot%20from%202025-10-16%2019-53-23.png)
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/26a49b000ed74f5bb71d578b56a816e01cf15925/DAY2/picslab2/Screenshot%20from%202025-10-16%2019-53-51.png)
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/26a49b000ed74f5bb71d578b56a816e01cf15925/DAY2/picslab2/Screenshot%20from%202025-10-16%2019-54-41.png)
### Introduction to Standard MOS Voltage-Current Parameters:
In MOS devices, Rp (PMOS) and Rn (NMOS) act as ***non-linear resistors***, where their resistance is a ***function of drain current (Ids)***, influenced by gate voltage (Vgs) and drain voltage (Vds)
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/f3e88a282f1b4ca904af57f51dd65c3c80267bb8/DAY2/picslab2/Screenshot%20from%202025-10-16%2019-55-11.png)
### PMOS/NMOS Drain Current vs. Drain Voltage:



1. **Linear Region (Vds < Vdsat):**
   - Drain current (**Ids**) increases *linearly* with **Vds**.  
   - Device behaves like a **resistor** controlled by **Vgs**.

2. **Saturation Region (Vds > Vdsat):**
   - Drain current (**Ids**) becomes **constant** and independent of **Vds**.  
   - For **NMOS**, Ids depends on **Vgs - Vth**.  
   - For **PMOS**, Ids depends on **Vth - Vgs**.


![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/9bcf3eb89b27daca5b438e80e39f71ed7f8f3331/DAY2/picslab2/Screenshot%20from%202025-10-16%2019-56-02.png)   
***Step1. Convert PMOS gate-source voltage to Vin.***
  -Replace internal node voltages with ***Vin***, ***Vdd***, ***Vss***, and ***Vout***.<br>
  -Simulate and plot the ***VTC*** by varying ***Vin*** and analyzing Vout. 

![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/aaeca61942eaf3259b2a3003875ccce1a9946b7a/DAY2/picslab2/Screenshot%20from%202025-10-16%2019-57-48.png)


 
. **Step 2 & Step 3:**
   - Convert PMOS and NMOS drain-source voltages to ***Vout***
   -  Relate the drain-source voltages of both devices to the output voltage (Vout) by considering their respective operating regions (linear or saturation). 
   ![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/b00b68500fcfa2d6dcdfd79179f482d8e0138601/DAY2/picslab2/Screenshot%20from%202025-10-16%2019-58-23.png)

. **Step 4:**
   -  ***Merge the PMOS and NMOS load*** curves by combining their drain current (Ids) characteristics with respect to Vout.
   -  ***Plot the Voltage Transfer Characteristic (VTC)*** by mapping Vout against Vin, showing the transition from low to high output          voltage.
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/818c40415bb9b0160cb82bb03fd51f2c483970c5/DAY2/picslab2/Screenshot%20from%202025-10-16%2019-59-39.png)
#  LAB-2
## SPICE simulation for lower nodes and velocity saturation effect
### Sky130 Id-Vgs
***EXAPLE1***:
'''bash
assh

'''
