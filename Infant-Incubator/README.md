# 👶 Smart Infant Incubator Monitoring System

A team-based biomedical engineering project designed to simulate and enhance infant incubator safety using real-time sensor-based monitoring and automated control.

---

## 📄 Project Overview
This system continuously monitors a simulated infant environment, measuring vital parameters like temperature, humidity, and heart rate.  
It ensures that the conditions inside the incubator stay within safe ranges, automatically activating alarms and ventilation systems if any abnormality is detected.

---

## 🔧 Features
- **Temperature & Humidity Monitoring**  
  DHT11 sensor constantly checks the incubator's internal climate to maintain a healthy environment.

- **Heart Rate Monitoring**  
  Pulse Sensor measures the infant's BPM (Beats Per Minute) and displays it on the screen.

- **Automatic Ventilation**  
  If temperature exceeds a safe threshold (> 35°C), a cooling fan is activated automatically.

- **Emergency Alerts**  
  If critical conditions are detected (e.g., high temperature), a buzzer sounds to alert caregivers immediately.

- **LCD Display**  
  Real-time updates of temperature, humidity, and heart rate on a 16x2 I2C LCD screen.

---


## 🖼️ System Images
- Final Prototype Photo
- ![WhatsApp Image 2025-05-03 at 04 38 06_2d5686a9](https://github.com/user-attachments/assets/db59fbd7-18dd-4614-b39f-6bbc3b6b6a02)

- Full Circuit Diagram
![ChatGPT Image 3 مايو 2025، 04_44_05 ص](https://github.com/user-attachments/assets/7085f619-6b9d-4613-9af1-864d43b08704)

---

## 💻 Code
All Arduino code is available inside the `/Code` directory, fully commented and modular.

---

## 📦 Hardware Components

| Component                | Purpose                                   |
|---------------------------|-------------------------------------------|
| Arduino UNO               | Main controller board                    |
| DHT11 Sensor              | Measures temperature and humidity        |
| Pulse Sensor              | Measures the infant’s heart rate (BPM)    |
| Fan (with motor driver)    | Ventilation and temperature regulation    |
| Buzzer                    | Emergency alert                          |
| Relay Module              | Control high-current devices (fan)       |
| LCD I2C 16x2              | Display sensor data in real-time         |
| Power Supply              | Provides reliable energy source          |

---

## 🤝 Teamwork
This project was developed collaboratively as part of our biomedical engineering coursework.  
We focused on improving infant safety using sensor integration, real-time monitoring, and automated intervention systems.

---

## 👥 Team Members
- Abdelrahman Emad Negm
- Muhammad Nasser
- Amat Alrahman Sayed
- Alaa Essam
- Farah Yehya
  
---
⭐ Star this repo if you find it useful or inspiring!
