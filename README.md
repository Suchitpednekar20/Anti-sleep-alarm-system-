# 🚘 Anti-Sleep Alarm System with Engine Cutoff for Drivers

An IoT & Embedded Systems project designed to prevent road accidents caused by driver fatigue. It continuously monitors eye movements via eyewear-mounted IR sensors, triggering an audible alarm and automatic engine cutoff if prolonged eye closure is detected.

---

## 📌 Problem & Solution Overview
- **The Problem:** Drowsy driving severely impairs reaction times and is a primary cause of major road accidents worldwide.
- **The Solution:** A wearable, real-time eye-monitoring safety device using Arduino. If the driver falls asleep, the system first sounds a high-decibel alarm and subsequently cuts power to the vehicle's motor/engine using a relay module.

---

## ⚡ Key Features
- **Wearable IR Detection:** Eye-blink sensor non-intrusively mounted on eyeglasses.
- **Multi-Stage Alert Logic:** 
  1. Detects eye closure ($\ge 5\text{ seconds}$).
  2. Triggers Piezo Buzzer to wake up the driver.
  3. If unresponsive ($\ge 2\text{ additional seconds}$), activates 5V Relay to cut engine power safely.
- **Fail-Safe Mechanism:** Automatic cutoff prevents runaway vehicle scenarios when a driver passes out completely.

---

## 🛠️ Hardware Components

| Component | Function / Role |
| :--- | :--- |
| **Arduino Uno** | Main Microcontroller processing sensor inputs and timing logic |
| **Eye Blink Sensor (IR)** | Transmits/Receives IR rays off the eye to check open/closed status |
| **5V Single-Channel Relay** | Controls power supply to the gear motor (Engine Cutoff) |
| **Piezo Buzzer** | High-decibel audio alert mechanism |
| **DC Gear Motor** | Simulates the vehicle's engine/drivetrain operation |
| **9V DC Battery & Power Switch** | Portable power source for the prototype |
| **Eyeglasses Frame** | Wearable mount for the IR sensor assembly |

---

## ⚙️ System Workflow Logic
