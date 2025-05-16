# EEE3088F 2025 Micro-Mouse Power Subsystem

## Project Overview
This repository contains the design files, documentation, and reports for the **Power Subsystem** of the EEE3088F 2025 Micro-Mouse project. The goal is to design a PCB that meets the strict power requirements for the Micro-Mouse robot while adhering to budget and mechanical constraints. The subsystem must power motors, manage battery charging, and provide regulated voltages, all within a compact form factor.

---

## Key Requirements
The power subsystem must fulfill the following **8 requirements**:

1. **Motor Control**  
   - Operate **4 motors** bidirectionally:  
     - 2x brushed DC motors (200mA each at max 1S1P battery voltage).  
     - 2x auxiliary motors (500mA each).  

2. **Battery Monitoring**  
   - Integrate an **INA219 current sensor** on the I2C bus.  
   - Ensure **A0 and A1 pins are not both grounded**.  

3. **Battery Charging**  
   - Charge the LiPo battery (800mAh, 3.7V) via the **9V input pin**.  

4. **Charging Modes**  
   - Support two charging currents:  
     - **200mA** (low mode).  
     - **600mA ±100mA** (high mode).  

5. **USB-C Integration**  
   - Extract **9V from a USB-C host** for charging.  

6. **External Load Switching**  
   - Provide **2x high-side switches** for external loads (1A each, connected to 5V).  

7. **Voltage Regulation**  
   - Deliver **3.3V ±5%** (300mA max) and **5V ±5%** (1.5A max).  

8. **Power Management**  
   - Include an **ON/OFF switch** with:  
     - **OFF state**: Battery draw <30µA.  
     - **ON state**: Handle peak current of 2A.  
     - Shut down 5V and 3.3V when OFF.  

---

## Additional Constraints
- **Budget**: Total component cost ≤ $56.5 (shared between two students).  
- **PCB Dimensions**: ≤82mm x 60mm (must fit under the motherboard).  
- **Connectors**:  
  - **JST PH 2mm** for battery.  
  - **2x16-pin header (2.54mm pitch)** for motherboard interface.  
  - **USB-C** connector.  
- **Testing**: Must interface with the provided testing jig for validation.  

---

## Repository Structure
This repository contains drafts schematics, GERBER and DRILL files that were used throughout this project
