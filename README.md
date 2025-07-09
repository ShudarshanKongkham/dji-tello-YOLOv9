# GestureFly 🚁

**Intelligent Gesture-Controlled Drone System with Face Recognition**

A real-time gesture recognition system for controlling DJI Tello drones using YOLOv9-based computer vision, MediaPipe face tracking, and face recognition authentication.

<div align="center">
    <a href="./">
        <img src="./figure/performance.png" width="79%"/>
    </a>
</div>

## 🌟 Features

- **🤖 Real-time gesture recognition** using trained YOLOv9 models
- **👤 Face recognition authentication** for secure drone access
- **📱 MediaPipe integration** for face tracking and rotation control
- **🎮 PyGame-based GUI** with interactive controls
- **💡 LED matrix support** for visual feedback (RoboMaster version)
- **📸 Automatic photo capture** with countdown timer
- **🔋 Battery monitoring** and safety features
- **🎯 Head-based drone rotation** control

## 🚀 Available Implementations

### Basic Drone Control with Face Recognition
**[`tello_mediapipe_modified.py`](tello_mediapipe_modified.py)**

Streamlined implementation for essential drone control:
- ✅ Gesture-based flight commands (up, down, left, right, forward, backward)
- ✅ Face recognition authentication
- ✅ Head movement for drone rotation control
- ✅ PyGame GUI with clickable buttons
- ✅ Automatic takeoff/landing gestures

### RoboMaster Edition with LED Support
**[`RoboMaster_windowsLED.py`](RoboMaster_windowsLED.py)**

Enhanced version with advanced visual feedback:
- ✅ All basic drone control features
- ✅ **LED matrix integration** for visual status indicators
- ✅ **Countdown display on LED matrix** for photo capture
- ✅ **Color-coded authentication feedback** (green for authenticated, red for unauthorized)
- ✅ **Command visualization** on LED matrix
- ✅ Enhanced visual feedback system

## 🤚 Supported Gestures

| Gesture | Action | Description |
|---------|--------|-------------|
| **👆 Up** | Move Up | Drone ascends vertically |
| **👇 Down** | Move Down | Drone descends vertically |
| **👈 Left** | Move Left | Drone moves left |
| **👉 Right** | Move Right | Drone moves right |
| **👋 Forward** | Move Forward | Drone moves forward |
| **🤚 Backward** | Move Backward | Drone moves backward |
| **📷 Picture** | Take Photo | Initiates 4-second countdown and captures photo |
| **🛬 Land** | Land | Emergency landing command |

## 👤 Face-based Controls

- **🔐 Face Recognition**: Only authenticated users can control the drone
- **🔄 Head Rotation**: Turn your head left/right to rotate the drone clockwise/counter-clockwise
- **⏰ Automatic Authentication**: Face recognition runs every 10 seconds for continuous security

## 🛠️ Installation & Setup

### 1. Install Dependencies
```bash
pip install djitellopy opencv-python pygame mediapipe torch torchvision
```

### 2. Prepare Face Recognition
- Ensure `core_embeddings.pkl` contains your face embeddings
- Update face database as needed for authorized users

### 3. Connect DJI Tello
- Power on your DJI Tello drone
- Connect to Tello's WiFi network

### 4. Run the Application
```bash
# Basic version
python tello_mediapipe_modified.py

# RoboMaster version with LED support
python RoboMaster_windowsLED.py
```

## 🎮 Controls

### ⌨️ Keyboard Controls
- `W/A/S/D`: Manual movement (up/left/down/right)
- `T`: Takeoff
- `L`: Land
- `P`: Take picture
- `F/B`: Forward/Backward movement
- `Q`: Quit application

### 🖱️ Mouse Controls
- Click on GUI buttons for corresponding actions
- Interactive button feedback with hover effects

## 📋 Requirements

### Hardware
- **DJI Tello drone**
- **Webcam** (for face recognition)
- **Computer** with sufficient processing power

### Software
- **Python 3.7+**
- **CUDA-capable GPU** (recommended for better performance)
- **Pre-trained YOLOv9 model** (`v9_c_best.pt`)
- **UI Assets** in `./assets/` directory

## 🛡️ Safety Features

- **🔒 Authentication required**: Only recognized users can control the drone
- **🔋 Battery monitoring**: Real-time battery level display
- **📱 Visual feedback**: Command status and user authentication status
- **🚨 Emergency controls**: Manual override via keyboard/mouse
- **⏱️ Timeout protection**: Automatic safety measures

## 🏗️ Project Structure

```
GestureFly/
├── RoboMaster_windowsLED.py          # Enhanced version with LED support
├── tello_mediapipe_modified.py       # Basic gesture control
├── FaceRecognitionC.py               # Face recognition module
├── core_embeddings.pkl               # Face recognition database
├── v9_c_best.pt                      # Trained YOLOv9 model
├── assets/                           # UI images and icons
├── models/                           # YOLOv9 model configurations
├── utils/                            # Utility functions
└── README.md                         # This file
```

## 🎯 Getting Started

1. **Clone the repository**
2. **Install dependencies** as listed above
3. **Prepare your face recognition database**
4. **Connect to your DJI Tello drone**
5. **Run the desired implementation**
6. **Follow on-screen instructions for gesture control**

## 🤝 Contributing

We welcome contributions! Please feel free to submit issues, feature requests, or pull requests.

## 📄 License

This project is licensed under the terms specified in [LICENSE.md](LICENSE.md).

## 🙏 Acknowledgments

Built upon the excellent work of:
- YOLOv9 object detection framework
- DJITelloPy drone control library
- MediaPipe face detection
- OpenCV computer vision library

---

**🚨 Safety Notice**: Always operate drones in safe environments and follow local regulations. This system is for educational and research purposes.
