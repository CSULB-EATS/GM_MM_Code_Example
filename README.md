# 🐭 Micromouse Software Implementation

## Overview
This repository contains the **software side** of the CSULB-EATS Micromouse project.  
It includes **firmware, examples, and implementation guides** for building and testing a HAL-based embedded control system using the **NUCLEO-TOF400 (or similar STM32 board)**.  

The project is written in **C/C++** using the **STM32 HAL library**, structured for modularity and ease of testing.

---

## 🧩 Repository Structure

```
Micromouse-Firmware/
│
├── /Core/                  # STM32 HAL core files (system init, startup) This should be within the STM32CubeMX/IDE built-in
├── /Drivers/               # STM32 HAL drivers (GPIO, TIM, ADC, UART, etc.) This one as well *
|
├── /Examples/              # Example projects for hardware testing
│   ├── IR_Test/
│   ├── Motor_Test/
│   ├── Encoder_Test/
│   ├── IMU_Test/
│   └── UART_Debug/
│
└── README.md
```

---

## ⚙️ Setup & Requirements

### Hardware
- **Board:** STM32 Board Specific 

### Software
- **IDE:** STM32CubeIDE (or VS Code)
- **Libraries:** STM32 HAL, CMSIS
- **Debugging Tools:** ST-Link V2, logic analyzer (optional)
- **Version Control:** Git / GitHub

---

## 🚀 Getting Started

### 1. Open in STM32CubeIDE
```
File → Import → Existing Projects into Workspace
```

### 2. Build & Flash
Connect your board via USB and click **Run → Debug**.  
Verify your ST-Link configuration matches the NUCLEO-TOF400 target.

---

## 🧠 Key Features

- **Modular HAL Design:** Each subsystem (motors, sensors, encoders) isolated in its own BSP layer  
- **PID Control:** Tunable motor control with adjustable gain parameters  
- **Sensor Fusion:** Combines IMU and encoder data for precise movement  
- **Serial Debug:** UART logging for live telemetry and diagnostics  
- **Examples Provided:** Quick validation for hardware bring-up and driver testing  

---

## 🧭 Contributing
All modules follow the **HAL-based modular architecture** and should include:
- Header (`.h`) and source (`.c`) files  
- Initialization, configuration, and runtime functions  
- Clear documentation in `/Docs` for setup and testing  

Please follow existing naming conventions and formatting.

---

## 📄 License
This project is open-source for educational and research purposes.  
© 2025 CSULB Embedded Application Technology Society (EATS)
