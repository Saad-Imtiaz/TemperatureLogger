# TemperatureLogger 🌡️

## Overview 📖
TemperatureLogger is an IoT project designed to measure and log temperature and humidity data. Utilizing the ESP-12E module and DHT-11 sensor, it sends this data to ThingSpeak for monitoring and analysis, then enters a power-saving deep sleep mode.

## Hardware Requirements 🔌
- ESP-12E Module
- DHT-11 Temperature and Humidity Sensor

## Software Dependencies 📚
- ESP8266WiFi
- ThingSpeak
- Adafruit_Sensor
- DHT Sensor Library

## Setup and Configuration 🛠️
1. **Hardware Setup:**
   - Connect the DHT-11 sensor's data pin to D4 on the ESP-12E.

2. **WiFi Configuration:**
   - Rename `secrets_example.h` to `secrets.h`.
   - Update with your WiFi network details.

3. **ThingSpeak Channel:**
   - Set up a ThingSpeak account and create a channel.
   - Add your Channel ID and Write API Key to `secrets.h`.

4. **Code Upload:**
   - Flash the provided sketch to your ESP-12E module.

## Functionality 🌟
- Connects to WiFi.
- Reads temperature and humidity.
- Sends data to ThingSpeak.
- Enters deep sleep for 10 minutes for efficiency.

## Deep Sleep Mode 💤
The device conserves energy by sleeping for 10-minute intervals between data transmissions, making it suitable for long-term deployment.
