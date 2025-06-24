# Wire Bending Machine 🤖

A Mechatronics Project for Programmable 3D Wire Shaping
*(TA212 Course Project)*

---

## 📌 Overview

The **Wire Bending Machine** is a programmable electromechanical system capable of bending wire in **any direction and angle** in 3D space. Built as part of the **TA212 course**, this project combines **mechanical design**, **electronics**, and **software control** to automate wire shaping.

The machine is controlled by an **Arduino-based system**, integrating multiple types of motors to execute precise feed and bend sequences, with support for **manual** and **pattern-based** operations like *star*, *cube*, and *stand*.

---

## 🛠️ Core Features

* **3-Axis Bending**: Stepper motors control wire bending across X, Y, and Z directions.
* **Programmable Patterns**: Predefined geometric wire forms (*star*, *cube*, *stand*) can be bent at the push of a command.
* **Manual Control Mode**: Custom wire movements and angles using serial commands.
* **Real-Time Servo Bending Arm**: A servo-driven pin lifts or lowers to apply precise bends.
* **Wire Feeding System**: A DC motor feeds wire forward before each bend.

---

## 🧩 Components Used

| Component            | Purpose                               |
| -------------------- | ------------------------------------- |
| Stepper Motors       | Control bending in X, Y, Z axes       |
| DC Motor             | Feed wire forward                     |
| Servo Motor          | Raise/lower the bending pin           |
| Arduino Board        | Central control unit (code execution) |
| AccelStepper Library | Smooth motion control for steppers    |
| Custom Frame         | Holds motor assembly and guides wire  |

---

## 🧠 Control Logic Overview

* **Feeding**: Wire is fed in fixed millimeter units, mapped to stepper steps.
* **Bending**: Servo lowers the bending pin, and the stepper motor executes rotation.
* **Z-Axis Rotation**: Allows changing the wire plane by rotating the axis.

Predefined patterns like `star()`, `cube()`, and `stand()` involve specific sequences of feeds, bends, and rotations to produce recognizable wire shapes.

### Manual Mode Commands

| Command | Function                                   |
| ------- | ------------------------------------------ |
| `f30`   | Feed 30mm of wire                          |
| `b90`   | Bend 90 degrees clockwise                  |
| `b-60`  | Bend 60 degrees counter-clockwise          |
| `z45`   | Rotate Z-axis by 45 degrees clockwise      |
| `z-30`  | Rotate Z-axis 30 degrees counter-clockwise |
| `end`   | Exit manual mode                           |

---

## 📂 File Structure

```
WireBendingMachine/
├── WireBender.ino           // Main Arduino code
├── README.md                // Project documentation
```

## Snapshot
Here a snapshot of our project.
![Machine](https://github.com/user-attachments/assets/77bb54cf-c28b-4810-a907-0886e978725a)

