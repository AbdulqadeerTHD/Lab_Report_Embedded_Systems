# Embedded Systems Lab 02 – Raspberry Pi Sense HAT

This repository contains code and instructions for **Lab 02: Sensor Interfacing with Raspberry Pi using Sense HAT**, part of the Embedded Systems course.

## Contents
- **`sense_led.py`** – Python script that displays a scrolling message on the 8×8 LED matrix of the Raspberry Pi Sense HAT.
- **`sense_sensor.py`** – Python script that reads environmental sensor data (temperature, humidity, pressure) from the Sense HAT and prints the values to the console.
- **`README.md`** – (This file) Usage instructions and setup information for the scripts.

## Hardware Requirements
- Raspberry Pi (Model 3 or newer recommended) with a Sense HAT attached.
- Micro SD card with Raspberry Pi OS.
- Network connection (for setup or SSH, if headless).

## Setup and Installation

1. **Prepare the Raspberry Pi:** If using a headless setup, enable SSH and connect to the Raspberry Pi via terminal. Ensure the Raspberry Pi OS is up-to-date:
   ```bash
   sudo apt update && sudo apt upgrade -y
   ```
2. **Attach the Sense HAT:** Carefully mount the Sense HAT onto the Raspberry Pi’s GPIO header. Ensure it is oriented correctly and firmly seated.
3. **Install Sense HAT Library:** The Sense HAT Python library must be installed for the scripts to work. Install it by running:
   ```bash
   sudo apt install sense-hat
   ```
   This provides the `sense_hat` module used in the Python scripts.

## Usage

### 1. LED Matrix Message Display (`sense_led.py`)
This script scrolls a text message across the Sense HAT’s LED matrix.
- **Before running:** You can edit the message or colors in the script if desired. By default, it will display "**Hello, Embedded AI!**" in red text.
- **Run the script:**
  On the Raspberry Pi, execute:
  ```bash
  python3 sense_led.py
  ```
- **Expected outcome:** The message will scroll from right to left on the 8×8 LED matrix in red. You should see the text repeat indefinitely until the program is stopped. Use `Ctrl+C` to terminate the script when done.

### 2. Sensor Data Reading (`sense_sensor.py`)
This script continuously reads the temperature, humidity, and pressure from the Sense HAT and outputs them to the console.
- **Run the script:**
  ```bash
  python3 sense_sensor.py
  ```
- **Expected outcome:** You will see output in the terminal similar to:
  ```
  Temp: 25.3C Humidity: 40.5% Pressure: 1012.8hPa
  Temp: 25.4C Humidity: 40.4% Pressure: 1012.5hPa
  ... (updates every 2 seconds) ...
  ```
  The values will update every 2 seconds. Use `Ctrl+C` to stop the script.
- **Note:** The temperature reading may be slightly higher than ambient temperature due to the heat from the Raspberry Pi board. This is normal for the Sense HAT’s sensors.

## Troubleshooting

- If you get an `ImportError: No module named sense_hat`, ensure that the Sense HAT library is installed (see setup step 3).
- If the LED matrix does not display the message:
  - Make sure the Sense HAT is correctly attached to the Raspberry Pi.
  - Ensure that you are running the script on the Raspberry Pi (the Sense HAT hardware is required).
- If sensor outputs seem wrong or zero:
  - Check that the Sense HAT is firmly connected.
  - Ensure that you’re not running the script in an environment without the Sense HAT (or use the Sense HAT emulator for testing on a PC).
- To exit the sensor reading script, press `Ctrl+C`. If running via SSH, you can also simply close the terminal which will terminate the process.


## License

This project is released under the MIT License. See `LICENSE` (if provided) for details.