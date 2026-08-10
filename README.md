# 🚗 Anti-Sleep Alarm System for Drivers (Arduino Based)

An Embedded Safety Solution designed to prevent road accidents caused by driver fatigue, drowsiness, and prolonged eye closure using real-time IR sensor monitoring and automatic engine cut-off mechanism.

---

## 📌 Project Overview
Drowsy driving is a major cause of road accidents worldwide. This project provides a real-time, non-intrusive safety system that monitors the driver's eye blinks via an eyewear-mounted IR sensor. If prolonged eye closure (drowsiness) is detected, the system triggers an audible buzzer alert and automatically cuts off the vehicle engine via a 5V relay.

---

## ⚡ Key Features
- **Real-Time Eye Blink Monitoring:** Detects prolonged eye closure using an IR sensor mounted on eyewear.
- **Audible Alert Mechanism:** Triggers a Piezo Buzzer to wake up the driver.
- **Automated Engine Cut-Off:** Uses a 5V Single-Channel Relay module to safely disable the motor/vehicle ignition if the driver remains unresponsive.
- **Low Cost & Compact:** Powered by Arduino Uno and compact 9V DC power source.

---

## 🛠️ Hardware & Components Used

| Component | Function | Quantity |
| :--- | :--- | :--- |
| **Microcontroller** | Arduino Uno (ATmega328P) | 1 |
| **Sensor** | Eye Blink Sensor (IR Tx / Rx pair on Eyewear) | 1 |
| **Relay Module** | 5V Single Channel Relay (Engine Ignition Simulation) | 1 |
| **Actuators** | DC Gear Motor (Vehicle Engine) & Piezo Buzzer | 1 Each |
| **Power Supply** | 9V DC Battery / Power Adapter | 1 |
| **Accessories** | Eyewear Frame, Jumper Wires, SPST Switch | As required |

---

## ⚙️ Circuit & Working Logic
1. **Normal State:** The driver wears the eyeglasses integrated with the Eye Blink Sensor. The DC gear motor runs continuously via the relay (simulating normal driving).
2. **Detection:** When the driver's eyes close for more than a set threshold (e.g., 3 to 5 seconds), the IR receiver detects continuous light reflection.
3. **Alarm Trigger:** Arduino processes the signal and immediately sounds the Piezo Buzzer to alert the driver.
4. **Engine Cut-off:** If eye closure persists for an extended period, Arduino triggers the 5V Relay to open the circuit, stopping the motor/engine to prevent an accident.

---

## 💻 Arduino Source Code
> *Upload your `.ino` file into the repository root or code block here.*

```cpp
// Sample Logic Outline
const int eyeSensorPin = 2;
const int buzzerPin = 8;
const int relayPin = 9;

void setup() {
  pinMode(eyeSensorPin, INPUT);
  pinMode(buzzerPin, OUTPUT);
  pinMode(relayPin, OUTPUT);
  digitalWrite(relayPin, HIGH); // Engine ON by default
}

void loop() {
  int sensorState = digitalRead(eyeSensorPin);
  
  if (sensorState == LOW) { // Eye Closed Condition
    delay(3000); // Wait for prolonged closure threshold
    if (digitalRead(eyeSensorPin) == LOW) {
      digitalWrite(buzzerPin, HIGH); // Sound Alarm
      delay(2000);
      digitalWrite(relayPin, LOW);   // Engine Cut-off
    }
  } else {
    digitalWrite(buzzerPin, LOW);
    digitalWrite(relayPin, HIGH);  // Engine ON
  }
}
