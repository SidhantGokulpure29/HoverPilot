<h1 align="center">🖐️ HoverPilot</h1>
<p align="center">
  <em>Control your computer with nothing but hand gestures. No mouse. No touch. Just magic.</em><br>
  <strong>Built with Python · OpenCV · MediaPipe · PyAutoGUI</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.9+-blue?style=flat-square">
  <img src="https://img.shields.io/badge/OpenCV-RealTime-green?style=flat-square">
  <img src="https://img.shields.io/badge/MediaPipe-HandTracking-orange?style=flat-square">
  <img src="https://img.shields.io/badge/Automation-PyAutoGUI-purple?style=flat-square">
</p>

---

## 🚀 What is HoverPilot?

HoverPilot is a gesture-powered virtual mouse that transforms your webcam into a motion-sensitive controller. By tracking your hand in real-time, it lets you:

- 🖱️ Move the cursor with your index finger
- 👆 Click by tapping your middle finger near the index
- 🎯 Interact with your screen like a Jedi

Perfect for accessibility, touchless interfaces, or just showing off your computer vision skills.

---

## 🎥 Live Demo (Coming Soon)

Imagine this:  
You raise your hand. Your cursor follows.  
You tap your fingers. A click registers.  
No hardware. No gimmicks. Just code.

---

## 🧠 How It Works

HoverPilot uses **MediaPipe’s 21-point hand landmark detection** to track your fingers and map their motion to screen coordinates.

### ✨ Gesture Logic

| Landmark | Role |
|----------|------|
| `ID 8`   | Index fingertip → cursor movement |
| `ID 12`  | Middle fingertip → click trigger |

### 🧪 Detection Flow

1. Capture webcam feed with OpenCV
2. Flip frame for mirror effect
3. Convert to RGB for MediaPipe
4. Detect hand landmarks
5. Map index finger to screen position
6. Detect click when index & middle fingers are close

---

## 🧾 Code Breakdown

```python
# Move cursor
if id == 8:
    index_x = screen_width / frame_width * x
    index_y = screen_height / frame_height * y
    pyautogui.moveTo(index_x, index_y)

# Detect click
if id == 12:
    if abs(index_y - thumb_y) < 30:
        pyautogui.click()
        pyautogui.sleep(1)
```
## 🛠️ Installation

### 📦 Requirements

Install the required Python packages:

```bash
pip install opencv-python mediapipe pyautogui
```
## 🧭 Controls

| Gesture                         | Action             |
|----------------------------------|--------------------|
| ✋ Raise hand                   | Activate tracking  |
| 👉 Point index finger            | Move cursor        |
| 🤌 Tap middle finger near index | Click              |
| ❌ Press `Q`                     | Quit the app       |

## 📸 Tech Stack

HoverPilot is powered by a trio of Python libraries that work together to deliver real-time gesture control:

### 🧰 Core Libraries

| 🧪 Tool        | 🔧 Purpose                   |
|---------------|------------------------------|
| **OpenCV**     | Captures webcam feed and renders visuals on screen |
| **MediaPipe**  | Detects and tracks 21 hand landmarks in real time |
| **PyAutoGUI**  | Translates finger gestures into mouse movements and clicks |

### 🧠 Why These Tools?

- **OpenCV** gives you full control over video frames and image processing.
- **MediaPipe** is optimized for fast, accurate hand tracking — no training required.
- **PyAutoGUI** lets you automate mouse actions across any OS, making gesture control seamless.

### 🚀 Integration Flow

1. OpenCV captures and flips the webcam feed.
2. MediaPipe detects hand landmarks and identifies finger positions.
3. PyAutoGUI maps those positions to screen coordinates and performs mouse actions.

Together, they form a lightweight, cross-platform gesture interface — no external hardware needed.

---
