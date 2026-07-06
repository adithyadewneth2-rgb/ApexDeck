<p align="center">
  <img src="https://raw.githubusercontent.com/adithyadewneth2-rgb/ApexDeck/refs/heads/main/gemini-svg.ico" width="128" height="128" alt="ApexDeck Logo">
</p>

<h1 align="center">APEX DECK </h1>



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

## 📁 Repository Structure
