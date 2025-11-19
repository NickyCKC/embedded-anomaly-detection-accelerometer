# Embedded Real-Time Accelerometer Anomaly Detection

## 🎯 Project Overview

During my internship, I developed a **real-time embedded anomaly detection system** using:

- **STM32H5 microcontroller**
- **ISM330DHCX 6-axis IMU (accelerometer + gyroscope)**
- **NanoEdge AI Studio anomaly detection model**
- **USB CDC data streaming**
- **Python visualization & monitoring GUI**

The system performs real-time data acquisition, inference, anomaly detection, and live visualization through a custom desktop application.

This repo documents:
- System architecture  
- Sensor pipeline  
- AI detection pipeline  
- GUI tooling  
- Firmware responsibilities  
- Engineering challenges & solutions  
- Skills demonstrated  

---

## 🧩 System Architecture

```mermaid
flowchart LR
    IMU[ISM330DHCX Accelerometer] --> FIFO[FIFO Data Collection]
    FIFO --> MCU[STM32H5 MCU]
    MCU --> AI[NanoEdge AI Anomaly Model]
    AI --> USB[USB CDC Data Stream]
    USB --> GUI[Python Real-Time GUI]
    GUI --> User[User]
