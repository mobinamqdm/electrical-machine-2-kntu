# AC Current Measurement Using Arduino and CT Sensor

This repository contains the **final project for the Electrical Machines I course** at **K. N. Toosi University of Technology**, instructed by **Dr. Ramin Alipour**.  
The project demonstrates the **design and implementation of a safe, low-cost AC current measurement system** using an **Arduino**, **current transformer (CT) sensor**, and **signal conditioning circuit**.

---

## 📘 Project Overview
In this project, we designed a compact and non-intrusive AC current measurement circuit capable of safely measuring the RMS current of AC loads.  
The system uses a **Current Transformer (CT)** sensor with an **LM358 operational amplifier** for signal conditioning and displays the current value in real time on a **16x2 LCD (I2C interface)**.

The design replicates the fundamental principle of commercial **clamp ammeters**—allowing measurement without breaking the AC line—while maintaining **safety, accuracy, and educational value**.

This project bridges theory and practice by combining **analog circuit design**, **signal conditioning**, and **embedded systems programming** in a real-world engineering context.

---

## 🎯 Objectives
- **Safe AC Current Measurement:** Develop a circuit that measures AC current without directly interfacing with high voltage.  
- **Practical Understanding of CT Sensors:** Demonstrate how CT sensors can be used for non-intrusive current measurement.  
- **Signal Conditioning:** Amplify and stabilize CT output using an **LM358 op-amp**, **burden resistor**, **Zener/Schottky diodes**, and **capacitors**.  
- **Microcontroller Processing:** Use **Arduino Uno** to calculate RMS current and display results on an **LCD**.  
- **Validation:** Compare measured values with **analog** and **clamp ammeters** to verify system accuracy.  

---

## 📊 Key Results and Analysis

| Measurement Method | Measured Current (A) |
|:--------------------|:--------------------:|
| Theoretical (cosϕ = 1) | 0.45 |
| Analog AC Ammeter | 0.39 |
| Clamp Ammeter | 0.33 |
| Arduino + CT System | 0.344 |

**Performance Highlights**
- The Arduino + CT readings matched **commercial clamp meters** within a **5% error margin**.  
- The system achieved **stable, real-time current readings** (updated every 300 ms).  
- Demonstrated **linear response** across load variations (tested for 40 W, 60 W, and 100 W lamps).  
- Achieved **excellent repeatability** (variation < ±0.01 A across repeated tests).  
- Verified safety and reliability using isolated sensing and protective diodes.

> ✅ The system successfully validated that low-cost, Arduino-based measurement circuits can safely and accurately replicate the performance of laboratory-grade current meters.

---

## 🧩 Repository Structure
```bash
electrical-machines-1-project/
├─ arduino-code/
│  └─ ac_current_measurement.ino          # Arduino source code (RMS current computation)
│
├─ circuit-design/
│  ├─ schematic.png                        # Circuit diagram (CT, LM358, protection)
│  └─ wiring-breadboard.jpg                # Breadboard wiring photo
│
├─ report/
│  └─ electrical-machine-1-final-project-report.pdf
│
├─ demo/
│  └─ ac_current_measurement_demo.mp4     # Video demonstration of the project in action
│
└─ README.md
