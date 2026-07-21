# 🎭 Face Mesh & Feature Interaction Suite

An interactive computer vision module built with **OpenCV**, **MediaPipe**, and **NumPy**. This tool performs real-time face mesh tracking, monitors eye states (blink counter and crop views), tracks mouth openness, and calculates head roll orientation.

---

## ✨ Key Features

* **3D Face Mesh Wireframe:** Real-time facial landmark mapping with a smooth semi-transparent overlay.
* **Blink Counter & EAR:** Tracks Eye Aspect Ratio (EAR) to count blinks and detect left/right eye states (`open` / `close`).
* **Live Eye Inspection Tiles:** Real-time cropped, close-up displays of both left and right eyes.
* **Mouth Opening Indicator:** Dynamic visual feedback showing mouth open percentage with responsive geometric overlays.
* **Head Roll Visualizer:** Tracks head tilt and alignment relative to the camera frame.

---

## 🛠️ Prerequisites & Installation

Make sure you have Python installed (supports **Python 3.12+**). Install the required dependencies:

```bash
pip install opencv-python mediapipe numpy
🚀 How to Run
Connect your webcam.

Run the main Python script:

Bash
python main.py
Controls:

Press q or ESC to exit the application.

⚙️ Customizable Parameters
You can easily adjust UI colors, text positions, and sensitivity thresholds directly from the top section of main.py:

Python
# Color Configurations (B, G, R)
TRACK_COLOR = (255, 0, 0)    # Wireframe and overlay color
TEXT_COLOR = (0, 255, 255)   # Neon yellow UI text

# Thresholds
EYE_OPEN_THRESHOLD = 0.28    # Sensitivity for eye blink detection
Part of the GesturePlay — Computer Vision Interaction Suite.
