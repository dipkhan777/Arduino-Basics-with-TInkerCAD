# Interfacing Ultrasonic Sensor with Arduino

This project demonstrates how to interface an Ultrasonic Sensor (HC-SR04) with an Arduino Uno to measure distance and display the readings on the Serial Monitor in real time. It's particularly useful in applications like robotics, obstacle detection, parking systems, and automation.

---

## 🧰 Required Components
- Arduino board (e.g., **Arduino Uno**)
- **Ultrasonic Sensor (HC-SR04)**
- **Breadboard**
- **Jumper wires**

---

## ⚙️ How It Works

### 🔊 Ultrasonic Signal Transmission
The HC-SR04 sensor features two key pins: Trig (Trigger) and Echo.

To initiate a measurement, the Trig pin is set HIGH for 10µs, sending out an ultrasonic pulse.

This pulse travels through the air and reflects back upon hitting an object.

### 🎯 Echo Reception & Distance Calculation
- The `Echo` pin receives the reflected pulse and measures the **round-trip time**.
- Distance is calculated using the formula:

Distance = (Time × 0.034) / 2
- `0.034 cm/µs` is the speed of sound in air.
- Division by 2 accounts for the signal traveling to the object and back.

### 🖥️ Displaying the Distance
- The **Arduino Serial Monitor** prints the calculated distance in real time.

---
