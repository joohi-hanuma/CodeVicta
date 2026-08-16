# Drowsiness & Yawning Detection Alert 
# Objective:

This project is a real-time driver safety monitoring system that detects drowsiness and yawning using a webcam feed. It analyzes facial landmarks to identify signs of fatigue and triggers a beep sound alert when drowsiness or yawning is detected.

The system is designed to be simple, lightweight, and easy to use with a USB webcam.

# 🚗 Features:

Drowsiness Detection → Uses Eye Aspect Ratio (EAR) to detect prolonged eye closure.

Yawning Detection → Uses Mouth Aspect Ratio (MAR) to detect prolonged mouth opening.

Real-Time Alerts → Activates vibration motor through USB relay module.

Adjustable Sensitivity → EAR and MAR thresholds can be customized.

No Special Camera Needed → Works with any USB webcam.

# 💻 Requirements

* Laptop or PC
  
* Built-in or USB webcam
  
* Python 3.11.9
  
* Required Python libraries for computer vision and data processing


# Libraries:

pip install opencv-python mediapipe pandas pyserial


USB Relay Driver (most modules are plug-and-play, some may need a driver)

# ⚙️ How It Works
1. The webcam captures the driver's face in real time.

2. MediaPipe detects facial landmarks around the eyes and mouth.

3. The system calculates Eye Aspect Ratio (EAR) to monitor eye closure.

4. The system calculates Mouth Aspect Ratio (MAR) to detect yawning.

5.When the defined thresholds are crossed, the system triggers a beep sound alert.


# 📦 Libraries Used:

- **OpenCV** – Webcam access and image processing.
  
- **MediaPipe** – Facial landmark detection.
  
- **SciPy** – Distance calculations for EAR and MAR.
  
- **NumPy** – Numerical operations.
  
- **Pandas** – Detection data handling.
  
- **Pygame** – Beep sound alerts.

  
# 📈 Future Improvements:

* **Add a GUI for adjusting EAR and MAR thresholds.**
  
* **Improve detection accuracy in different lighting conditions.**
  
* **Add additional driver-safety features such as lane-departure detection.**
  
* **Explore IoT-based monitoring in future versions.**
