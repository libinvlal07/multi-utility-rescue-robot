# 🤖 Multi-Utility Rescue Robot

A smart multi-sensor rescue system combining **Embedded C (NodeMCU)** for sensor control and **Python GUI** for offline data monitoring. Built for use in disaster-prone or hazardous areas to assist rescue operations by monitoring environmental conditions in real-time.

---

## 📌 Project Overview

The **Multi-Utility Rescue Robot** is equipped with multiple environmental sensors and a wireless data communication system. The robot collects real-time sensor data via a **NodeMCU microcontroller**, transmits it to a **web server** for live access on smartphones, and offers a **Python-based GUI** for offline access.

---

## ⚙️ Technologies Used

### 🖥️ Front-End Interface
- **Python GUI (Tkinter)**
  - User-friendly offline interface
  - Displays sensor data in real-time

### 🔧 Back-End Microcontroller
- **Embedded C on NodeMCU (ESP8266)**
  - Sensor data collection and processing
  - Wi-Fi communication to server/web app

---

## 🔍 Sensors Used

| Sensor                  | Description                                |
|-------------------------|--------------------------------------------|
| 🌡️ Temperature Sensor    | Monitors temperature levels               |
| 💧 Humidity Sensor       | Measures air humidity                     |
| 🔥 Fire Sensor           | Detects flames or fire presence           |
| 💨 Explosive Gas Sensor  | Detects flammable/explosive gases         |
| 🧲 Metal Detector        | Locates buried or hidden metallic objects |

---

## 🧠 System Architecture

```mermaid
graph TD
A[Sensor Array] --> B[NodeMCU ESP8266]
B --> C[Web Server / Smartphone View]
B --> D[Python GUI - Offline Monitoring]
