# ESP32 Marauder - Cheap Yellow Display

<p align="center">
  <img alt="Marauder logo" src="https://github.com/Fr4nkFletcher/ESP32-Marauder-Cheap-Yellow-Display/blob/master/img/logo01.png" width="240">
</p>

<p align="center">
  <img src="https://github.com/Fr4nkFletcher/Adafruit_WebSerial_ESPTool/actions/workflows/pages.yml/badge.svg" alt="GitHub Actions Badge" />
  <img src="https://komarev.com/ghpvc/?username=Fr4nkFletcher&label=Views&color=0e75b6&style=flat" alt="Profile Views" />
  <img src="https://img.shields.io/github/issues/Fr4nkFletcher/ESP32-Marauder-Cheap-Yellow-Display?style=flat-square" alt="GitHub Issues" />
</p>

## Project Goal

The aim of this project is to port the ESP32-Marauder firmware to the Cheap Yellow Display (CYD) module, offering powerful WiFi and Bluetooth testing features on an affordable and accessible hardware platform.

---

## 🏴‍☠️ Latest Update Highlights (09/28/24)

- Flash older Marauder firmware versions
- [Guide for antenna modification](https://github.com/Fr4nkFletcher/ESP32-Marauder-Cheap-Yellow-Display/blob/master/AntennaModNew.md) for ESP-WROOM-32U with built-in IPEX/U.FL connector
- [Evil Portal examples and setup](https://github.com/Fr4nkFletcher/ESP32-Marauder-Cheap-Yellow-Display/blob/master/evilportal/)
- [How to add an external antenna](https://github.com/Fr4nkFletcher/ESP32-Marauder-Cheap-Yellow-Display/blob/master/AntennaMod.md)

---

## Requirements

1. A compatible CYD module (see [Compatibility](#compatibility))
2. Chrome browser
3. Data-capable USB cable
4. *(Optional)* GPS module for enhanced functionality

---

## Installation Steps

### Web Flasher Method (Recommended)

1. Go to the [CYM Web Flasher](https://fr4nkfletcher.github.io/Adafruit_WebSerial_ESPTool/)
2. Click "Connect" and select your device
3. Choose the appropriate Model and Version
4. Click "Program" to start flashing

<p align="center">
  <img src="https://github.com/Fr4nkFletcher/Adafruit_WebSerial_ESPTool/blob/main/assets/sc002.png?raw=true" alt="CYM Web Flasher Screenshot" width="100%" style="max-width:800px; border-radius: 10px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
</p>

#### Troubleshooting:

If issues arise, try the following steps:

1. Unplug and restart your CYD module
2. Hold `RST`, tap `BOOT`, release `RST` (the screen should go blank)
3. Refresh the Web Flasher page and click "Connect"
4. If problems persist, hold `BOOT` while clicking "Connect"

For further details, check out the [Web Flasher repository](https://github.com/Fr4nkFletcher/Adafruit_WebSerial_ESPTool).

---

### Manual Arduino IDE Method

1. Set up your Arduino environment following the [ESP32 Marauder Arduino IDE Setup Guide](https://github.com/justcallmekoko/ESP32Marauder/wiki/arduino-ide-setup).
2. Add the necessary libraries to your Arduino libraries folder.
3. Set the upload speed to `115200` in the Arduino IDE (tested on version 1.8.19).
4. Upload the firmware to your CYD module.

For a step-by-step guide, refer to [Smoochiee's tutorial](https://github.com/smoochiee/MARAUDER-FOR-CYD---CHEAP-YELLOW-DISPLAY).

---

## Compatibility

The project has been successfully tested on:

- [Module 1](https://amazon.com/dp/B0BVFXR313)
- [Module 2](https://amazon.com/dp/B0CLR7MQ91)

No hardware modifications are required, thanks to **@ggaljoen's** fork of the [TFT_eSPI](https://github.com/ggaljoen/TFT_eSPI) library.

---

## GPS Functionality

GPS functionality is fully supported via the 4-pin connector near the MicroUSB port. For a list of compatible GPS hardware, refer to the [official wiki](https://github.com/justcallmekoko/ESP32Marauder/wiki/gps-modification).

| GPS | -> | CYD |
|-----|:--:|-----|
| VCC | -> | VIN |
| GND | -> | GND |
| TX  | -> | TX  |
| RX  | -> | RX  |

---

## Example Usage

After flashing, your CYD module will boot into the Marauder interface. Refer to the [ESP32 Marauder Wiki](https://github.com/justcallmekoko/ESP32Marauder/wiki) for detailed usage instructions.

<p align="center">
  <img src="https://github.com/Fr4nkFletcher/ESP32-Marauder-Cheap-Yellow-Display/blob/master/screenshots/2.gif" alt="Demo 1" width="45%">
  <img src="https://github.com/Fr4nkFletcher/ESP32-Marauder-Cheap-Yellow-Display/blob/master/screenshots/swift2.gif" alt="Demo 2" width="45%">
</p>

---

## Acknowledgments

A huge thanks to the creators and supporters of the [ESP32 Cheap Yellow Display](https://github.com/witnessmenow/ESP32-Cheap-Yellow-Display) project and the community Discord, especially **@cod5fgzj**, [**smoochiee**](https://github.com/smoochiee), [**ggaljoen**](https://github.com/ggaljoen), and [**ATOMNFT**](https://github.com/ATOMNFT). And a special mention to [**JustCallMeKoko**](https://github.com/justcallmekoko) for their foundational work on the [ESP32Marauder](https://github.com/justcallmekoko/ESP32Marauder).

---

## Disclaimer

This project is for educational purposes only. Always obtain proper authorization before testing on networks you don't own or have explicit permission to test. Don't be a dick!
