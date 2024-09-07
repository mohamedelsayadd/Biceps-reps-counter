# Biceps Reps Counter using Computer Vision

This project is a **Biceps Reps Counter** built using **OpenCV**, **Mediapipe**, and **NumPy**. It uses pose detection to monitor body movements during biceps exercises and counts the number of repetitions performed by the user.

## Features
- Detect body pose using Mediapipe
- Track the right shoulder, elbow, and wrist for biceps exercises
- Calculate the angle between joints to detect the exercise stage (Up/Down)
- Automatically count and display the number of repetitions performed
- Display landmarks and connections of the body on the video in real-time

## Installation

1. Clone the repository to your local machine:
    ```bash
    git clone https://github.com/yourusername/biceps-reps-counter.git
    ```

2. Install the required dependencies:
    ```bash
    pip install opencv-python mediapipe numpy
    ```

3. Make sure you have a video file named `me_gym.mp4` to test the program, or modify the file path in the code to your own video.

## How It Works

The program processes a video of a person performing biceps exercises. It uses Mediapipe's Pose module to detect key landmarks on the body. The angle between the right shoulder, elbow, and wrist is calculated to determine the movement stage (Up/Down). When a full repetition (from Down to Up) is detected, the rep counter is incremented. The processed video displays:
- Body landmarks and connections
- The current number of reps
- The current exercise stage (Up/Down)
- The calculated angle of the arm

## Running the Code

1. Ensure your video file is loaded properly:
    ```python
    cap = cv2.VideoCapture("me_gym.mp4")
    ```

2. Run the main Python script to process the video and track reps:
    ```bash
    python biceps_counter.py
    ```

3. The output video with the processed frames will be saved as `result.avi`.

## Key Functions
- **calculate_angle(a, b, c)**: This function calculates the angle between three points (shoulder, elbow, wrist) using trigonometry.
- **Mediapipe Pose Detection**: Detects the body pose and extracts landmarks for pose estimation.
- **OpenCV Video Processing**: Handles reading from the video, displaying frames, and writing the output video with the overlays.

## Future Improvements
- Add support for multiple exercises
- Use real-time camera feed instead of pre-recorded video
- Improve robustness of angle detection for various body positions

## Thank You

This project was developed using Google Colab for demonstration and quick prototyping. For more details, feel free to explore the code in the Jupyter notebook.
