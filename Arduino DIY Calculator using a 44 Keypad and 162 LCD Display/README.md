# Arduino Calculator using 4x4 Keypad and LCD Display

This project is a simple calculator built using an Arduino, a 4x4 matrix keypad, and a 16x2 LCD display. It can perform basic arithmetic operations and demonstrates the fundamentals of embedded systems, input/output interfacing, and real-time display control.

---

## 🔧 Required Components

- Arduino board (e.g., Arduino Uno)  
- 16x2 LCD display  
- 4x4 Keypad module  
- Breadboard  
- Connecting wires  

---

## Connection

In the keypad, there are 8 pins in total out of which 4 pins correspond to the Rows (viz., R1, R2, R3, R4) and the other four correspond to the Columns (viz., C1, C2, C3, C4). 

These 8 row and column pins of the keypad are connected from 0-7 PWM pins of the Arduino board respectively.

DB 4-DB7 pins of the LCD are connected to 11-8 pins of the Arduino respectively.

The 12th port of the Arduino is connected to Enable pin of the LCD and the 13th port of the Arduino is connected to Rs of the LCD.

LED 1 of the LCD is connected to the ground pin of the Arduino through a 1-kilo-ohm resistor. Further, the Vo and ground pins of the LCD are also connected to the ground pin of the Arduino.

Vo and RW pins of the LCD are shorted (i.e., grounded)

Vcc and the other LED of the LCD are short-circuited and connected to 5V pin of the Arduino.

---


## 💡 How It Works

### 🔢 Input Mechanism
- The user enters numbers using the 4x4 keypad.
- The LCD displays the input in real time.

### ➕ Operations Supported
- **Addition (+)**  
- **Subtraction (-)**  
- **Multiplication (*)**  
- **Division (/)**

### ✅ Operation Flow
1. Enter the first number using the keypad.
2. Press an operator key.
3. Enter the second number.
4. Press **`=`** to calculate the result.
5. The result is shown on the LCD display.

### 🧹 Special Functionalities
- **Clear (C)**: Resets the calculator and clears the display.
- **Division by Zero**: If attempted, shows `"Invalid"` on the display.
- **Result Memory**: The calculator can store the result of the last operation for use in the next one.

---
