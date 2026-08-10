# 🔔 Touchless Doorbell System (IR Proximity Sensor)

An innovative, contactless, and hygienic smart doorbell system designed to eliminate physical surface contact using Infrared (IR) sensing technology.

---

## 📌 Project Overview
Traditional doorbells require physical touch, making them high-contact surfaces that can easily transmit germs and viruses. This project presents a hardware solution for a **Touchless Doorbell** that automatically detects hand proximity and triggers an alert signal without any physical contact.

---

## ⚡ Key Features
- **Contactless Operation:** Uses IR Proximity sensing for touch-free activation.
- **Dual Output Alert:** Triggers both a visual (LED) and audible (Buzzer) response.
- **Adjustable Sensitivity:** Integrated potentiometer for range calibration.
- **Cost-Effective & Compact:** Built using easily available discrete components and an op-amp comparator.

---

## 🛠️ Circuit & Component Details

### Hardware Components
| Component | Specification | Quantity |
| :--- | :--- | :--- |
| **Op-Amp IC** | LM358 (Dual Operational Amplifier) | 1 |
| **Sensors** | IR LED Transmitter & IR Photodiode Receiver | 1 Pair |
| **Output Indicators** | Piezo Buzzer & Red LED | 1 Each |
| **Sensitivity Adjustment** | 10kΩ Potentiometer / Preset | 1 |
| **Resistors** | 100Ω, 220Ω, 10kΩ | As required |
| **Power Supply** | 9V DC Battery | 1 |
| **Board** | Custom PCB / Zero PCB Board | 1 |

---

## ⚙️ How It Works (Working Principle)
1. **Infrared Emission:** The IR LED continuously emits invisible light into the immediate environment.
2. **Reflection & Detection:** When a hand or object comes near, the light reflects back into the Photodiode receiver, dropping its resistance.
3. **Signal Comparison:** The LM358 IC compares the incoming voltage from the receiver against a predefined threshold voltage set by the potentiometer.
4. **Trigger Output:** When the sensor voltage exceeds the threshold, LM358 outputs a HIGH signal, activating the Buzzer and illuminating the LED indicator.

---

## 📊 Schematic & Layout
> *Place your circuit diagram and PCB photos here.*
- `Circuit Diagram`: Included in report docs.
- `PCB Board Design`: Copper-clad / Zero PCB implementation.

---

## 👥 Authors & Contributors
- **Suchit Pednekar**
- **Arvind Golatkar**
- **Wilson Metri**
- **Parth Kulkarni**

*Under the guidance of Prof. Vijaypal Yadav — Department of Electronics & Telecommunication Engineering, Terna Engineering College (University of Mumbai).*
