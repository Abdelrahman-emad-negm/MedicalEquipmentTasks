# Infusion Pump Project

## Overview

This project presents a prototype of an **Infusion Pump System** built using an Arduino Uno platform. The design focuses on the safe and precise control of fluid delivery rates, inspired by medical-grade infusion pumps used in hospitals. The system features real-time monitoring, user adjustability, and automatic alerts to ensure patient safety and operational reliability.

---

## Features

* **Accurate Flow Control:** Real-time sensing and adjustment of flow rates.
* **LCD Display:** Continuous monitoring of live flow rate and motor speed.
* **User Interaction:** Two push buttons to dynamically increase or decrease the motor speed.
* **Alarm System:** Buzzer and LED activation under abnormal flow conditions (overflow or no flow).
* **Fail-Safe Mechanism:** Immediate motor halt or alarm when thresholds are violated.

---

## Final Project Image

![WhatsApp Image 2025-05-03 at 02 31 30_f89ba3f8](https://github.com/user-attachments/assets/ece945ec-818e-4b3f-b234-e6c8dc07b9df)

---




## Circuit Diagram


![ChatGPT Image 3 مايو 2025، 03_44_19 ص](https://github.com/user-attachments/assets/d70b2737-b8f9-4bb3-984d-3b74b53c2bbf)

---

## Components Used

* Arduino Uno R3
* LCD 16x2 Display (with potentiometer for contrast control)
* L298N Motor Driver
* DC Motor
* Flow Sensor (e.g., YF-S201)
* Push Buttons (Increase/Decrease speed)
* Buzzer
* LED with a current-limiting resistor
* Breadboard and jumper wires
* Power Supply (USB or external 5V/12V for motor)

---

## System Architecture

1. **Initialization:**

   * LCD and motor control pins are initialized.
   * Motor starts with a default speed.

2. **Flow Measurement:**

   * The flow sensor outputs pulses corresponding to the flow rate.
   * An interrupt routine counts these pulses and updates the flow measurement.

3. **User Control:**

   * Button A0 increases motor speed.
   * Button A1 decreases motor speed.

4. **Alarm Conditions:**

   * **High Flow (>1000 mL/min):** Buzzer and LED activate.
   * **Zero Flow:** LED turns on to alert user.

5. **Display Update:**

   * LCD is updated every 500 ms with current flow rate and motor speed.

---

## How It Works

* **Real-Time Monitoring:** Calculates flow rate based on pulse count and updates the LCD.
* **Motor Speed Control:** PWM signal adjusts motor power based on user input.
* **Safety Checks:** Immediate alarms on detecting abnormal flow behaviors.
* **User-Friendly Interface:** Clear feedback on screen and through alarms.

This design emulates critical aspects of commercial infusion pumps: precision, reliability, and responsive safety alerts.

---

## Potential Improvements

* Implement closed-loop feedback to automatically adjust motor speed for maintaining a set flow rate.
* Add battery backup for enhanced portability.
* Integrate wireless monitoring via Bluetooth or Wi-Fi.
* Expand alarm system to include visual LCD warnings and log error history.

---

## Team Members
-Abdelrahman Emad Negm
-Amat Alrahman Sayed
-Alaa Essam
-Farah Yehya
-Muhammed Nasser


## License

This project is developed for educational purposes under the Introduction to Medical Equipment course (Spring 2025).

---
