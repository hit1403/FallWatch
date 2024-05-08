# Fall Detection Using YOLO Object Detection

## Overview
This project implements a fall detection system using the YOLO (You Only Look Once) object detection model. The system analyzes video streams to detect instances of people falling and triggers a "Fall Detected" message when a fall is detected.

## Features
- Video Input: The system takes input from a video file.
- Object Detection: YOLO model (yolov8s-pose.pt) is used to detect objects in the video frames, providing bounding box coordinates and confidence scores.
- Bounding Box Visualization: Bounding boxes are drawn around detected persons with confidence scores above a certain threshold (default: 40%), along with labels.
- Fall Detection Logic: Fall detection is implemented by analyzing the bounding box dimensions. If the difference between the height and width of the bounding box is negative, indicating a person is falling, a "Fall Detected" message is triggered.
- Output Video: Processed video frames with bounding boxes and fall detection messages are written to an output video file.

## Usage
1. Install dependencies:
   ```bash
   pip install opencv-python opencv-python-headless cvzone ultralytics
2. Run the Script: Run the script fall_detection.py, providing the path to the input video file:
   ```bash
   python fall_detection.py --input_video_path <input_video_path>
3. Monitor Output: Monitor the output video file generated for fall detection results.

## Code Analysis
- Initialization: The code initializes the YOLO model.
- Frame Processing: Iterates through each frame of the input video.
- Object Detection: YOLO model predicts objects in each frame.
- Bounding Box Handling: Calculates bounding box dimensions and checks for fall conditions for each detected person.
- Visualization: Draws bounding boxes and labels on frames for detected persons.
- Fall Detection: Triggers a "Fall Detected" message if a fall condition is met.
- Output Video Writing: Writes processed frames to an output video file.
