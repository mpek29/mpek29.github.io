---
layout: page
title: SmartRadioAlarm
description: 🎧 ESP32 WiFi radio, BT speaker & alarm clock
full_name: mpek29/SmartRadioAlarm
img: assets/img/projects/SmartRadioAlarm/main.png
importance: 1
git: https://github.com/mpek29/SmartRadioAlarm
github: https://github.com/mpek29/SmartRadioAlarm
category: Computer Science
subcategory: Firmware Development
---



**SmartRadioAlarm** is an open-source project that integrates **Internet Radio**, **Bluetooth audio playback**, and a **programmable alarm** into a single device. Users can control it via **physical buttons** on the device or through a **cross-platform Flutter app** connected over the local network.

## 🎯 Purpose


* 🎵 **Audio Streaming**: Stream music from Internet radio or Bluetooth devices.
* ⏰ **Alarm Functionality**: Schedule alarms with custom audio streams.
* 🔘 **User Control**: Easily adjust volume, play/pause, and stop using physical buttons.
* 🌐 **Network Configuration**: Configure the device via Wi-Fi and control it using a REST API.
* 🛠️ **Open-source & Customizable**: Modify and extend for various audio or alarm use cases.

## 📝 Features


| 🏷️ Feature                      | 🔍 Description                                                   |
| -------------------------------- | ---------------------------------------------------------------- |
| 🎶 **Internet Radio**            | Stream music from online sources                                 |
| 📱 **Bluetooth A2DP Sink**       | Play audio from smartphones or other BT devices                  |
| 🔊 **Volume & Playback Control** | Control volume and playback via buttons or mobile app            |
| ⏰ **Programmable Alarm**         | Set alarm time and choose a custom audio stream                  |
| 🌐 **REST API**                  | Local API for configuration and real-time control                |
| 🖥️ **ESP32 + I2S DAC**          | High-quality audio output through DAC (PCM5102, MAX98357A, etc.) |
| 🌍 **Cross-platform App**        | Flutter app compatible with both Android & iOS                   |

## ⚡ Quick Setup


1. Clone the repository:

   ```bash
   git clone https://github.com/mpek29/SmartRadioAlarm.git
   cd SmartRadioAlarm
   ```
2. Set the ESP32 target:

   ```bash
   idf.py set-target esp32
   ```
3. Build, flash, and monitor:

   ```bash
   idf.py build flash monitor
   ```

## 📚 Full Documentation


For detailed architecture, schematics, API reference, and configuration instructions, see the [`/docs`](./docs) folder.

