# DetectionModules

Overview
This project provides real-time hand tracking using computer vision and the MediaPipe library. It can detect and track hand landmarks (21 points per hand) from a webcam feed, displaying the results with optional visualization of landmarks and connections between them.

Files
1. HandTrackingModule.py
A reusable module that encapsulates hand detection functionality in a handDetector class. Features include:

Hand detection with configurable parameters (number of hands, confidence thresholds)

Landmark position extraction

Visualization of hand landmarks and connections

FPS calculation for performance monitoring

2. HandTrackingNew.py
A simplified implementation that uses the handDetector class from HandTrackingModule.py to:

Capture webcam video

Detect and track hands

Display landmarks and FPS

Print thumb tip position (landmark 4)

3. main.py
A basic implementation of hand tracking without using the custom module. It:

Initializes MediaPipe hands directly

Processes webcam frames

Draws landmarks and connections

Displays FPS

Prints all landmark positions

How to Use
Requirements:

Python 3.x

OpenCV (pip install opencv-python)

MediaPipe (pip install mediapipe)

Running the project:

Run any of the Python files to start hand tracking:

bash
python main.py
or

bash
python HandTrackingNew.py
Controls:

Press 'q' or Ctrl+C to quit the application

The program will display:

Real-time camera feed with hand landmarks

Current FPS in the top-left corner

In console: coordinates of detected landmarks

Customization Options
In HandTrackingModule.py, you can adjust:

maxHands: Maximum number of hands to detect (default: 2)

detectionCon: Detection confidence threshold (default: 0.5)

trackCon: Tracking confidence threshold (default: 0.5)

Applications
This hand tracking system can be used as a foundation for:

Gesture recognition systems

Sign language interpretation

Virtual reality controls

Human-computer interaction projects

Future Enhancements
Add gesture recognition capabilities

Implement multi-hand tracking with identification

Add 3D position estimation

Create interactive applications using the hand tracking data

Note
For best results, ensure good lighting conditions and keep your hands clearly visible to the camera. Performance may vary depending on your hardware.
