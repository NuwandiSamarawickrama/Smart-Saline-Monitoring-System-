# Smart Saline Monitoring System

## Project Overview

The **Smart Saline Monitoring System** is a hospital-grade solution designed to improve patient safety during IV fluid administration. The system continuously monitors saline bottles and IV lines, detecting issues such as empty bottles, air bubbles, disconnected lines, or abnormal flow rates. When a critical condition is detected, the system alerts medical staff and can automatically actuate an IV clamp to prevent backflow or other hazards.  

The project integrates **LabVIEW**, a **DAQ interface**, sensors, and actuators to provide real-time monitoring, control, and visualization.

---

## Key Features

- **Empty Bottle Detection:** Prevents backflow using a load cell to measure the saline bottle weight.  
- **Air Bubble Detection:** Optical sensors identify air bubbles in the IV line.  
- **Line Connection Verification:** Hall effect sensor ensures the IV line is properly connected.  
- **Abnormal Flow Monitoring:** Detects irregular flow rates due to bent or blocked tubing.  
- **Automated IV Clamp Control:** Servo motor closes the IV clamp when necessary.  
- **Real-Time Dashboard:** LabVIEW displays sensor readings, flow rate, and alerts for staff monitoring.  
- **Calibration & Alerts:** Supports sensor calibration and generates visual/audible warnings for unsafe conditions.  

---

## Hardware Components

- **Sensors:**
  - Load cell – Measures bottle weight.  
  - IR LED + photodiode – Detects air bubbles.  
  - Hall effect sensor – Checks IV line connection.  
- **Actuators:**
  - Servo motor – Controls the IV clamp.  
  - Audible/visual alarms – Alerts staff to unsafe conditions.  
- **Other Components:**
  - DAQ interface – Central platform for data acquisition and control.  
  - Arduino Uno – Collects selected sensor readings.  
  - Standard IV setup (bottle, tubing, clamp) and connecting wires.  

---

## Software Components

- **LabVIEW:** Real-time monitoring, sensor-actuator integration, alarm handling, and dashboard visualization.  
- **Arduino IDE:** Acquires sensor data and sends it to LabVIEW via the DAQ interface.  

---

## System Workflow

1. Sensors continuously collect data:
   - Load cell for bottle weight.  
   - IR LED + photodiode for air bubbles.  
   - Hall effect sensor for line connection.  
2. LabVIEW processes the data in real-time:
   - Compares readings to safety thresholds.  
   - Activates alarms for unsafe conditions.  
   - Controls the servo motor to automatically close the IV clamp if needed.  
   - Calculates IV flow rate and displays it on the dashboard.  
3. Staff can monitor all data via the LabVIEW interface and respond accordingly.  

---

## Setup Instructions

1. **Hardware:** Connect all sensors and actuators to the DAQ interface. Ensure proper power connections.  
2. **Arduino:** Upload sensor-reading code and verify data transmission to LabVIEW.  
3. **LabVIEW:** Open the VI files, configure DAQ channels, calibrate sensors, and link actuators.  
4. **Operation:** Run the system to monitor IV setup in real-time. Automatic responses and alerts handle unsafe conditions.  

---

## Future Enhancements

- Expand monitoring to multiple IV setups simultaneously.  
- Add wireless communication for remote monitoring and notifications.  
- Integrate additional sensors to monitor medication type, fluid consistency, or temperature.  

---

## License

This project is released under the **MIT License**. See `LICENSE` for details.
