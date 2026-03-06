---
title: PicoForge
weight: -20
---

<!--more-->

{{< toc >}}

**PicoForge** is a modern desktop application for configuring and managing open source security keys such as `Pico-Fido`, `LibreKeys One`, `Pico-OpenPGP` and `Pico-HSM`. Written in Rust using GPUI-Component for GUI.

{{< hint type=important >}}
**Beta Status**: This application is currently under active development and in beta stage. Users should expect bugs and are encouraged to report them. PicoForge has been tested on Linux, Windows 10/11 and MacOS with the official Raspberry Pi Pico2, WaveShare RP2350 One & ESP32-S3. 

Currently it supports Pico-Fido firmware version 7.2 and LibreKeys One firmware version 7.4.

It does not support all the features exposed by the `pico-fido`, `pico-openpgp`, `pico-hsm` and `LibreKeys One`.
{{< /hint >}}

## Features

- **Device Configuration** - Customize USB identifiers, LED behavior, and hardware settings
- **Security Management** - Enable secure boot and firmware verification (experimental and WIP)
- **Real-time Monitoring** - View flash usage, connection status, and system logs
- **Modern UI** - Clean, responsive interface built with Svelte and shadcn-svelte
- **Multi-Vendor Support** - Compatible with multiple hardware variants
- **Cross-Platform** - Works on Windows, macOS, and Linux
- **Detailed Capabilities**:
    - Reading device information and firmware details
    - Configuring USB VID/PID and product names
    - Adjusting LED settings (GPIO, brightness, driver)
    - Managing security features (secure boot, firmware locking) (WIP)
    - Real-time system logging and diagnostics
    - Support for multiple hardware variants and vendors

## Usage

1. Connect your smart card reader
2. Insert your Pico FIDO device
3. Launch PicoForge
4. Click **Refresh** button at top right corner to detect your key
5. Navigate through the sidebar to configure settings:
   - **Home** - Device overview and quick actions
   - **PassKeys** - Passkey management
   - **Configuration** - USB settings, LED options
   - **Security** - Secure boot management (experimental)
   - **Logs** - Real-time event monitoring
   - **About** - Application information

## Disclaimer

{{< hint type=warning >}}
 **USB VID/PID Notice**: The vendor presets provided in this software include USB Vendor IDs (VID) and Product IDs (PID) that are the intellectual property of their respective owners. These identifiers are included for testing and educational purposes only. You are NOT authorized to distribute or commercially market devices using VID/PID combinations you do not own or license. Commercial distribution requires obtaining your own VID from the USB Implementers Forum (usb.org) and complying with all applicable trademark and certification requirements. Unauthorized use may violate USB-IF policies and intellectual property laws. The PicoForge developers assume no liability for misuse of USB identifiers.
{{< /hint >}}

## Source code
You can find the PicoForge source code in the [LibreKeys PicoForge Repository](https://github.com/librekeys/picoforge)
