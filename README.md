# AI Virtual Mouse using Hand Gesture Recognition

A real-time computer vision project that lets you control your mouse using hand gestures captured through a webcam — no physical mouse needed.

## Tech Stack

- **Language:** Python
- **Computer Vision:** OpenCV
- **Hand Tracking:** MediaPipe
- **Numerical Processing:** NumPy
- **Mouse Control:** AutoPy

## How It Works

1. The webcam captures a live video feed.
2. **MediaPipe** detects hand landmarks (21 key points per hand) in real time.
3. Based on which fingers are raised, the system switches between different modes.
4. **AutoPy** translates the detected gesture into an actual mouse action on the computer.

## Gestures Supported

| Gesture | Action |
|---------|--------|
| ☝️ Index finger up only | **Move** the mouse cursor |
| ✌️ Index + middle finger up (fingers close together) | **Left click** |
| ✌️ Index + middle finger up (different finger distance) | **Right click** |
| ✌️ Index + middle finger up (specific distance) | **Open a drive/folder** |

## Key Features

- Real-time hand landmark detection using MediaPipe.
- Coordinate mapping and smoothening applied to cursor movement to reduce jitter and provide a stable experience.
- Achieves stable performance at **20+ FPS** on a standard laptop — no GPU required.
- Manually tested under different lighting conditions and hand positions to verify gesture accuracy and reliability.

## Project Structure

```
AI-Virtual-Mouse-using-Hand-Gesture-Recognition/
├── HandTrackingModule.py     # Reusable hand detection class (landmarks, finger state, distance)
└── aivirtualmouseproject.py  # Main script - captures webcam feed and maps gestures to mouse actions
```

## How to Run

### Prerequisites
- Python 3.8+
- Webcam

### Installation

```bash
pip install opencv-python mediapipe numpy autopy
```

> **Note:** `autopy` may require additional build tools on some systems. On Windows, installing via a prebuilt wheel is recommended if `pip install autopy` fails.

### Run the project

```bash
python aivirtualmouseproject.py
```

Press **Esc** to exit the application.

## Author

**Manas Kumar Nayak**
[LinkedIn](https://linkedin.com) | [GitHub](https://github.com/ManasKumarNayak)
