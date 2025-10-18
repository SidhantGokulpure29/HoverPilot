🌟 Overview

HoverPilot is an AI-powered hand-tracking virtual mouse built with Python, OpenCV, MediaPipe, and PyAutoGUI.
It uses your webcam to detect hand landmarks in real-time and lets you control your cursor with intuitive gestures.

Features:

✅ Move your cursor by moving your index finger

✅ Click by bringing your index and middle fingers together

✅ Completely hands-free control

🧰 Tech Stack
Component	Description
🧠 MediaPipe	Real-time hand tracking & landmark detection
👁️ OpenCV	Webcam feed processing & visualization
🖱️ PyAutoGUI	System-level cursor movement & clicks
🐍 Python	Glue code connecting everything

Python 3.8+ installed

Install dependencies
pip install opencv-python mediapipe pyautogui

Run HoverPilot
python hoverpilot.py


Now, wave your hand in front of your webcam — your cursor is under AI control! 🪄

✋ Controls & Gestures
Gesture	Action
👉 Move index finger	Move the cursor
✌️ Bring index & middle fingers close	Click
🖐️ Open hand	Idle / neutral state

💡 Tip: Keep your hand visible and well-lit for best tracking accuracy.

📸 Example Output


Real-time hand landmarks detection


Gesture-based click recognition

💡 How It Works

Capture webcam frames using OpenCV

Detect hand landmarks using MediaPipe

Map landmark positions to screen coordinates

Trigger system actions via PyAutoGUI (move, click, etc.)

A simple yet powerful demonstration of AI-driven human-computer interaction.

🚀 Future Improvements
✨ Add scroll & drag gestures
🎯 Smooth cursor movement filters
🤖 Multimodal control (voice + hand gestures)
💻 Build a GUI toggle application




If you want, I can also create a version with sleek GitHub badges, live demo GIF placeholders, and a clickable "Run Locally" button so it looks ultra-professional and ready to impress recruiters.

Do you want me to do that next?
