# 🤖 Line Following Robot 

A smart **Arduino-based Line Following Robot** designed to autonomously navigate along a predefined path using five infrared sensors and differential motor control. The robot continuously detects the line position and adjusts its movement through left and right corrections to ensure accurate path tracking.

This project demonstrates the practical implementation of **embedded systems**, **sensor interfacing**, and **motor control algorithms** using Arduino.

---

## ✨ Features

### 🔍 Intelligent Line Detection

* Uses **five IR sensors** for accurate line sensing.
* Detects the position of the line in real time.
* Supports center, left, and right line tracking.

### ⚙️ Dynamic Motion Control

* Smooth forward movement.
* Automatic left and right corrections.
* Hard turns for sharp curves.
* Line recovery mechanism when the path is temporarily lost.

### 🚗 Differential Drive System

* Independent control of left and right motors.
* Adjustable motor speed using PWM.
* Stable navigation through speed balancing.

### 📊 Serial Monitoring

* Real-time sensor data output through the Serial Monitor.
* Simplifies testing and debugging.
* Helps with threshold calibration and performance tuning.

---

## 🛠 Hardware Components

| Component                 |    Quantity |
| ------------------------- | ----------: |
| Arduino Uno/Nano          |           1 |
| L298N Motor Driver Module |           1 |
| DC Motors                 |           2 |
| IR Sensor Array           |           5 |
| Robot Chassis             |           1 |
| Wheels                    |           2 |
| Caster Wheel              |           1 |
| Battery Pack              |           1 |
| Jumper Wires              | As Required |

---

## ⚡ Working Principle

The robot continuously reads data from five infrared sensors:

* **Center Sensor (S2)** → Moves forward.
* **Left Sensors (S0, S1)** → Performs left correction.
* **Right Sensors (S3, S4)** → Performs right correction.
* **Sharp turns** are handled when outer sensors detect the line.
* If the line is temporarily lost, the robot performs a search movement to regain the path.

---

## 🧠 Control Algorithm

The control logic is based on sensor states:

1. Read all five sensor values.
2. Compare readings against a threshold.
3. Determine the position of the line.
4. Apply:

   * Forward motion
   * Slight left correction
   * Slight right correction
   * Hard left turn
   * Hard right turn
5. Continue tracking until the path ends.

---

## 🔌 Pin Configuration

### Motor Driver Connections

| Arduino Pin | Function                |
| ----------- | ----------------------- |
| 9           | ENA (Left Motor Speed)  |
| 8           | IN1                     |
| 7           | IN2                     |
| 6           | ENB (Right Motor Speed) |
| 5           | IN3                     |
| 4           | IN4                     |

### Sensor Connections

| Sensor | Arduino Pin |
| ------ | ----------- |
| S0     | A0          |
| S1     | A1          |
| S2     | A2          |
| S3     | A3          |
| S4     | A4          |

---

## 🚀 Technologies Used

* **Arduino IDE**
* **Embedded C/C++**
* **PWM Motor Control**
* **Infrared Sensors**
* **L298N Motor Driver**

---

## 📈 Applications

* Autonomous robots
* Industrial material transportation
* Warehouse automation
* Path-following vehicles
* Educational robotics projects
* Robotics competitions

---

## 🔮 Future Improvements

Planned enhancements include:

* PID-based line following for smoother navigation.
* Adjustable speed modes.
* Bluetooth control and monitoring.
* Obstacle avoidance using ultrasonic sensors.
* Wireless telemetry.
* Junction and maze-solving algorithms.
* OLED display for sensor status visualization.

---

## 📸 Project Preview

<img width="233" height="299" alt="image" src="https://github.com/user-attachments/assets/69774520-9bca-41b7-8c8d-7d74c77a68be" />
<img width="624" height="420" alt="image" src="https://github.com/user-attachments/assets/bbdfb7dc-d8b5-4416-9450-82576e55a502" />

---

---


