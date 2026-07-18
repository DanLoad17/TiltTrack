# TiltTrack

TiltTrack is an embedded Linux systems project that creates a custom motion tracking device using an ESP32, accelerometer, touch sensor, Linux kernel driver, and OpenGL visualization application.

The goal of this project is to design a complete hardware-to-software pipeline:
MMA845X Accelerometer
|
|
ESP32 Firmware
|
|
USB Serial Communication
|
|
Linux Kernel Driver
|
|
User Space Application
|
|
OpenGL Visualization


## Project Goals

- Interface an MMA845X 3-axis accelerometer using I2C
- Use an AT42QT1012 capacitive touch sensor as an activation switch
- Develop ESP32 firmware for sensor acquisition and communication
- Design a custom Linux kernel driver
- Communicate with hardware through the Linux device subsystem
- Create an OpenGL application that visualizes device orientation

## Hardware

- ESP32 DevKit V1
- MMA845X 3-axis accelerometer
- AT42QT1012 capacitive touch sensor

## Software

- Ubuntu Linux
- C/C++
- Linux Kernel Modules
- USB Serial Communication
- OpenGL
- Git

## Repository Structure

TiltTrack/
|
├── firmware/ ESP32 firmware
├── driver/ Linux kernel driver
├── application/ OpenGL user application
├── hardware/ Hardware documentation
├── docs/ Design documentation
└── tests/ Testing


## Current Status

Project initialization completed.

Development roadmap:

- [x] Repository setup
- [ ] ESP32 communication
- [ ] Sensor integration
- [ ] USB protocol design
- [ ] Linux driver development
- [ ] OpenGL visualization
