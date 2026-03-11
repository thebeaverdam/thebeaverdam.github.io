---
title: "ESP32 MultiBoard"
excerpt: "An expandable ESP32 board with the most common connectors for makers: Grove, Qwiic, SPI and UART."
header:
  teaser: /assets/images/designs/MultiBoard.png
  overlay_image: /assets/images/designs/MultiBoard.png
  overlay_filter: "0.5"
sidebar:
  - title: "Specs"
    text: |
      **MCU:** ESP32-WROOM  
      **Connectors:** Grove Digital, Grove Analog, Grove UART, Qwiic (I2C), SPI  
      **Power:** 5V via USB  
      **Firmware:** ESPHome / Arduino IDE  
      **Programming:** OTA (after first flash) or Serial Adapter  
  - title: "Resources"
    text: |
      [GitHub Repository](https://github.com/thebeaverdam/ESP32_MultiBoard){: .btn .btn--info .btn--small}  
      [ESPHome Firmware](https://github.com/thebeaverdam/ESP32_MultiBoard/blob/main/firmware/ESPHome.yml){: .btn .btn--info .btn--small}  
      [AM2303 + OLED Example](https://github.com/thebeaverdam/ESP32_MultiBoard/blob/main/firmware/AM2303%20Oled%20Display/README.md){: .btn .btn--info .btn--small}
---

## Overview

The **ESP32 MultiBoard** is a custom board that helps makers connect an ESP32 with all kinds of sensors and actuators, using the most common connectors such as **Qwiic** and **Grove**.

A serial adapter is needed to program the board for the first time. Once configured, you can update code wirelessly via **OTA** in ESPHome or Arduino IDE.

---

## 🛒 Buy this Board

Puedes adquirir el kit completo o la PCB suelta en nuestra tienda oficial:

[Check Stock on Lectronz](https://lectronz.com/stores/thebeaverdam){: .btn .btn--success .btn--large}

---

## Connector Specifications

### Grove Digital

Ideal for binary sensors, actuators, or general-purpose digital I/O.

| Pin | Function | ESP32 GPIO | Notes |
| :--- | :--- | :--- | :--- |
| 1 | GND | GND | System Ground |
| 2 | VCC | 3V3 | 3.3V Power Supply |
| 3 | IO_0 | GPIO 25 | Supports DAC Output / Digital I/O |
| 4 | IO_1 | GPIO 26 | Supports DAC Output / Digital I/O |

---

### Grove Analog

Designed for interfacing with analog sensors via ADC.

| Pin | Function | ESP32 GPIO | Notes |
| :--- | :--- | :--- | :--- |
| 1 | GND | GND | System Ground |
| 2 | VCC | 3V3 | 3.3V Power Supply |
| 3 | AN 1 | GPIO 35 | Input Only (ADC1_CH7) |
| 4 | AN 0 | GPIO 34 | Input Only (ADC1_CH6) |

> ⚠️ **Note:** GPIOs 34 and 35 do not have internal pull-up/down resistors and **cannot be used as outputs**.

---

### Grove UART

For serial communication with modules like GPS, CO2 sensors, or MIDI devices.

| Pin | Function | ESP32 GPIO | Notes |
| :--- | :--- | :--- | :--- |
| 1 | GND | GND | System Ground |
| 2 | VCC | 3V3 | 3.3V Power Supply |
| 3 | TX | GPIO 17 | Transmit (UART2 TX) |
| 4 | RX | GPIO 16 | Receive (UART2 RX) |

---

### Qwiic Connector (I2C)

Standard 4-pin JST-SH 1.0mm connector for I2C daisy-chaining.

| Pin | Function | ESP32 GPIO | Notes |
| :--- | :--- | :--- | :--- |
| 1 | GND | GND | System Ground |
| 2 | VCC | 3V3 | 3.3V Power Supply |
| 3 | SDA | GPIO 21 | I2C Data (Default) |
| 4 | SCL | GPIO 22 | I2C Clock (Default) |

---

### SPI Connector

Standard 6-pin JST-PH 2.0mm connector for SPI interface.

| Pin | Function | ESP32 GPIO | Notes |
| :--- | :--- | :--- | :--- |
| 1 | VCC | 3V3 | 3.3V Power Supply |
| 2 | CS | GPIO 05 | Chip Select |
| 3 | CLK | GPIO 18 | Clock |
| 4 | MISO | GPIO 19 | Input |
| 5 | MOSI | GPIO 23 | Output |
| 6 | GND | GND | System Ground |

---

## ⚡ ESPHome Setup (No Serial Adapter Needed)

You can purchase the board with the **ESPHome firmware pre-installed**. This lets you adopt the board directly in Home Assistant without a serial adapter. Follow these steps:

1. **Power the board** via a 5V USB supply.
2. On a mobile device or laptop, search for the Wi-Fi network **"Setup_MultiBoard"** and connect to it.
3. A captive portal will appear to configure your home Wi-Fi. If it doesn't appear automatically, navigate to **[192.168.4.1](http://192.168.4.1)** in your browser.
4. Once connected to your network, the **ESPHome Dashboard** will automatically detect the board and offer the option to **"Adopt"** it.
5. You're all set! Edit the firmware to your liking from the ESPHome editor.

> 💡 **Tip:** After the initial setup, all future firmware updates can be pushed **Over-The-Air (OTA)** directly from ESPHome — no cables needed.

---

## 📦 Examples

| Example | Description |
| :--- | :--- |
| [AM2303 + OLED Display](https://github.com/thebeaverdam/ESP32_MultiBoard/blob/main/firmware/AM2303%20Oled%20Display/README.md) | Read temperature & humidity and display it on a 1.3" I2C OLED screen |
