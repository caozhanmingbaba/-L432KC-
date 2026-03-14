# Smart Locker Security and Environmental Monitoring System

## Overview
This repository contains the embedded software for a smart locker system, driven by a Nucleo L432KC mbed board. It integrates password-based access control with real-time environmental monitoring.

## Core Features
* **Access Control:** Two-button password input system. A correct entry illuminates the Green LED, while an incorrect attempt triggers the Red LED and a buzzer warning.
* **Temperature Monitoring:** Utilizes a TMP102 sensor. A continuous buzzer alarm is triggered if the internal temperature exceeds 29°C.
* **Tamper Detection:** Uses an ADXL345 accelerometer to monitor movement. An alarm triggers if the acceleration change exceeds 1.2g.
* **Data Visualization:** Outputs specific temperature and acceleration readings to a connected PC.

## Hardware Setup
* **Microcontroller:** Nucleo L432KC
* **Sensors:** TMP102, ADXL345
* **Peripherals:** 2x Push Buttons, 1x Green LED, 1x Red LED, 1x Buzzer

## Pin Configuration
The system relies heavily on the I2C protocol for sensor communication.

| Component | Pin | Type |
| :--- | :--- | :--- |
| TMP102 / ADXL345 SDA | `D0` | I2C  |
| TMP102 / ADXL345 SCL | `D1` | I2C  |
| Green LED | `D4` | Digital Out  |
| Red LED | `D12` | Digital Out  |
| Button 1 | `D9` | Digital In  |
| Button 2 | `D10` | Digital In  |
| Buzzer | `D13` | Digital Out  |

## Development Environment
* **IDE:** Offline MBED STUDIO.
* **Library Note:** Mbed function libraries are stored locally within the project folder to bypass regional compilation restrictions.

## Author
Song Zexu 
