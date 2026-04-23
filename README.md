# TraceVigil-AI
###  Smart IoT Ecosystem for High-Value Export & Cold Chain Accountability
##  Table of Contents
* [ Project Description](#-project-description)
* [ Key Features](#-key-features)
* [ Hardware Requirements](#-hardware-requirements)
* [ Software Stack](#-software-stack)
* [ How It Works](#-how-it-works)
* [ Setup Instructions](#-setup-instructions)


## Project Description
TraceVigil-AI is a next-generation Smart IoT Ecosystem designed for high-value exports and cold chain accountability. While standard trackers only show location, TraceVigil-AI provides a complete digital custody chain. By combining Edge Intelligence with MERN-stack connectivity, the system monitors cargo health, detects impacts, and predicts spoilage before it happens.

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

### 2. Backend Setup
```bash
cd backend
npm install
npm start.

### 3. Frontend Setup
cd frontend
npm install
npm start
