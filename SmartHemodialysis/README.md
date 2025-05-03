

![Image](https://github.com/user-attachments/assets/0d274a75-7672-4039-86cf-557ef202e867)

# 🩸 Smart Hemodialysis Monitoring System

A team-based biomedical engineering project that simulates and enhances the safety of the hemodialysis process using real-time sensor-based monitoring.

##  Project Overview

This system was designed to simulate the blood filtration process used in hemodialysis while monitoring for **patient safety** using multiple sensors.  
It takes **blood** from the arm, simulates **filtration**, and then returns it — all while keeping track of critical parameters to ensure the patient's well-being during the session.

---

## 🔧 Features

-  **Blood Flow Simulation**: Blood is filtered and recirculated.
-  **GSR Sensor**: Monitors skin conductivity to detect patient stress or fatigue. If the patient is in distress, the system adjusts the flow rate or halts operation.
-  **Color Sensor**: Detects any **membrane rupture** in the dialyzer. If blood leaks, the dialyzer color changes and the sensor triggers an alarm + system shutdown.
-  **Ultrasonic Sensor**: Monitors the tubing system for **blockages or air bubbles** and triggers a buzzer alert if detected.
-  **Buzzer**: Gives a loud alert in case of any malfunction or emergency.

---

## 🎥 Demo Video

> 📹 **Watch the full prototype in action**:
> 
https://github.com/user-attachments/assets/c1d99e23-ceb6-464e-bc36-a12c5db7a491
> 
---
![Image](https://github.com/user-attachments/assets/a2d20a4c-5ee8-445a-bd47-856498e0a35b)
## System Diagram

Below is a visual representation of the simulation and sensor connections using Arduino:

![Image](https://github.com/user-attachments/assets/2d4a07a6-e41b-439f-9307-5dbae61e6291)
---

## 💻 Code

All the Arduino code used in the project is available in the [`/Code`](./Code) directory.

---

## 📦 Hardware Components

| Component        | Purpose                                      |
|------------------|----------------------------------------------|
| Arduino UNO      | Main microcontroller                         |
| GSR Sensor       | Measures skin resistance (stress indicator)  |
| TCS3200 Color Sensor | Detects dialyzer blood leakage        |
| Ultrasonic Sensor| Detects tube blockage or air                 |
| Buzzer           | Alerts in emergency cases                    |
| Tubing + Motor   | Simulates blood flow                         |
| Power Supply     | Provides stable power                        |

---
## 🤝 Teamwork

This project was developed collaboratively as part of our biomedical engineering studies.  
We tackled real-life challenges with creative sensor integration and medical insight.

### 👥 Team Members

- [Amat Alrahman Sayed](https://www.linkedin.com/in/amat-alrahman-sayed-871712349)  
- [Alaa Essam](https://www.linkedin.com/in/alaa-essam-76a692292)  
- [Farah Yehya](https://www.linkedin.com/in/farah-yehya-bba680326)  
- [Abdelrahman Emad Negm](https://www.linkedin.com/in/abdelrahman-emad-negm-30baab314)


---

### ⭐ Star this repo if you find it useful or inspiring!

