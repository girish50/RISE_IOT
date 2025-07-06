# TankIntel – Smart Water Level Monitoring System

## 📌 Project Overview

TankIntel is a microcontroller-based water level monitoring system developed using Arduino Uno.  
It detects the water level in a tank using an ultrasonic sensor and gives real-time updates via:

- 16x2 LCD Display (I2C based)
- RGB LED indicators (Red, Blue, Green)
- Buzzer alert for critical levels

This project was created as part of an IoT & Embedded Systems internship to address the common issue of manual tank monitoring and water wastage.

---

## 🎯 Objective

- Monitor water levels in a tank automatically.
- Alert users visually (LED + LCD) and audibly (buzzer).
- Eliminate the need for manual water level checking.
- Provide a cost-effective embedded solution.

---

## 🔧 Components Used

| Component                        | Quantity |
|----------------------------------|----------|
| Arduino Uno                      | 1        |
| Ultrasonic Sensor (HC-SR04)      | 1        |
| 16x2 LCD Display with I2C Module | 1        |
| RGB LED (Red, Blue, Green)       | 1 each   |
| Buzzer                           | 1        |
| Breadboard + Jumper Wires        | As needed |

---

## ⚙️ Working Principle

- The ultrasonic sensor calculates distance from the sensor to the water surface.
- Based on the distance:
  - **≥ 200 cm** → **EMPTY**  
    - Red LED ON  
    - Buzzer active (high frequency)  
    - LCD shows: `Status: EMPTY`
  - **70 cm ≤ distance < 200 cm** → **MEDIUM**  
    - Blue LED ON  
    - No buzzer  
    - LCD shows: `Status: MEDIUM`
  - **< 70 cm** → **FULL**  
    - Green LED ON  
    - Buzzer active (high frequency)  
    - LCD shows: `Status: FULL`

- The system updates every second.

---

## 🖥️ Sample LCD Output

