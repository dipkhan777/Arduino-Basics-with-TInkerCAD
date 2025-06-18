# Fire Alarm System Project by Interfacing Arduino with Temperature & Gas Sensor using TinkerCad

 We are going to design a Fire Alarm circuit using a few electrical components like Temperature and  Gas sensors using TinkerCad and interface it with Arduino. Let's start with the components we will require to build the circuit in the #TinkerCad software.

---
## Hardware Requirements

- Arduino board (e.g., Arduino Uno)  
- Temperature sensor (e.g., LM35 or similar)  
- Gas sensor (e.g., MQ-2, MQ-5, or MQ-7)  
- LED (for fire alert)  
- Buzzer (for gas alert)  
- Breadboard  
- Jumper wires

---
## Software Requirement

- TinkerCad circuit simulation software.

---

## Connection 

Firstly, we need to connect one line of the breadboard to the ground and the other to the power supply. This is done by connecting the 5V pin of the Arduino Board to one line of connection pins on the breadboard. The other line of the breadboard is connected to the ground terminal of the Arduino Board. These lines will be connected to other devices. 


The Temperature sensor has three pins. Ground, Vout, and Vs (Supply). The Vs pin that has a range of 4-20V is connected to the power supply line of the breadboard. The Ground terminal of the sensor is connected to the ground line of the breadboard. The Vout terminal of the temperature sensor is connected to one of the Analog pins of the Arduino Board, A1.


Now let us learn how the connections are done with the Gas sensor. This sensor has 6 pins. 3 pins of the gas sensor are directly connected to the power supply line of the breadboard. Amongst the other 3 pins of the sensor, one pin is connected to one of the Analog pins of the Arduino Board, A0. The pin in the middle is connected to the ground line of the breadboard. The third pin of the sensor is connected to a resistor and then connected to the ground line. 


The piezo buzzer is externally connected to the circuit. The ground pin of the #buzzer is connected to the ground line of the breadboard. Another pin of the buzzer is connected to the digital pin, PIN 7 of the Arduino Board.


Lastly, the LED is connected to the Arduino directly. The cathode of the LED is connected to the GND pin of Arduino and the anode of the LED is connected through a resistor to the digital pin 13 of the Arduino.

---

## Working Process

### 🌡️ Temperature Monitoring
- The **temperature sensor** reads the ambient temperature and outputs an analog voltage.
- Arduino reads this analog value (typically from **A1**) and converts it into Celsius.
- If the temperature is **≥ 80°C**, the **LED turns ON**, indicating a possible fire hazard.

### 💨 Gas Detection
- The **gas sensor** detects gases like LPG, methane, or smoke and provides an analog output based on concentration.
- If gas levels exceed a threshold (e.g., **100**, adjustable), the **buzzer is activated** to signal danger.

### 🖥️ Data Display & Alerts
- Both **temperature** and **gas levels** are printed to the **Serial Monitor** in real-time.
- The system runs continuously and updates alerts dynamically based on changing readings.

---





  
