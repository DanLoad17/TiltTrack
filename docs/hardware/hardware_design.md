# TiltTrack Hardware Design

## Overview

TiltTrack is an embedded motion tracking device using an ESP32 microcontroller,
MPU6500 IMU, and AT42QT1012 capacitive touch sensor.

The device detects user activation through touch and tracks orientation changes
using the MPU6500 motion sensor.

---

# Components

## Microcontroller

ESP32 DevKit V1

Responsibilities:
- Communicate with MPU6500 through I2C
- Read touch sensor state
- Send motion data to Linux host through USB serial

---

## Motion Sensor

MPU6500

Features used:
- 3-axis accelerometer
- I2C communication

Configuration:
- Address: 0x68
- Interface: I2C
- Initial communication method: polling

---

## Touch Sensor

AT42QT1012

Configuration:
- Digital output mode
- Connected to ESP32 GPIO
- Used as tracking enable switch

---

# Communication

## MPU6500

Protocol:
I2C

Connections:

ESP32 GPIO21 -> SDA

ESP32 GPIO22 -> SCL

---

## Computer Communication

ESP32 -> Linux VM

Protocol:
USB Serial

---

# Power

Supply voltage:

3.3V logic system

Components:

ESP32:
USB powered

MPU6500:
3.3V

AT42QT1012:
3.3V

---

# MPU6500 Configuration

Device address:

0x68

Reason:

AD0 connected to GND

---

# Initial Firmware Strategy

Startup:

1. Initialize I2C
2. Verify WHO_AM_I register
3. Wake MPU6500
4. Configure accelerometer
5. Begin polling measurements

Main Loop:

1. Read touch sensor
2. If enabled:
   - Read accelerometer data
   - Convert raw values
   - Send over serial

