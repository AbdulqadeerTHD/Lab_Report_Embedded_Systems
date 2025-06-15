# Lab 02: Sensor Interfacing with Raspberry Pi using Sense HAT

This repository contains the source code and documentation for Lab 02 of the Embedded Systems course. The objective is to display messages and real-time sensor readings using the Raspberry Pi Sense HAT.

---

## 📦 Contents

- `sense_led.py`: Scrolls a message on the Sense HAT LED matrix.
- `sense_sensor.py`: Displays real-time temperature, humidity, and pressure readings on the LED matrix.
- `README.md`: Setup and usage instructions.

---

## 🛠️ Requirements

- Raspberry Pi 3/4 with Raspberry Pi OS
- Raspberry Pi Sense HAT attached
- Python 3 installed
- Sense HAT library installed

```bash
sudo apt update
sudo apt install sense-hat
```

---

## 📡 Accessing Raspberry Pi via SSH

If you're using a headless setup:
- Enable SSH on the Pi
- Connect using PuTTY from your PC
- Default IP (if static): `192.168.0.10`
- SSH Port: `22`

---

## 🚀 How to Run

1. **LED Message Display**
   ```bash
   python3 sense_led.py
   ```

2. **Sensor Reading Display**
   ```bash
   python3 sense_sensor.py
   ```

   > Press `Ctrl + C` to stop the script.

---

## 📷 Results Preview

- **Red LED Text:** Message scrolling across the 8×8 matrix
- **White LED Text:** Live sensor values displayed (temperature, humidity, pressure)

---

## 🧑‍💻 Author

**Abdul Qadeer**  
TH Deggendorf – Campus Cham  
Embedded Systems (SS25)

---

## 📚 References

- [Sense HAT API Docs](https://pythonhosted.org/sense-hat/api/)
- [Raspberry Pi Sense HAT](https://shop.pimoroni.com/products/raspberry-pi-sense-hat)
- [PuTTY SSH Client](https://www.putty.org)
