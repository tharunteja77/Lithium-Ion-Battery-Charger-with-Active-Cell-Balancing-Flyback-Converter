# Lithium-Ion-Battery-Charger-with-Active-Cell-Balancing-Flyback-Converter

This project focuses on designing and implementing a **Battery Management System (BMS)** for a 3-cell Li-ion battery pack. The system uses an **isolated Flyback DC–DC converter** with **active cell balancing**, **CC–CV charging strategy**, and a **PID-based control loop** implemented on an Arduino platform.

## Introduction
Battery Management Systems (BMS) are critical for the safe and optimal operation of battery packs, especially in electric vehicles (EVs). Early BMS designs provided basic monitoring and protection; modern systems now include advanced features like state-of-charge (SoC) estimation, state-of-health (SoH) monitoring, and cell balancing. These functionalities prevent individual cell overloading, thus enhancing safety and performance.

## Project Overview
The demand for efficient, safe, and fast charging solutions for Li-ion batteries is growing rapidly. This project aims to:
- Achieve **accurate charging** with **constant-current (CC)** and **constant-voltage (CV)** modes.
- Implement **active balancing** using a flyback transformer, redistributing energy between cells to extend battery life.
- Ensure **isolation and safety** through an opto-isolated gate driver and flyback topology.
- Validate the system through **MATLAB simulation** and **hardware implementation**.

### 🔹 Key Features
- **Closed-loop PID Control**:
  - Proportional-Integral-Derivative controller for accurate voltage and current regulation.
  - Runs on Arduino UNO, with real-time computation and PWM modulation.
- **Flyback Converter Topology**:
  - Provides **galvanic isolation** and supports multiple secondary windings for active balancing.
  - Designed for efficiency and safety in Li-ion charging applications.
- **Active Cell Balancing**:
  - Balances individual cell voltages during charging, improving battery lifespan and performance.
- **Real-Time Monitoring**:
  - Voltage and current sensing using **ACS712** and voltage dividers.
  - LCD display for user-friendly parameter visualization.
- **Safety and Reliability**:
  - Opto-isolated gate driver (TLP250) for safe MOSFET switching.
  - PWM switching at **25 kHz** for smoother control.

### 🛠️ Technologies
- **Hardware:** Arduino UNO, Current Sensor (ACS712), Flyback transformer, MOSFET, Opto-isolator.
- **Software:** Arduino IDE (C++), MATLAB/Simulink.

## 🛠️ System Design
- **Input**: DC power source (e.g., 24 V supply).
- **Output**: 3-cell Li-ion battery pack (nominal 11.1 V).
- **Converter**: Flyback DC–DC converter with transformer isolation.
- **Control**: PID-based regulation, switching between CC and CV modes automatically.

### Key Design Elements:
- **Transformer Design**:
  - Calculated primary/secondary turns ratio based on output requirements.
  - Selected ferrite core for minimal losses and high-frequency operation.
- **PID Controller**:
  - Tuned values: Kp = 2, Ki = 0.9, Kd = 0.5.
  - Handles load variations and maintains stability.


  ---

## 📐 Technical Specifications
| Parameter         | Value           |
|--------------------|---------------|
| PWM Frequency      | 25 kHz        |
| Converter Topology | Flyback       |
| Control Algorithm  | PID (CC–CV)   |
| Input Voltage      | 24 V          |
| Output Voltage     | 12.6 V (3S)   |
| Microcontroller    | Arduino UNO   |

---

## 📊 Simulation and Testing
- **Simulation**: Conducted in **MATLAB/Simulink** to validate control performance under varying load and input conditions.
- **Hardware Prototype**:
  - Verified CC–CV transition and balancing functionality.
  - Measured minimal overshoot and stable response to disturbances.
