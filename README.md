# 💓 Arduino Pulse Monitor with OLED Display

This project is a simple real-time heart rate (BPM) monitor built using an Arduino, a pulse sensor, and a 128x64 SH1106 OLED display. It visualizes BPM and waveform data while providing LED feedback based on heartbeats.

---

## 🛠️ Features

- Real-time BPM (Beats Per Minute) calculation
- OLED display output using Adafruit SH1106 library
- Animated heartbeat waveform
- LED heartbeat indicator
- Smooth signal filtering and noise handling
- Adaptive waveform scrolling and LED blink based on BPM

---

## 🔌 Hardware Required

| Component          | Description                        |
|-------------------|------------------------------------|
| Arduino (Uno/Nano)| Main microcontroller               |
| Pulse Sensor      | Analog pulse sensor (e.g., KY-039) |
| OLED Display      | SH1106 128x64 OLED (I2C)           |
| Resistor & Wires  | Basic connections                  |
| LED               | For heartbeat blink indicator      |

---

## 🖥️ Display Output

- **Top Left**: Current BPM value (updated in real-time)
- **Lower Area**: Heartbeat waveform scrolls horizontally
- **LED**: Blinks in sync with detected pulses

---

## 🔧 Wiring

| Component      | Arduino Pin |
|----------------|-------------|
| Pulse Sensor   | A0          |
| OLED SDA       | A4 (SDA)    |
| OLED SCL       | A5 (SCL)    |
| LED (+)        | D13         |

---

## 📦 Libraries Used

Install the following libraries via Library Manager:

- [`Adafruit GFX`](https://github.com/adafruit/Adafruit-GFX-Library)
- [`Adafruit SH110X`](https://github.com/adafruit/Adafruit_SH110X)

---

## 🧠 Code Logic Overview

1. Reads analog pulse signal
2. Filters and smooths signal
3. Detects rising edge to calculate Inter-Beat Interval (IBI)
4. Computes BPM:  
   \[
   \text{BPM} = \frac{60000}{\text{IBI}}
   \]
5. Displays BPM and waveform
6. Blinks LED without `delay()` based on BPM

---

## 📈 BPM and Waveform Adaptation

- Faster BPM = faster waveform scroll
- LED blink rate adapts dynamically
- Graph clears when display is full for continuous scroll

---

## ✅ How to Use

1. Connect all components as shown above
2. Upload the provided sketch
3. Open Serial Monitor at 9600 baud (optional)
4. Observe OLED and LED response to pulse changes

---

## 📃 License

This project is open-source under the MIT License.

---

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first.

---

## 👨‍💻 Author

**Javier Siliacay**  
Passionate Arduino maker from USTP-CDO

---

> *“The beat of your heart, visualized in real time.”*
