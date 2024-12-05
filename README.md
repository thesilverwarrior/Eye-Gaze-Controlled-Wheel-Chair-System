# Eye-Gaze-Controlled-Wheel-Chair-System

The **Eye-Gaze Controlled Wheelchair** is an assistive technology designed for individuals with mobility impairments. It allows users to control a wheelchair using eye movements and blinks, providing a hands-free navigation solution. By leveraging computer vision and gaze tracking, this system detects eye gaze direction and blinking patterns to determine wheelchair movement, making it an intuitive and accessible solution for people with disabilities.

---

## Features
- **Gaze-Based Control**: Determines movement directions (FORWARD, LEFT, RIGHT, STOP) based on the user's gaze ratio.
- **Blink Detection**: Uses blinking patterns to send specific commands, including stopping or reversing the wheelchair.
- **Real-Time Processing**: Implements efficient eye-tracking using OpenCV and Dlib for real-time responsiveness.
- **Arduino Integration**: Sends movement commands to the wheelchair via serial communication with an Arduino microcontroller.
- **Safety Mechanisms**: Automatically stops the wheelchair when no valid direction is detected.

---

## Technology Stack
- **Programming Language**: Python
- **Libraries**:
  - `OpenCV`: For image processing and real-time frame capture.
  - `Dlib`: For facial landmark detection and gaze analysis.
  - `NumPy`: For numerical operations on eye region coordinates.
  - `Serial`: For Arduino communication.
- **Hardware**:
  - Webcam for eye tracking.
  - Arduino microcontroller for controlling wheelchair motors.
  - Eye-tracking sensors (using webcam as a basic sensor).

---

## How It Works
1. **Face Detection**: The program uses Dlib's pre-trained facial landmark detector to identify key points on the face, focusing on the eyes.
2. **Blinking Detection**:
   - Calculates the blinking ratio by analyzing the vertical and horizontal dimensions of the eyes.
   - Determines whether one or both eyes are blinking to trigger specific commands.
3. **Gaze Ratio Analysis**:
   - Analyzes the left and right eye gaze ratio to estimate the direction of the user's gaze.
   - Determines the movement direction based on thresholds for gaze ratio (e.g., LEFT, RIGHT, or FORWARD).
4. **Command Transmission**:
   - Sends the movement command to the Arduino via serial communication, which then drives the wheelchair motors accordingly.
5. **Real-Time Feedback**:
   - Displays the detected direction on the screen for visual feedback.
   - Highlights the user's eyes with bounding boxes to indicate detection accuracy.

---

## Installation and Usage

### Prerequisites
- Python 3.7 installed on your system.
- Required Python libraries: `opencv-python`, `dlib`, `numpy`, and `pyserial`.
- Pre-trained facial landmark model (`shape_predictor_68_face_landmarks.dat`).

### Steps
1. Clone the repository and navigate to the project directory.
   ```bash
   git clone https://github.com/thesilverwarrior/Eye-Gaze-Controlled-Wheel-Chair-System.git
   cd Eye-Gaze-Controlled-Wheel-Chair-System








