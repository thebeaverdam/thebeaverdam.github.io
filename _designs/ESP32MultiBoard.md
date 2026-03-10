---
title: "ESP32 MultiBoard v1.1"
excerpt: "A rugged IoT development board."
header:
  teaser: /assets/images/designs/MultiBoard.png
sidebar:
  - title: "Specs"
    text: "MCU: ESP32-S3<br>RAM: 8MB PSRAM<br>Power: LiPo + Solar"
  - title: "Resources"
    text: "[Schematics (PDF)](/assets/docs/schematic-v1.pdf)<br>[Firmware (GitHub)](https://github.com/thebeaverdam/firmware)"
---

## Technical Overview
Este es el corazón de nuestro ecosistema IoT. Diseñada para durar en exteriores (como una verdadera presa de castor).

### Key Features
* **Ultra-low power:** Optimized for battery life (10uA in deep sleep).
* **Connectivity:** WiFi, BLE 5.0, and an expansion header for LoRa.
* **Open Hardware:** Designed in KiCad.

### 🛒 Buy this Board
Puedes adquirir el kit completo o la PCB suelta en nuestra tienda oficial:

[Check Stock on Lectronz](https://lectronz.com/stores/thebeaverdam){: .btn .btn--success .btn--large}

---

### Bill of Materials (BOM)
| Component | Value | Package |
| :--- | :--- | :--- |
| C1, C2 | 10uF | 0805 |
| U1 | ESP32-S3-WROOM-1 | Module |