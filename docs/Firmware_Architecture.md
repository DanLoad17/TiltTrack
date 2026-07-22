# TiltTrack Firmware Architecture

## Hardware

ESP32 DevKit V1
MPU6500 IMU
AT42QT1012 Touch Sensor

## Communication

ESP32 ↔ MPU6500:
I2C

ESP32 ↔ Computer:
USB Serial

## Operating Mode

Polling initially

## Startup Sequence

1. Initialize ESP32
2. Initialize I2C
3. Verify MPU6500 WHO_AM_I
4. Wake MPU6500
5. Configure accelerometer
6. Begin sampling

## Main Loop

1. Check touch sensor
2. If tracking enabled:
    - Read acceleration
    - Convert raw values
    - Send serial data

3. Repeat
