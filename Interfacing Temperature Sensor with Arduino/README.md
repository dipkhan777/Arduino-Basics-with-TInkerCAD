
# Temperature Sensor with Arduino

This project explains how to measure ambient temperature using an LM35 analog temperature sensor with an Arduino. It calculates and displays real-time temperature readings in both Celsius and Fahrenheit via the Serial Monitor. It’s an excellent project for beginners learning about sensors, analog input, and data conversion.

---

## 🔧 Required Components

- Arduino board (e.g., Arduino Uno)  
- Analog temperature sensor (e.g., LM35)  
- Breadboard  
- Jumper wires  

---

## Connection

The connection between the Arduino board and LM35- Temperature sensor by using jumper wires involves simple steps:

The supply voltage is the voltage by which the circuit operates, and it needs to be connected to 5V on the Arduino board to power the temperature sensor LM35.

The output voltage is the analog pin connected to the A0 pin of the Arduino board through which we receive data.

Finally, connect the ground pin of the sensor to the GND terminal in the Arduino board to establish a common ground connection. 

---

## 💡 How It Works

### 🌡️ Analog Temperature Reading
- The **LM35 sensor** outputs an analog voltage proportional to the temperature.
- Arduino reads this analog voltage through **analog pin A0**.

### 🔁 Voltage to Temperature Conversion

- **Analog to Voltage Conversion**  
  The analog value (0–1023) is converted to voltage (0–5V) using:
  ```
  Voltage = (AnalogReading × 5.0) / 1024.0
  ```

- **Celsius Conversion**  
  LM35 outputs 10mV per °C. Temperature in Celsius is calculated as:
  ```
  TempC = Voltage × 100
  ```

- **Fahrenheit Conversion**
  ```
  TempF = (TempC × 9.0 / 5.0) + 32
  ```
