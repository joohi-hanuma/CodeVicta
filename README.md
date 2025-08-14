Drowsiness & Yawning Detection with USB Vibration Alert
📌 Overview

This project is a real-time driver safety monitoring system that detects drowsiness and yawning using a webcam feed.
When a detection is made, the system sends a signal to a USB relay module, which triggers a USB vibration motor to alert the driver.

Designed to be low-cost, portable, and easy to integrate with laptops or embedded systems like the Jetson Nano.

🚗 Features

Drowsiness Detection → Uses Eye Aspect Ratio (EAR) to detect prolonged eye closure.

Yawning Detection → Uses Mouth Aspect Ratio (MAR) to detect prolonged mouth opening.

Real-Time Alerts → Activates vibration motor through USB relay module.

Adjustable Sensitivity → EAR and MAR thresholds can be customized.

No Special Camera Needed → Works with laptop webcam or any USB webcam.

🛠 Hardware Requirements

USB Relay Module (1-channel, 5V)

USB Vibration Motor (USB powered)

USB A-to-B Cable (printer-style) for connecting relay to laptop

Laptop/PC with USB ports and webcam

💻 Software Requirements

Python 3.11.9

Libraries:

pip install opencv-python mediapipe pandas pyserial


USB Relay Driver (most modules are plug-and-play, some may need a driver)

⚙ How It Works

Webcam captures driver’s face in real-time.

MediaPipe detects facial landmarks for eyes and mouth.

EAR & MAR values are calculated from the landmarks.

If thresholds are crossed:

Sends command to USB relay module via PySerial.

Relay powers USB vibration motor → alerts driver.

🔌 Circuit Connection Diagram

Laptop USB Port → USB A-to-B Cable → USB Relay Module

Relay Output → USB Vibration Motor

Vibration motor is powered only when relay is activated.
