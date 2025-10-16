
# **1. Static Behavior Evaluation: CMOS Inverter Robustness - Power Supply Variation**

**Overview:**  
- Power supply scaling affects the static behavior of the CMOS inverter, including the switching threshold, noise margins, and overall robustness.  

**Smart SPICE Simulation:**  
- Simulate the CMOS inverter across different supply voltage values (VDD).  
- Analyze how the voltage transfer characteristics (VTC) and critical parameters (like VM and noise margins) shift with varying power supply.  

**Key Observations:**  
1. As **VDD decreases**, the switching threshold (VM) may shift closer to the center of the supply range, but noise margins reduce.  
2. Lower power supply reduces overall noise immunity and can impact performance.  
3. At higher VDD, both static power dissipation and noise margins increase.  
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/3526082f4d3df354a55734577d121ce41107bbaf/DAY5/day5pics/Screenshot%20from%202025-10-16%2023-29-37.png)

### **Simulation Observations: Power Supply Variations**

1. **Robust Operation at Lower VDD:**  
   - The CMOS inverter operates effectively even at 0.8V, which is below half the original supply voltage (1.8V) and close to the transistor threshold voltages.

2. **Switching Threshold Proportionality:**  
   - With a fixed transistor ratio (*r*), the switching threshold (VM) is approximately proportional to VDD.

3. **Gain in Transition Region:**  
   - The inverter gain in the transition region increases as the supply voltage decreases.

4. **Transition Region Width:**  
   - The width of the transition region reduces when the supply voltage is scaled down from the original VDD.
   ![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/9dcd8cf59ba1818e62522444f883ea10a3e4da69/DAY5/day5pics/Screenshot%20from%202025-10-16%2023-30-33.png)
   ![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/9dcd8cf59ba1818e62522444f883ea10a3e4da69/DAY5/day5pics/Screenshot%20from%202025-10-16%2023-30-23.png)
### **Limitations of Operating at Low Supply Voltages**

1. **Performance Degradation:**  
   - Lowering the supply voltage reduces energy dissipation but significantly increases gate transition times, negatively affecting performance.

2. **Parameter Sensitivity:**  
   - At low supply voltages, the DC characteristics become highly sensitive to variations in device parameters, such as transistor threshold voltages.

3. **Reduced Signal Swing:**  
   - Scaling VDD reduces signal swing, lowering internal noise (e.g., crosstalk) but increasing sensitivity to external noise sources, which do not scale proportionally.
![imaage](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/9dcd8cf59ba1818e62522444f883ea10a3e4da69/DAY5/day5pics/Screenshot%20from%202025-10-16%2023-31-28.png)
### **CMOS Inverter Robustness to Device Variations**

1. **Design vs. Real Operating Conditions:**  
   - Gates are designed for nominal conditions, but actual operating temperatures and device parameters can vary widely after fabrication.

2. **DC Characteristics Stability:**  
   - The DC characteristics of the CMOS inverter are relatively insensitive to variations in device parameters, allowing the gate to remain functional across a broad range of operating conditions.

3. **Sources of Variation:**  
   - One common source of variation is the etching process during fabrication, which can affect device parameters.
   ### SOURCES OF ETCHING PROCESS
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/9dcd8cf59ba1818e62522444f883ea10a3e4da69/DAY5/day5pics/Screenshot%20from%202025-10-16%2023-36-34.png)
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/9dcd8cf59ba1818e62522444f883ea10a3e4da69/DAY5/day5pics/Screenshot%20from%202025-10-16%2023-36-57.png)
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/9dcd8cf59ba1818e62522444f883ea10a3e4da69/DAY5/day5pics/Screenshot%20from%202025-10-16%2023-37-32.png)
### Sources of variation: Oxide Thickness
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/9dcd8cf59ba1818e62522444f883ea10a3e4da69/DAY5/day5pics/Screenshot%20from%202025-10-16%2023-38-03.png)
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/9dcd8cf59ba1818e62522444f883ea10a3e4da69/DAY5/day5pics/Screenshot%20from%202025-10-16%2023-38-30.png)
# LABS-5
## Static behavior evaluation: CMOS inverter robustness, Power supply variation
### Smart SPICE simulation for power supply variations

![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/9dcd8cf59ba1818e62522444f883ea10a3e4da69/DAY5/day5pics/Screenshot%20from%202025-10-16%2023-34-51.png)
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/9dcd8cf59ba1818e62522444f883ea10a3e4da69/DAY5/day5pics/Screenshot%20from%202025-10-16%2023-33-18.png)
### **CMOS Inverter Robustness: Extreme Device Width Variation**

- **Robustness to Width Variation:**  
   The CMOS inverter remains functional even under extreme variations in device width (W) due to its static behavior properties.  

- **Effect on Switching Threshold:**  
   Large deviations in device width primarily affect the switching threshold \( V_M \) but do not drastically impact the inverter's ability to operate as a logic gate.  

- **Impact on Noise Margins:**  
   Variations in width cause asymmetry in the noise margins, with one margin (high or low) reducing while the other increases.

- **Key Insight:**  
   The CMOS inverter exhibits robust static behavior, tolerating extreme width variations without functional failure.

![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/fb25d9fc6de331b877b0bd3d2f7ff1aa052675b8/DAY5/day5pics/Screenshot%20from%202025-10-16%2023-57-50.png)
![image](https://github.com/manohargumma/INTRODUCTION-TO-CIRCUIT-DESIGN-AND-SPICE-SIMUATIONS/blob/fb25d9fc6de331b877b0bd3d2f7ff1aa052675b8/DAY5/day5pics/Screenshot%20from%202025-10-16%2023-58-43.png)
