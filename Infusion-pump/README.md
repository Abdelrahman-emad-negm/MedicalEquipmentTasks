# 🏥 Arduino Infusion Pump System

![WhatsApp Image 2025-05-03 at 02 31 30_638dbe13](https://github.com/user-attachments/assets/e7aaa286-fd54-4fa8-8de5-dac42f916e83)


## 📌 Overview
An Arduino-based medical infusion pump that precisely controls liquid drug delivery with real-time monitoring and safety alarms.

---

## 🛠 Hardware Components
| Component | Specification | Connection |
|-----------|---------------|------------|
| Arduino Uno | ATmega328P | - |
| L298N Motor Driver | 2A, 12V | IN3(D3), IN4(D5), ENB(D6) |
| YF-S201 Flow Sensor | 1-30L/min | D2 (Interrupt) |
| 16x2 LCD | HD44780 | D7-D12 |
| Peristaltic Pump | 12V DC | Connected to L298N |
| Buzzer | 5V Active | D4 |
| LED Indicator | Red 5mm | D13 |

---

## 🔧 Key Code Features

### ⚙️ Motor Control
```arduino
analogWrite(ENB, motorSpeed);  // PWM speed control (0-255)
digitalWrite(int3, HIGH);      // Set direction
digitalWrite(int4, LOW);

🌊 Flow Measurement
// Interrupt handler
void pulseCounter() { pulseCount++; } 

// Calculate flow rate (7.5 pulses/mL for YF-S201)
flowRate = (pulses / 7.5) * 1000;  // mL/min
🖥 LCD Display
lcd.setCursor(0, 1);
lcd.print(flowRate, 1);  // Show actual flow
lcd.print(" mL/min S:");
lcd.print(motorSpeed);   // Show set speed
🚨 Alarm System
Condition 	LED  	Buzzer	 LCD Display
Normal    	OFF 	 OFF	   Flow Value
No Flow	    ON	   OFF    	"NO FLOW"
High Flow  	BLINK 	ON	    "WARNING!"
📊 Technical Specifications
Parameter	         Value	                  Notes
Flow Range	    0-1000 mL/min        	Adjustable via code
Control Resolution	±20 units	        Per button press
Update Rate       	2 Hz	             500ms intervals
Accuracy	          ±2%                After calibration
🚀 Circuit Diagram
![ChatGPT Image 3 مايو 2025، 03_44_19 ص](https://github.com/user-attachments/assets/c441ad45-b671-4b68-8f96-62cee8f6b6f3)


🎥 Demonstration

https://github.com/user-attachments/assets/df086b73-b543-4cda-b8bb-df0331b2ee66


