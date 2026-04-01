# 🚗 CAN ECU Dashboard (STM32 | Multi-ECU System)

## 📖 Overview

The **CAN ECU Dashboard** project implements a **real-time automotive communication system** using the **CAN protocol** on **STM32 microcontrollers**.

The system consists of **3 ECU nodes** connected over a CAN bus, enabling real-time data exchange and dashboard visualization of vehicle parameters such as **Indicator status, speed, RPM, Temperature, Time and Gear Position**.

---

## 🎯 Key Highlights

* Real hardware implementation using **STM32 microcontrollers**
* Multi-node CAN communication with **3 ECU boards**
* Real-time data transmission and synchronization
* CAN protocol implementation (arbitration, error handling)
* Embedded system + automotive communication integration

---

## 🏗️ System Architecture

```text
ECU 1 (Sensor Node) ──┐
                      ├──► CAN Bus ───► ECU 3 (Dashboard Node)
ECU 2 (Control Node) ─┘
```

### 🔧 ECU Roles

* **ECU 1 (Sensor Node)**

  * Generates vehicle parameters (e.g.,Indicator, speed, RPM)

* **ECU 2 (Control Node)**

  * Sends control/status signals

* **ECU 3 (Dashboard Node)**

  * Receives CAN messages
  * Processes and displays data

---

## ⚙️ Features

* 📡 CAN communication across multiple ECUs
* 🔄 Real-time data transmission between nodes
* 🧠 Message encoding and decoding
* 📊 Dashboard display for:

  * Vehicle Speed
  * Engine RPM
  * Status Indicators
* ⚠️ Error detection and handling (CAN protocol)

---

## 🛠️ Hardware & Tools

### 🔌 Hardware

* STM32 Microcontrollers
* CAN Transceiver Modules
* 3 ECU Boards
* Connecting CAN Bus (twisted pair wiring)

### 💻 Software

* Embedded C
* STM32CubeIDE
* CAN Drivers / HAL Libraries

---

## 🧪 Implementation Details

* Configured CAN peripheral on STM32 (bit timing, filters)
* Implemented message IDs for different parameters
* Used interrupt-based CAN reception
* Designed structured data frames for communication
* Ensured synchronization between multiple ECUs

---

## 📂 Repository Structure

```text
CAN_ECU_Dashboard/
├── ecu1_sensor/        # Sensor node firmware
├── ecu2_control/       # Control node firmware
├── ecu3_dashboard/     # Dashboard node firmware
├── drivers/            # CAN drivers / HAL configs
├── docs/               # Documentation & diagrams
└── README.md
```

---

## ▶️ How to Run

1. Flash firmware to respective STM32 boards
2. Connect all ECUs via CAN bus
3. Power the system
4. Monitor data on dashboard node

---

## 📊 Results

* Reliable communication between 3 ECU nodes
* Real-time updates of vehicle parameters
* Stable CAN bus operation with proper arbitration
* Successful handling of message transmission and reception
