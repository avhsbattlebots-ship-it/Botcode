# Botcode
The base code for controlling the bot
# ESP32 Arduino Setup Guide

## Arduino IDE Installation Complete ✅

The Arduino IDE has been successfully installed on your Mac and is available in your Applications folder.

## Next Steps for ESP32 Development

### 1. Configure Arduino IDE for ESP32

1. Open Arduino IDE
2. Go to **File > Preferences**
3. Add this URL to "Additional Boards Manager URLs":
   ```
   https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
   ```
4. Click OK

### 2. Install ESP32 Board Package

1. Go to **Tools > Board > Boards Manager**
2. Search for "esp32"
3. Install "ESP32 by Espressif Systems"
4. Wait for installation to complete

### 3. Select Your Board

1. Go to **Tools > Board > ESP32 Arduino**
2. Select your specific ESP32 board (e.g., "ESP32 Dev Module")

### 4. Configure Board Settings

Set the following in **Tools** menu:
- **Upload Speed**: 921600
- **CPU Frequency**: 240MHz (WiFi/BT)
- **Flash Frequency**: 80MHz
- **Flash Mode**: QIO
- **Flash Size**: 4MB (32Mb)
- **Partition Scheme**: Default 4MB with spiffs
- **Port**: Select your ESP32's COM port

## Your Battle Bot Project

Your `esp.cpp` file contains:
- Bluetooth Serial communication for remote control
- Motor control for a 4-wheel robot
- Key mapping for movement (WASD controls)

### Pin Configuration:
- Motor1A: GPIO 26
- Motor1B: GPIO 33  
- Motor2A: GPIO 25
- Motor2B: GPIO 32

### Usage:
- Connect to Bluetooth device named "Battle Bot"
- Send WASD keys to control movement
- Send '!' followed by a key to release that key

## Uploading Code

1. Connect your ESP32 via USB
2. Select the correct port in Tools > Port
3. Click Upload button
4. If upload fails, hold BOOT button while uploading

## Troubleshooting

- **Upload Issues**: Try lowering upload speed to 115200
- **Bluetooth Issues**: Ensure ESP32 has adequate power supply
- **Motor Issues**: Check wiring and power supply for motors
