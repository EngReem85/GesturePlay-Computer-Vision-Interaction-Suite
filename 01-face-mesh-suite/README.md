# 🎭 Face Scan Wireframe — GesturePlay Suite

![Python](https://img.shields.io/badge/Python-3.12-blue?style=for-the-badge&logo=python&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5.0+-red?style=for-the-badge&logo=opencv&logoColor=white)
![MediaPipe](https://img.shields.io/badge/MediaPipe-0.10+-00C7B7?style=for-the-badge&logo=google&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-2.5+-013243?style=for-the-badge&logo=numpy&logoColor=white)

A real-time face tracking application built with **[OpenCV](https://opencv.org/)**, **[Google MediaPipe](https://github.com/google-ai-edge/mediapipe)**, and **[NumPy](https://numpy.org/)** for facial mesh tracking, blink counting, head roll estimation, and mouth analysis.

---

## ✨ Features

- **Real-time Face Mesh:** 468 landmarks mesh tracking via [MediaPipe Face Mesh](https://ai.google.dev/edge/mediapipe/solutions/vision/face_landmarker).
- **Blink Counter:** Eye Aspect Ratio (EAR) calculation for blink detection.
- **Eye Cropping:** Live zoomed viewports for left and right eyes.
- **Head Roll Indicator:** Visual alignment line for head tilt.
- **Mouth Metrics:** Percentage display and responsive circle overlay.

---

## 🚀 Demo

![Face Scan Wireframe Demo](demo.gif)

---

## 📋 Requirements


pip install opencv-python mediapipe numpy
🛠️ Installation
Clone repository:

Bash
git clone [https://github.com/EngReem85/GesturePlay.git](https://github.com/EngReem85/GesturePlay.git)
cd GesturePlay/01-face-mesh-suite
Install dependencies:

Bash
pip install -r requirements.txt
Run:

Bash
python main.py
⚙️ Configuration
Visual Settings
Python
TRACK_COLOR = (255, 0, 0)        # Wireframe color (BGR)
TEXT_COLOR = (0, 255, 255)       # HUD text color
Eye & Blink Detection
Python
BLINK_OFFSET_X = 180              # Counter X position
BLINK_OFFSET_Y = -50              # Counter Y position
EYE_OPEN_THRESHOLD = 0.28        # EAR threshold
Head Roll Display
Python
HEAD_LINE_OFFSET_Y = 190          # Line Y offset
HEAD_LINE_LENGTH = 80             # Line half-length
Mouth Opening Metrics
Python
MOUTH_OFFSET_X = -230             # Display X offset
MOUTH_OFFSET_Y = 0                # Display Y offset
MOUTH_CIRCLE_MAX = 50             # Max circle radius
🎮 Controls
Press q or ESC: Exit application.

🔧 Technical Details
Landmark Indices
Python
LEFT_EYE_IDX = [33, 133, 159, 145, 158, 153]
RIGHT_EYE_IDX = [362, 263, 386, 373, 387, 380]
MOUTH_IDX = [13, 14]
Key Functions
eye_aspect_ratio() — Computes EAR for blink detection.

draw_face_wireframe() — Renders face mesh overlay.

crop_square() — Extracts eye regions.

🎯 Use Cases
Human-Computer Interaction (HCI)

Fatigue Monitoring

Accessibility Tools

Interactive Gaming
