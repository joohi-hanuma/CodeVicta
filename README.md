This project is a real-time driver safety monitoring system that detects drowsiness and yawning using a webcam feed.
It uses a two-stage alert mechanism:
Stage 1: Beep sound alert.
Stage 2: Beep sound + USB vibration motor alert.
The system connects to a USB relay module that controls the vibration motor.
🚗 Features:
Drowsiness Detection → Eye Aspect Ratio (EAR) for prolonged eye closure.
Yawning Detection → Mouth Aspect Ratio (MAR) for prolonged mouth opening.
Two-Stage Alerts → Gradual warning system to avoid unnecessary vibration.
Real-Time Processing → Uses MediaPipe and OpenCV for face/landmark detection.
Plug-and-Play USB Relay → No complex wiring.
🛠 Hardware Requirements:
USB Relay Module (1-channel, 5V)
USB Vibration Motor (USB powered)
USB A-to-B Cable (printer-style) for connecting relay to laptop
Laptop/PC with webcam and USB ports
💻 Software Requirements:
Python 3.11.9
Libraries:
OpenCV – For video capturing, image processing, and face landmark detection.
Mediapipe – For facial landmark detection (eyes and mouth).
PySerial – For communication with external devices (e.g., DC motor, Arduino).
SciPy – For calculating distances between facial landmarks (EAR, MAR).
NumPy – For numerical operations.
Pandas – For storing and analyzing detection data.
Playsound / Pygame (optional) – For playing alert sounds.
⚙ How It Works:
Webcam feed is processed with MediaPipe to get facial landmarks.
EAR & MAR values are calculated to monitor eye closure and yawning.
Alert Logic:
Stage 1: If mild drowsiness/yawning → play beep sound.
Stage 2: If condition persists → activate USB relay + vibration motor and play beep sound together.
🔌 Circuit Connection Diagram:
Laptop USB Port → USB A-to-B Cable → USB Relay Module
Relay Output → USB Vibration Motor
Relay powers vibration motor only when Stage 2 is triggered.
📈 Future Improvements:
Adjustable EAR/MAR thresholds via GUI.
Multi-feature driver safety system (lane departure, collision detection).
IoT integration for fleet monitoring.
