<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=700&size=28&duration=3000&pause=900&color=00F5A0&center=true&vCenter=true&width=700&lines=Ghost+Stroke+%28Madiff%29;ESP32-S3+HID+Toolkit;Security+Research+Prototype" alt="Ghost Stroke (Madiff)" />
</div>

<p align="center">
  <img src="https://img.shields.io/badge/C%2B%2B-100%25-blue.svg" alt="C++" />
  <img src="https://img.shields.io/badge/ESP32-S3-Black.svg" alt="ESP32-S3" />
  <img src="https://img.shields.io/badge/WiFi-AP-Enabled-green.svg" alt="WiFi AP" />
  <img src="https://img.shields.io/badge/USB-HID-Controller-orange.svg" alt="USB HID" />
  <img src="https://img.shields.io/badge/Status-Prototype-lightgrey.svg" alt="Prototype status" />
</p>

<h1 align="center">Ghost Stroke (Madiff)</h1>

<p align="center">
  A compact ESP32-based HID automation prototype designed to expose a browser-based control panel and trigger host-side interactions through USB keyboard emulation.
</p>

<p align="center">
  <a href="#overview">Overview</a> •
  <a href="#features">Features</a> •
  <a href="#hardware-and-software">Hardware & Software</a> •
  <a href="#setup">Setup</a> •
  <a href="#security-disclaimer">Security Disclaimer</a>
</p>

---

## Overview

Ghost Stroke (Madiff) is a firmware project built for the ESP32-S3 platform. It creates a Wi-Fi access point and serves a lightweight dashboard over HTTP. The board acts as a USB HID device, emulating keyboard input to automate common desktop actions on a connected host machine.

This project is intended as a learning, experimentation, and controlled-research prototype for understanding:

- HID emulation on embedded devices
- Wi-Fi enabled controller interfaces
- Desktop automation behavior via keyboard injection
- Prototype interaction flows for authorized testing scenarios

---

## Features

- Wi-Fi access point mode with a simple web dashboard
- USB keyboard emulation using the ESP32 USB HID stack
- Host-side action triggers such as launching applications and commands
- PowerShell integration for system-level interactions
- Reverse-shell configuration patterns for testing environments
- Keylogging prototype behaviors for experimental evaluation
- Persistent task scheduling patterns for controlled lab scenarios
- Built-in status and log display within the web interface

<div align="center">
  <img src="https://img.shields.io/badge/Interface-Web+Dashboard-00D1B2.svg" alt="Web Dashboard" />
  <img src="https://img.shields.io/badge/Host-Actions-Triggered-FF4D4D.svg" alt="Host actions triggered" />
  <img src="https://img.shields.io/badge/Platform-ESP32-S3-8A2BE2.svg" alt="ESP32-S3 platform" />
</div>

---

## Project Structure

```text
ghost-troke-madiff/
├── Malware.cc      # Main ESP32 firmware source file
├── heyy.txt        # Additional note / placeholder file
└── README.md       # Project documentation
```

---

## Hardware and Software

### Required Hardware
- ESP32-S3 development board
- USB connection to a target host machine
- Stable power source
- Optional USB cable and enclosure for prototype deployment

### Required Software
- Arduino IDE or VS Code with PlatformIO
- ESP32 Arduino core installed
- Libraries compatible with the target ESP32 board
- Wi-Fi AP access and a test environment with explicit authorization

---

## Setup

1. Open the project in Arduino IDE or PlatformIO.
2. Load `Malware.cc` as the main sketch.
3. Confirm your board and port are correctly selected.
4. Install any required ESP32 board support packages.
5. Compile and upload the firmware to the ESP32 device.
6. Connect to the Wi-Fi access point created by the board.
7. Open the embedded control panel in the browser.

### Access Points
The firmware sets up a local access point using the configuration embedded in the project. This allows the user to reach the device's HTTP control interface over Wi-Fi.

---

## Web Interface

The firmware exposes a browser-based UI that allows interaction with the device through a local web panel. The interface includes sections for:

- Application launch controls
- PowerShell-related actions
- Configuration controls
- Persistence and keylogging workflow toggles
- Logging and status feedback

This simplifies testing and operational monitoring while keeping the interaction flow centralized in a single control surface.

---

## Build Notes

This project relies on the ESP32 Arduino environment and uses the USB HID stack to simulate keyboard input on the attached host. As a result, successful operation depends on:

- Correct board configuration
- Stable firmware upload
- Host OS compatibility
- Explicitly authorized testing conditions

---

## Configuration

The firmware includes core configuration values such as:

- Wi-Fi SSID
- Wi-Fi password
- Reverse shell target address
- Reverse shell port

These values are defined in the firmware and can be adjusted before flashing the device for a lab or controlled environment.

---

## Security Disclaimer

This repository is a security-research and embedded-experimentation prototype. It should only be used in environments where you have explicit authorization to test or evaluate the behavior.

Important guidelines:

- Do not deploy on systems you do not own or have permission to test.
- Do not use this project in production or public environments.
- Respect local laws, organizational policies, and responsible disclosure practices.
- Treat all security tooling as controlled research software, not end-user software.

Use this project strictly for ethical testing, authorized evaluation, and defensive learning.

---

## License

This repository does not include an explicit license file at this time. If you plan to reuse or distribute the project, confirm the governing licensing terms before publishing or sharing outside your authorized environment.

---

## Contact / Notes

For internal lab or research use, keep a clear record of:

- test environment
- host machine details
- device configuration
- explicit approval for testing

This helps maintain compliance and a clean audit trail for any controlled security evaluation.

<p align="center">
  <img src="https://img.shields.io/badge/Project-Ghost%20Stroke%20%28Madiff%29-0A0A0A.svg" alt="Ghost Stroke (Madiff)" />
</p>
