# Controlling LED using IR Remote and Arduino

This project demonstrates how to control multiple LEDs using an IR remote and Arduino. Each button on the remote triggers a specific action, allowing wireless LED control. It’s a beginner-friendly introduction to IR communication and remote-controlled electronics, perfect for home automation projects.

---

## 🔧 Required Components

- Arduino board (e.g., Arduino Uno)  
- IR remote control  
- IR receiver module (e.g., TSOP1738)  
- LEDs (Blue, Orange, Green)  
- 220Ω resistors  
- Breadboard  
- Jumper wires  

---

## Connection

Anodes of the #LEDs are connected to pin 2, pin3, and pin4 of the Arduino UNO  board respectively.

Cathodes of the LEDs are connected to a 220-ohm resistor which is further connected to the ground of the breadboard.

GND of the IR sensor ( middle terminal ) is connected to the ground of #Arduino UNO.

The power ( third terminal) of the IR #Sensor is connected to the positive power supply ( +5V ) of the Arduino UNO board. 

The output ( first terminal ) of the IR Sensor is connected to Pin12 of the Arduino board.

GND pin of the Arduino board is connected to the GND of the breadboard.

---

## 💡 How It Works

### 📶 Receiving Signals
- The **IR receiver** detects signals sent by the **IR remote**.
- Arduino decodes these IR signals into **unique numerical values** using an IR library.
- These values are compared to **predefined button codes**.

### 💡 LED Control Mechanism
Each button on the IR remote performs a specific function:

| Button | Action                  |
|--------|--------------------------|
| 1      | Turn **Blue LED** ON     |
| 2      | Turn **Blue LED** OFF    |
| 3      | Turn **Red LED** ON   |
| 4      | Turn **Red LED** OFF  |
| 5      | Turn **Green LED** ON    |
| 6      | Turn **Green LED** OFF   |

### 🔁 Functionality
- The Arduino **constantly listens** for incoming IR signals.
- Once a signal is received:
  - It is decoded.
  - The corresponding **LED is turned ON or OFF**.
- After processing, the system continues to listen for new commands.

---
