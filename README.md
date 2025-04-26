# MotorDriver Library for ESP32 🛠️

Welcome to the **MotorDriver** library, designed for controlling DC motors using the **L298N motor driver** on the **ESP32** platform. This library allows you to control the speed and direction of up to two motors via **PWM**.

## 🚀 Overview

This library provides an easy-to-use interface to control **one or two motors** connected to an L298N motor driver. It supports **PWM speed control** and **direction control** (forward/backward).

## 💻 Installation

### Step 1: Clone the Repository

Clone the repository to your local machine:

```bash
git clone https://github.com/EmDonato/motorDriver.git
```
### Step 2: Add to Arduino Libraries

Copy the motorDriver folder into your Arduino libraries directory:

    Windows: Documents/Arduino/libraries/

    Mac/Linux: ~/Arduino/libraries/

Once the library is installed, restart the Arduino IDE if it was open.
## 🛠️ Features

- **One or Two Motors Control**: Easily manage up to two motors.
- **PWM Speed Control**: Control the motor speed via PWM signals.
- **Forward and Backward Motion**: Direct the motors to move in both directions.
- **ESP32 Compatibility**: Fully compatible with ESP32 development boards.

## 🚦 Quick Start Guide

To get started, include the MotorDriver.h file in your sketch and initialize the motors.
Example Code

```bash
#include "MotorDriver.h"

// Initialize motor control for one motor
L298N motor(0, 5000, 8, 1);  // PWM Channel, Frequency, Resolution, Number of Motors

void setup() {
    motor.init(18, 19, 21); // Pin configuration for the motor
}

void loop() {
    motor.forward(200);   // Move motor forward with PWM value 200
    delay(1000);          // Wait for 1 second

    motor.backward(200);  // Move motor backward
    delay(1000);

    motor.stop();         // Stop the motor
    delay(1000);          // Wait for 1 second
}
```

## ⚙️ Dependencies

This library is designed for ESP32 and requires the ledcWrite() function for PWM control. Ensure that you have the ESP32 board package installed in the Arduino IDE.

Enjoy building with MotorDriver! 🚗💨

