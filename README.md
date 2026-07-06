<p align="center">
  <img src="https://raw.githubusercontent.com/adithyadewneth2-rgb/ApexDeck/refs/heads/main/gemini-svg.ico" width="128" height="128" alt="ApexDeck Logo">
</p>

<h1 align="center">APEX DECK 🎛️</h1>

An ESP32-powered dual-core macro deck featuring dual rotary encoders, a 10-pad touch matrix with full haptic feedback, an OLED live display, an explicit active window kill switch (XKILL), and seamless support for both standalone Bluetooth (BLE) and wired USB companion modes.

This repository contains both the **ESP32 PlatformIO Firmware** and the **Cross-Platform Python Host Utility** (compatible with Linux and Windows).

---

## ✨ Features

- **Dual Operating Modes**: 
  - **USB Mode**: Streams raw encoder and touch events over Serial to the companion Python host utility for advanced system actions.
  - **BLE Mode**: Acts as a native Bluetooth HID keyboard using an optimized background core layout to inject macro strokes directly.
- **Dynamic Haptic Engine**: Fully non-blocking, variable-duration vibration feedback triggered instantly on touch gestures and encoder transitions.
- **Hardware Diagnostics Window**: Seamless dual-core telemetry display reporting live host computer CPU and RAM load percentages.
- **Active Window Terminator (XKILL)**: Dedicated standalone capacitive button that forcefully intercepts and closes the active application workspace instantly across Linux and Windows.

---

## 🛠️ How to Build & Assemble

### 1. Hardware Requirements & Bill of Materials (BOM)
To build the physical APEX DECK hardware workspace, you will need:
* **Microcontroller**: 1x ESP32 Dev Module (30-pin or 38-pin variant).
* **Display**: 1x 1.3-inch SH1106 I2C OLED Screen Display (128x64 resolution).
* **Inputs**: 2x EC11 Rotary Incremental Encoders with built-in push switches.
* **Haptics**: 1x 5V ERM Cylindrical or Coin Vibration Motor (driven via a simple transistor circuit or logic-level driver module to protect ESP32 GPIO rails).
* **Keypads**: 11x Custom Copper foil pads or Capacitive touch surfaces (10 for the general Macro Matrix, 1 for the isolated XKILL Switch).

### 2. Physical Pin Wiring Map
Wire your components to the ESP32 pins according to this schematic reference table:

| Component Module | Peripheral Pin | Target ESP32 GPIO Pin |
| :--- | :--- | :--- |
| **SH1106 OLED Screen** | I2C SDA<br>I2C SCL | **GPIO 21**<br>**GPIO 22** |
| **Rotary Encoder 1 (Audio)** | Channel A<br>Channel B<br>Push Switch | **GPIO 14**<br>**GPIO 12**<br>**GPIO 27** |
| **Rotary Encoder 2 (System)** | Channel A<br>Channel B<br>Push Switch | **GPIO 26**<br>**GPIO 25**<br>**GPIO 33** |
| **Haptic Feedback Engine** | Signal Control Input | **GPIO 13** |
| **Isolated XKILL Key** | Touch Pad Input | **GPIO 34** |
| **Macro Pad Matrix (P1–P10)**| Touch Inputs 1 to 10 | **GPIO 15, 2, 4, 16, 17, 5, 18, 19, 23, 32** |

---

## 🚀 How to Flash & Run

Coming Soon
