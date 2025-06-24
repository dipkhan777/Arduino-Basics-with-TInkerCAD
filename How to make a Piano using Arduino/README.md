# 🎹 Creating a Piano with Arduino

This project demonstrates how to build a **mini piano** using an **Arduino**, 8 **push buttons**, and a **piezo buzzer**. Each button corresponds to a musical note, and pressing a button plays the note through the buzzer.

---

## 🧰 Required Components
- Arduino board (e.g., **Uno**, **Mega**)
- **8 Push buttons**
- **Piezo buzzer**
- **8 × 10kΩ resistors** (for pull-down configuration)
- **Breadboard**
- **Jumper wires**

---

## ⚙️ How It Works

1. **Button Inputs**:
   - 8 buttons are connected to individual digital pins.
   - Each button represents a **musical note**.

2. **Tone Generation**:
   - When a button is pressed, Arduino detects it using `digitalRead()`.
   - The `tone()` function is called to play a specific **frequency**.

3. **Piezo Buzzer Output**:
   - The buzzer plays the sound for **100 milliseconds**.

4. **Serial Feedback**:
   - The **Serial Monitor** logs button presses for easy debugging.

5. **Debouncing**:
   - A `delay(100)` prevents multiple detections from a single press (basic debounce).

---

## 🎵 Musical Notes Mapping

| Note | Frequency (Hz) |
|------|----------------|
| C4   | 262            |
| D4   | 294            |
| E4   | 330            |
| F4   | 349            |
| G4   | 392            |
| A4   | 440            |
| B4   | 494            |
| C5   | 523            |

Each button triggers one of these tones.

---
