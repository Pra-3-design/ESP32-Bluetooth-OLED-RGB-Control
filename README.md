# ESP32-Bluetooth-OLED-RGB-Control
# ESP32 Bluetooth OLED and RGB LED Controller

This project enables an **ESP32** microcontroller to act as a **Bluetooth-based message processor** that:
- Displays received text on an **OLED screen**
- Converts modern English to **Old English-style** text
- Controls an **RGB LED** using commands sent via Bluetooth

## Features

- 🔤 Converts incoming Bluetooth text to a stylized "Old English"
- 📺 Displays messages on a 128x64 I2C OLED display
- 🎨 Controls RGB LED color via Bluetooth command (`RGB R,G,B` format)
- 📶 Bluetooth communication using the `BluetoothSerial` library

---

## Hardware Requirements

- ESP32 Development Board
- 0.96" I2C OLED Display (SSD1306, 128x64)
- Common Anode or Cathode RGB LED (and appropriate resistors)
- Jumper wires, breadboard, etc.

### Pin Configuration

| Component | ESP32 Pin |
|----------|-----------|
| OLED SDA | 21 (default I2C) |
| OLED SCL | 22 (default I2C) |
| RGB Red  | 16 |
| RGB Green| 17 |
| RGB Blue | 18 |

Make sure the RGB pins used are **PWM-capable**.

---

## Software Requirements

- Arduino IDE with ESP32 board support
- Install the following libraries via Library Manager:
  - `Adafruit GFX Library`
  - `Adafruit SSD1306`
  - `BluetoothSerial` (included with ESP32 support)

---

## Installation

1. Connect the components as per the pin configuration above.
2. Open the provided `.ino` file in the Arduino IDE.
3. Select your ESP32 board and correct COM port.
4. Upload the code.

---

## Usage

### 1. Bluetooth Text Messaging

Pair your phone or computer with the ESP32 (Bluetooth name: `ESP32_OLED_BT`).  
Send any plain text and see it converted and displayed in Old English on the OLED.

#### Example:
- **Sent:** `hello, you are good`
- **Display:** `hail, thee art goodly`

### 2. RGB LED Control

Send a message in the format:

