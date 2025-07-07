# Real-Time Hand Tracking with MediaPipe & OpenCV

A real-time hand tracking solution using **MediaPipe** and **OpenCV** that detects and visualizes hand landmarks from a webcam feed.

---

## 📁 File Structure

HandTrackingProject/
├── HandTrackingModule.py # Custom hand detection module
├── HandTrackingNew.py # Simplified implementation using the module
└── main.py # Basic hand tracking implementation


---

## Detection Modules

### HandTrackingModule.py

A reusable class-based module for hand tracking and landmark detection.

#### Key Methods

- `findHands()`: Detects hands and draws landmarks  
- `findPosition()`: Returns landmark coordinates in pixel space

---

## Implementations

### HandTrackingNew.py

- Uses the custom `handDetector` class  
- Tracks **thumb tip position** (Landmark #4)  
- Displays **real-time FPS**

### main.py

- Direct implementation using MediaPipe  
- Shows **all 21 landmarks per hand**  
- Prints **complete landmark data** in the console

---

## Setup & Usage

### Install Dependencies

```bash
pip install opencv-python mediapipe

python HandTrackingNew.py  # Recommended implementation
# or
python main.py             # Basic implementation
```

## configuration

You can modify the following parameters inside HandTrackingModule.py to control tracking behavior:
```
def __init__(self, 
             mode=False,          # Static image mode
             maxHands=2,          # Max hands to detect
             detectionCon=0.5,    # Detection confidence threshold
             trackCon=0.5):       # Tracking confidence threshold
```

## output features

- Real-time hand landmark visualization
- FPS counter on the video stream
- Console output of landmark positions
- Supports multiple hands tracking
