# Password Protected Security System Using Arduino

This project showcases a simple yet effective password-protected security system using an Arduino, a 4x4 keypad, and visual/audio indicators. It serves as a solid introduction to access control systems and user authentication in embedded electronics.

---

## 🔧 Required Components

- Arduino board (e.g., Arduino Uno)  
- 4x4 Keypad  
- Red LED (Access Denied Indicator)  
- Green LED (Access Granted Indicator)  
- Piezo Buzzer (for beeps and unlock sound)  
- Breadboard  
- Jumper wires  

---

## Connection

The input device used here is the 4*4 #keypad. It has 8 terminals and here each terminal is connected to one digital pin of the Arduino board to allow Arduino to receive input from the keypad. Pressing of each key triggers a particular function of each of the 8 terminals and hence the input is received by the Arduino.


The #breadboard is going to house all the external connections done to the Arduino board. So the power supply line and Ground line are specified separately by making a connection from 5V and GND pins from the Arduino board respectively.


We will be using 2 two #LEDs along with a Piezo buzzer as output. One LED can be chosen RED and the other can be chosen GREEN. The Cathode of the LEDs is connected to the ground line through resistors and the Anode is connected to the digital pins of Arduino, D10, and D11 respectively.


The positive terminal of the Piezo #buzzer is connected to another digital pin of Arduino, say D12. The negative terminal of the buzzer is connected to the ground line on the breadboard.

---

## 💡 How It Works

### 🔢 User Input via Keypad
- A **five-digit password** is entered using the **4x4 keypad**.
- Each keypress triggers a short **beep sound** for feedback via the buzzer.

### ✅ Password Verification
- If the entered password **matches the predefined password** (e.g., `12345`):
  - The **green LED** lights up.
  - A melodic **unlocking tone** plays through the buzzer.
- If the password **does not match**:
  - The **red LED** stays ON.
  - A **loud buzzer alert** signals unauthorized access.

### 🔁 Reset & Retry
- After each verification attempt (successful or not), the system **resets** and waits for a new input.
- The system **continuously monitors** keypad inputs and handles logic accordingly.

---
