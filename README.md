# Biceps Reps Counter using Computer Vision

This project is a Python-based **Biceps Reps Counter** that utilizes **OpenCV**, **Mediapipe**, and **NumPy**. It tracks body movements during biceps exercises by detecting key landmarks on the body, calculating arm angles, and counting the repetitions automatically.

## Table of Contents

1. [Introduction](#introduction)
2. [Environment Setup](#environment-setup)
3. [How It Works](#how-it-works)
4. [Running the Code](#running-the-code)
5. [Future Improvements](#future-improvements)
6. [Video Demo](#video-demo)

## Introduction

The **Biceps Reps Counter** processes a video of a person performing biceps exercises. It uses **Mediapipe** to detect body landmarks, and tracks the shoulder, elbow, and wrist to calculate arm angles. The system determines whether the user is in the "Up" or "Down" stage of the exercise and counts repetitions based on the angle movement.

## Environment Setup

To run this project, you need to have Python installed. Follow these steps:

1. Clone the repository:
    ```bash
    git clone https://github.com/mohamedelsayadd/biceps-reps-counter.git
    ```
2. Install the required dependencies:
    ```bash
    pip install opencv-python mediapipe numpy
    ```
3. Place your workout video (`me_gym.mp4`) in the project folder or modify the video path in the code.

## How It Works

- **Pose Detection**: Uses Mediapipe's Pose module to detect key landmarks on the body.
- **Angle Calculation**: Tracks the shoulder, elbow, and wrist to calculate the angle of the arm.
- **Rep Counting**: The rep counter increments when the arm moves from the "Down" position (angle > 140°) to the "Up" position (angle < 75°).
- **Real-time Feedback**: Displays the current rep count, stage (Up/Down), and landmarks directly on the video.

## Running the Code

1. Open the terminal and run the Python script:
    ```bash
    python biceps_counter.py
    ```
2. The processed video will display landmarks, the current rep count, and the current exercise stage.
3. The output video will be saved as `result.avi`.

Make sure your input video is properly loaded by updating the file path if necessary.

## Future Improvements

- Support for multiple exercises beyond biceps curls.
- Use of real-time webcam feed for rep counting.
- Better handling of various body positions for more accurate angle detection.
- Add graphical interface for easier use.

## Video Demo

![Biceps Reps Counter](path_to_your_gif.gif)


