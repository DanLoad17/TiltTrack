# TiltTrack Architecture

## Objective

TiltTrack is an embedded motion-tracking system designed to explore the interaction between embedded firmware, Linux kernel development, and computer graphics.

The system consists of:

- ESP32 DevKit V1
- AT42QT1012 capacitive touch sensor
- MPU6500 inertial measurement unit (IMU)
- USB CDC serial communication
- Custom Linux kernel character driver
- OpenGL visualization application

The touch sensor enables or disables tracking. The ESP32 reads motion data from the MPU6500 over I²C, packages it into a serial protocol, and transmits it over USB. A custom Linux driver exposes the data through `/dev/tilttrack`, which is then consumed by an OpenGL application that renders a real-time 3D cube representing the device's orientation.
