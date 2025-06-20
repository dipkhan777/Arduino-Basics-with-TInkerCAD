# Light Intensity Measurement Using LDR Sensor

This project utilizes an LDR (Light Dependent Resistor) with an Arduino to measure ambient light levels and dynamically adjust an LED’s brightness. It’s a great demonstration of real-time analog input processing and output control — ideal for smart lighting systems and other automation applications.

---

## 🧰 Required Components
- Arduino board (e.g., Arduino Uno)  
- LDR sensor (Light Dependent Resistor)  
- 10kΩ resistor (for voltage divider)  
- LED (for brightness indication)  
- Breadboard  
- Jumper wires

---

## Connection

First, it is necessary to define the ground and power supply line of the breadboard. This is done by connecting the 5V supply pin from the Arduino to one of the lines of the breadboard and the Ground (GND) pin of the Arduino to another line of pins of the breadboard. In the given circuit diagram, the wires in Red are connected to the power supply and those in Green are connected to the Ground.


The LDR has two terminals of which one is directly connected to the Analog pin (A0) of the Arduino and the same PIN is connected to the ground line of the breadboard through the resistor. The second pin of the #LDR is connected to the power supply line of the breadboard.


Next, in this circuit, LED is the output device. So the anode terminal of the LED is connected to the Digital pin (PIN 9) of the Arduino. The cathode terminal of the #LED is connected to the ground line of the breadboard through the resistor.


We are using Multimeter as the output indicator. Hence, the pin used for output, i.e. PIN 9 is connected to the positive (RED) terminal of the Multimeter and the negative (BLACK) terminal of the #multimeter is connected to the ground line of the breadboard.

---

## 💡 How It Works

### 🔦 Light Detection
- The **LDR** changes its resistance based on the surrounding light level.
- Combined with a **10kΩ resistor**, it forms a **voltage divider** circuit.
- The voltage output is read by the Arduino through the **A0 analog pin**.

### 🧠 Data Processing
- Arduino reads the analog value (0–1023) from the LDR.
- This value is sent to the **Serial Monitor** for real-time observation.
- The value is mapped to a range of **0–255** using `map()` and sent to the LED using `analogWrite()` for PWM brightness control.

### 💡 LED Brightness Control
- **More Light** → **Lower LED Brightness**
- **Less Light** → **Higher LED Brightness**

This simulates an automatic lighting system that adjusts based on environmental brightness.

---
