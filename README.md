# 🤖 Multi-Utility Rescue Robotic System

A compact, multi-utility **rescue robot** designed for **public safety**, **environmental monitoring**, and **remote surveillance** using **IoT**, **Python interface**, and **Blynk platform**. Built to operate in hazardous or inaccessible environments like **airports**, **railway stations**, **fire zones**, **mines**, and **industrial sectors**.

---

## 🌟 Project Overview

This project integrates:
- 🤖 Autonomous robot navigation
- 📡 Real-time sensor data collection
- 📲 Remote monitoring and control (via smartphone app or PC)
- 🧠 Predictive analytics for early anomaly detection

### Architecture:
- **Frontend**: Python-based GUI  
- **Backend**: Embedded C for motion and sensor logic  
- **Microcontroller**: NodeMCU ESP8266 (IoT-enabled)

---

## 🚀 Key Features

- 🔥 Fire Detection  
- 🌡️ Temperature & Humidity Monitoring  
- 💣 Explosive Gas Detection  
- 🧲 Metal Detection  
- 📶 Real-Time IoT Communication (via Blynk)  
- 📱 Smartphone App Control (Blynk)  
- 🧠 Cloud-Based Event Logging  
- 🕹️ Robot Motion Control (Forward, Backward, Left, Right)  
- 📊 Predictive Alerts via Blynk Events  

---

## 🔧 Components Used

| Component         | Description                                       |
|------------------|---------------------------------------------------|
| **NodeMCU ESP8266** | Microcontroller with built-in Wi-Fi             |
| **Temperature Sensor** | Detects surrounding heat/fire             |
| **Humidity Sensor**    | Monitors atmospheric moisture             |
| **Gas Sensor (MQ2)**   | Detects presence of explosive gases       |
| **Flame Sensor**       | Fire proximity detection                  |
| **Metal Detector Coil**| Detects hidden metals                     |
| **Servo Motor**        | Used for robotic arm or camera movement   |
| **Python GUI**         | Desktop live monitoring                   |
| **Blynk IoT App**      | Mobile control & monitoring               |
| **Embedded C**         | Sensor + Motion control logic             |

---

## 🔧 Backend: Robot Motion & Sensor Control

The backend code is written in **Embedded C using Arduino IDE** and handles:

- Sensor input readings
- Robot movement logic
- Servo motor control
- Buzzer alerts
- Wireless communication with the Blynk IoT platform

### 🔌 Motion Control via Blynk

The robot can be controlled remotely using Blynk app buttons:

| Virtual Pin | Action          |
|-------------|------------------|
| V0          | Move Forward     |
| V1          | Move Backward    |
| V2          | Turn Left        |
| V3          | Turn Right       |
| V8          | Servo Position   |

### 📊 Sensor Data Upload

Sensor readings are sent every second:
- V4: Gas Level  
- V5: Fire Proximity  
- V6: Temperature  
- V7: Metal Detection  

### ⚠️ Sample Events Triggered

- Metal detected → `Warning!! Metal Presence Detected!!`
- Explosive gas detected → `Warning!! Explosive Material Detected!!`
- Fire detected → `Warning!! Fire Detected!!`

---

## 📡 How It Works

1. Sensors collect environmental data.
2. NodeMCU processes inputs and uploads to Blynk server.
3. Blynk app displays alerts & enables robot movement.
4. Python GUI or smartphone app shows real-time data.

---

## 🧠 Applications

- 🚨 Public Area Safety (airports, stations)  
- 🔥 Fire Monitoring in risky zones  
- 🏭 Industrial Gas & Temperature Monitoring  
- 🛑 Bomb/Metal Detection in secured zones  
- ⛏️ Mining or cave exploration  
- 🕳️ Disaster rescue support  

---

## 📲 Live Monitoring Interfaces

- 💻 **Python GUI** (for desktop)
- 📱 **Blynk IoT App** (for Android/iOS)

---

## 🛠️ Technologies Used

- **Languages**: Python, Embedded C  
- **Microcontroller**: NodeMCU ESP8266  
- **IoT Platform**: Blynk  
- **GUI Framework**: Tkinter / PyQt  
- **Sensors**: DHT11, MQ2, Flame Sensor, Metal Detector  

---

## 📦 Future Enhancements

- 🎯 AI-based object detection and decision support  
- 🛰️ GPS integration for live location tracking  
- 🎥 Camera module for live video feed  

---

## 📁 Backend Code Snippet (Example)

```cpp
BLYNK_WRITE(V0) {
  int i = param.asInt();
  if (i == 1) {
    digitalWrite(M0, HIGH);
    digitalWrite(M1, LOW);
    digitalWrite(M2, LOW);
    digitalWrite(M3, HIGH);
  } else {
    digitalWrite(M0, LOW);
    digitalWrite(M1, LOW);
    digitalWrite(M2, LOW);
    digitalWrite(M3, LOW);
  }
}






