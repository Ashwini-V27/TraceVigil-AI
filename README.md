# TraceVigil-AI
###  The Immutable Intelligent Watchman for Global Trade
##  Table of Contents
* [Problem Statement](#-project-statement)
* [ Project Description](#-project-description)
* [ Proposed Solution](#-proposed-solution)
* [ Key Features](#-key-features)
* [ Software Stack](#-software-stack)
* [ Hardware Requirements](#-hardware-requirements)
* [ How It Works](#-how-it-works)
* [ Setup Instructions](#-setup-instructions)

##  Problem Statement
The global supply chain is currently "blind and vulnerable." Every year, the logistics industry loses over **\$50 Billion** due to spoilage, theft, and physical damage. Existing tracking solutions are **reactive** (notifying users after damage occurs) and **tamperable** (allowing data deletion to hide negligence).
### The Crisis in Numbers:
* **Perishables:** Up to **30%** of all exported produce is wasted before reaching the consumer due to thermal instability.
* **Sensitive Tech:** High-end semiconductors and EV batteries are frequently rendered defective by undetected micro-impacts during sea transit.
* **The "Blind" Spot:** Once a container leaves a warehouse, there is a total lack of **Accountability** regarding who opened the cargo, where, and when.

## Project Description

**TraceVigil-AI** addresses the three "Silent Killers" of global exports:

1.  **The Semiconductor & EV Battery Crisis:** High-precision electronics often suffer internal structural damage from rough handling. TraceVigil-AI uses high-fidelity vibration analysis to detect these "micro-fractures" in real-time.
2.  **Broken Cold Chains:** Moving beyond simple logging, our system utilizes a **Predictive Spoilage Velocity** algorithm. It analyzes thermal trends to predict remaining shelf-life, allowing for emergency rerouting before goods are lost.
3.  **Cargo Theft & Tampering:** By implementing **Blockchain-at-the-Edge**, we ensure that historical logs cannot be altered. Any attempt to hide a breach or a temperature spike will break the cryptographic hash chain.
   
 ##  Proposed Solution
TraceVigil-AI transforms standard shipping containers into **Self-Auditing Intelligent Nodes**:
* **Cryptographic Integrity:** Uses **SHA-256 Hashing** to chain every sensor reading, creating an unbreakable digital seal.
* **AI-Driven Prediction:** Real-time shelf-life forecasting based on environmental data.
* **Geofenced Authentication:** Integrated **RFID + GPS** ensures cargo is only accessed by authorized personnel at verified destination coordinates.
* **Resilient Edge Storage:** Utilizing **SPIFFS**, the system logs data during "Data Deserts" (deep-sea transit) and auto-syncs upon reconnection.

## Key Features
* **Predictive Spoilage:** Calculates temperature trends to estimate remaining shelf life.
* **Impact Sensing:** 6-axis motion analysis to detect drops or rough handling.
* **RFID Security:** Authorized-only access to cargo data and physical locking.
* **Data Integrity:** Uses SHA-256 hashing to ensure logs are tamper-proof.
* **Edge Defense:** Automatic offline data logging (SPIFFS) during network loss.

## Software Stack
* **Firmware:** Arduino C++ (MPU6050, DHT22, GPS, RFID, SPIFFS, SHA-256)
* **Backend:** Node.js + Express + MongoDB (JWT, bcrypt, nodemailer)
* **Frontend:** React 18 + Vite + Recharts + CSS-in-JS
* **Security:** JWT tokens, SHA-256 hash chain, and role-based access control.

 ## Hardware Requirements
* **Microcontroller:** ESP32 (Dual-core, WiFi/BT enabled)
* **Motion Sensor:** MPU6050 (Accelerometer + Gyroscope)
* **Environment:** DHT22 (High-accuracy Temp & Humidity)
* **Positioning:** Neo-6M GPS Module
* **Security:** RC522 RFID Module & Tags

## How It Works
1. **Sense:** Sensors gather vibration, temperature, and GPS coordinates.
2. **Process:** ESP32 calculates if an Impact Alert or Spoilage Warning is needed.
3. **Secure:** Data packets are signed with a SHA-256 hash to prevent tampering.
4. **Sync:** Data is sent via WiFi to MongoDB or stored in SPIFFS if offline.
5. **Monitor:** Users view live status and alerts via the React dashboard.


## Operational Workflow
The system provides dual-interface monitoring:
* **Admin Command Center:** Real-time logistics dashboard, predictive alerts, remote security commands, and PDF audit reporting.
* **Field Driver Alert:** Mobile-optimized view showing immediate operational alerts, shock impact warnings, and driver safety ratings.

## Setup Instructions

### 1. Hardware Connection
* **DHT22:** Pin 4
* **RFID (SDA/RST):** Pin 5 / Pin 2
* **GPS (RX/TX):** Pin 16 / Pin 17
* **MPU6050:** I2C (SDA 21, SCL 22)


### 2. Frontend Setup
```bash
cd frontend
npm install
npm start
```

### 3. Backend Setup
```bash
cd backend
npm install
npm run dev.
```





