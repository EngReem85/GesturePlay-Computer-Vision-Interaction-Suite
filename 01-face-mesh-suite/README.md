# 🎭 Face Mesh & Feature Interaction Suite

![Python](https://img.shields.io/badge/Python-3.12-blue?style=for-the-badge&logo=python&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5.0+-red?style=for-the-badge&logo=opencv&logoColor=white)
![MediaPipe](https://img.shields.io/badge/MediaPipe-0.10+-00C7B7?style=for-the-badge&logo=google&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-2.5+-013243?style=for-the-badge&logo=numpy&logoColor=white)

An interactive, real-time Computer Vision analysis module powered by **[Google MediaPipe](https://github.com/google-ai-edge/mediapipe)** and **[OpenCV](https://opencv.org/)**. This component performs high-fidelity 3D facial landmark mapping, tracks pupil states, measures Eye Aspect Ratio (EAR) for blink counting, calculates mouth opening dynamics, and estimates head roll orientation.

---

## 🔥 Key Features

* **🕸️ 3D Face Wireframe Mapping:** Renders a 468+ landmark mesh overlay using [MediaPipe Face Mesh](https://ai.google.dev/edge/mediapipe/solutions/vision/face_landmarker).
* **👁️ Real-time Eye Inspection & EAR:** Calculates Eye Aspect Ratio (EAR) to detect individual eye states (`open` / `close`) and tracks total blinks dynamically.
* **🔎 Live Eye Crop Tiles:** Isolates and displays real-time zoomed viewports for both left and right eyes with zero latency.
* **😮 Dynamic Mouth Metric:** Quantifies mouth displacement and visualizes opening intensity (%) through responsive geometric overlays.
* **📐 Head Roll Orientation Tracker:** Calculates horizontal head inclination and spatial rotation relative to the webcam feed.

---

## 🛠️ Built With & Dependencies

This module relies on the following core technologies:

| Library | Version / Link | Role in Project |
| :--- | :--- | :--- |
| **MediaPipe** | [v0.10+](https://ai.google.dev/edge/mediapipe/solutions/guide) | High-performance face landmark detection & mesh geometry |
| **OpenCV** | [v5.0+](https://docs.opencv.org/) | Video stream processing, UI rendering, and spatial drawing |
| **NumPy** | [v2.5+](https://numpy.org/) | High-speed vector math for Euclidean distances & EAR logic |

---

## 🚀 Quick Start

### 1. Installation

Ensure you have **Python 3.12+** installed, then run:

```bash
pip install opencv-python mediapipe numpy
2. Execution
Run the standalone module using Python:

Bash
python main.py
Controls: Press q or ESC at any time to exit the live camera feed.

⚙️ Configuration Parameters
You can fine-tune UI colors, threshold tolerances, and offsets at the top of main.py:

Python
# Color Palette (BGR Format)
TRACK_COLOR = (255, 0, 0)     # Electric Blue (Wireframe & HUD elements)
TEXT_COLOR  = (0, 255, 255)   # Neon Yellow (Overlay metrics)

# Detection Thresholds
EYE_OPEN_THRESHOLD = 0.28     # Sensitivity for EAR blink detection
MOUTH_CIRCLE_MAX   = 50       # Scale factor for mouth openness
