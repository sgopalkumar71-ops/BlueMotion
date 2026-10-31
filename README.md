# BlueMotion

### Bluetooth Controlled Smart Robotic Car

<img width="1069" height="1001" alt="WhatsApp Image 2026-10-21 at 10 30 21 AM" src="https://github.com/user-attachments/assets/ada2279d-1b51-47f7-ade4-fe3e608a70f6" />

<img width="800" height="800" alt="Wx_Q0WfPLUQvkGLHaoKcrzxoHH5mHSFU-xOprqhQznZQEi983inbPuavKLH4VQG0e_i6p6VR5WNhWhtJxk4BrG9bcvlXzSb1V142pAXUaYnE_bytxAQ0gwGJXwqmSTcBm8YX0jQSqWu6Jnc-kLfQhhbioDTmxre_Dje-aXpgTIYtN2ybNnu0IMIjMIbIC4hi" src="https://github.com/user-attachments/assets/1541a051-7ec6-43e3-9e16-0f426ab15717" />

<img width="812" height="757" alt="Screenshot 2026-08-05 220747" src="https://github.com/user-attachments/assets/6c527119-df11-4a51-be15-aedee872e136" />

<img width="1152" height="864" alt="image" src="https://github.com/user-attachments/assets/b994d9de-bf16-4782-947a-beed7e6d4887" />


## 📌 Project Overview

**RoboDrive X** is an Arduino-based Bluetooth-controlled robotic car designed to move wirelessly using commands sent from an Android smartphone.

The project uses an HC-05 Bluetooth module for wireless communication, an Arduino UNO as the main controller, and an L298N motor driver to control the DC motors.

The car can move forward, backward, turn left, turn right, stop, and adjust its speed through Bluetooth commands.

## ✨ Key Features

-  Wireless control through an Android smartphone.
-  HC-05 Bluetooth communication.
-  Forward movement.
-  Backward movement.
-  Left turn.
-  Right turn.
-  Instant stop command.
-  Adjustable motor speed using PWM.
-  Command-based movement control.

## 🔧 Hardware Components

| Component | Purpose |
|---|---|
| Arduino UNO R3 | Main microcontroller |
| HC-05 Bluetooth Module | Wireless communication |
| L298N Motor Driver | DC motor control |
| DC Geared Motors | Car movement |
| Robot Car Chassis | Mechanical structure |
| Wheels | Movement |
| Battery | Power supply |
| Jumper Wires | Circuit connections |

## 🔌 Pin Configuration

### L298N Motor Driver to Arduino UNO

| L298N Pin | Arduino Pin |
|---|---|
| ENA | 5 |
| IN1 | 8 |
| IN2 | 7 |
| IN3 | 4 |
| IN4 | 3 |
| ENB | 6 |

### HC-05 Bluetooth Connection

For the direct hardware serial configuration in this sketch:

| HC-05 | Arduino UNO |
|---|---|
| TXD | RX (Pin 0) |
| RXD | TX (Pin 1) |
| GND | GND |
| VCC | 5V (HC-05 breakout board) |

**Important:** Disconnect HC-05 TX/RX from Arduino pins 0 and 1 while uploading code. Use appropriate voltage-level shifting for the HC-05 RX input.

## 🎮 Bluetooth Commands

| Command | Action |
|---|---|
| F | Move Forward |
| B | Move Backward |
| L | Turn Left |
| R | Turn Right |
| S | Stop |
| 0-9 | Adjust Speed |
| q | Maximum Speed |

### ⚡ Speed Control

The project uses PWM-based motor speed control.

- Speed 0: PWM value 100
- Speed 5: PWM value approximately 186
- Speed 9: PWM value 255
- Command q: Maximum speed 255

## ⚙️ Working Principle

1. The Android smartphone sends a command through Bluetooth.
2. The HC-05 receives the command and transfers it to Arduino UNO.
3. Arduino processes the received character.
4. The L298N motor driver controls the direction and speed of the motors.
5. The robotic car performs the requested movement.

## 💻 Software Requirements

- Arduino IDE
- Arduino UNO board package
- Bluetooth terminal/controller Android application

No additional Arduino libraries are required for this sketch.

##  How to Run

1. Install Arduino IDE.
2. Connect Arduino UNO to your computer.
3. Open `Arduino/RoboDrive_X.ino`.
4. Select Arduino UNO board and correct COM port.
5. Upload the code.
6. Connect the HC-05 module after uploading.
7. Pair your smartphone with HC-05.
8. Open a Bluetooth controller application.
9. Send F, B, L, R, S or speed commands.

**Serial Communication:** 9600 baud.

##  Future Improvements

- Add obstacle detection using ultrasonic sensors.
- Integrate ESP32 for Wi-Fi control.
- Add mobile application with a graphical interface.
- Implement autonomous navigation.
- Add camera-based remote monitoring.

## 👨‍💻 Developer

**Gopal Kumar Sahu**

Student | Aspiring Software Developer | Robotics & Embedded Systems Enthusiast

GitHub: https://github.com/sgopalkumar71-ops

---

<p align="center">
  ⭐ If you find this project interesting, consider giving it a star!
  <br/>
  <b>Learn • Build • Innovate</b>
</p>
