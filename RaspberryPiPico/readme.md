# Raspberry Pi Pico

## Overview

Raspberry Pi Pico is a low-cost, high-performance microcontroller board built around the RP2040 chip designed by the Raspberry Pi Foundation. It is designed for embedded systems, IoT applications, robotics, and electronics projects.

Unlike a full Raspberry Pi computer, Pico is a microcontroller board, meaning it runs a single program at a time and does not run an operating system.

---

## Key Features

- Microcontroller: RP2040
- Dual-core ARM Cortex-M0+ processor
- Clock speed: Up to 133 MHz
- 264 KB SRAM
- 2 MB onboard QSPI Flash
- 26 multi-function GPIO pins
- 3 Analog-to-Digital Converter (ADC) inputs
- 2 UART interfaces
- 2 SPI controllers
- 2 I2C controllers
- 16 PWM channels
- USB 1.1 device support
- Internal temperature sensor
- Low power consumption

---

## RP2040 Microcontroller

The RP2040 is a dual-core ARM Cortex-M0+ microcontroller chip designed by Raspberry Pi.

### Main Specifications:
- Dual-core ARM Cortex-M0+
- 133 MHz max clock speed
- 264 KB SRAM
- Flexible I/O (Programmable I/O - PIO)
- DMA controller

The PIO (Programmable I/O) feature allows advanced custom communication protocols.

---

## Pinout Summary

- GPIO Pins: 26
- ADC Pins: 3 (GPIO26, GPIO27, GPIO28)
- Power Pins: VSYS, 3V3, GND
- USB: Micro-USB port
- BOOTSEL button for firmware flashing

---

## Power Options

The Raspberry Pi Pico can be powered using:

1. Micro-USB port (5V)
2. VSYS pin (1.8V to 5.5V input)
3. 3.3V regulated output available onboard

---

## Programming Languages Supported

You can program Raspberry Pi Pico using:

- MicroPython
- C
- C++
- CircuitPython

---

## Getting Started (MicroPython)

### Step 1: Install MicroPython Firmware

1. Download the latest UF2 firmware file.
2. Press and hold the BOOTSEL button on the Pico.
3. Connect it to your computer via USB.
4. Release the BOOTSEL button.
5. Drag and drop the UF2 file into the Pico storage drive.

---

### Step 2: Install Thonny IDE

1. Download and install Thonny IDE.
2. Go to Tools → Options → Interpreter.
3. Select "MicroPython (Raspberry Pi Pico)".
4. Select the correct port.
5. Click OK.

You are now ready to program.

---

## Example: Blink LED (MicroPython)

```python
from machine import Pin
import time

led = Pin(25, Pin.OUT)

while True:
    led.toggle()
    time.sleep(1)
