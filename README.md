Exercise Recognition Pipeline
📌 Objective
This project aims to develop an Exercise Recognition Pipeline that integrates object detection, 3D pose estimation, and exercise classification using deep learning techniques. The pipeline detects a person using YOLO, estimates 3D body landmarks using a pretrained model (MediaPipe), and classifies the exercise using a custom CNN based on the extracted 3D landmarks.

🗃️ Dataset
Description:
The dataset includes annotated 3D body landmark positions corresponding to various exercise types.

Exercises Covered (5 total):

Push-up (push-up_up, push-up_down)

Pull-up (pull-up_up, pull-up_down)

Sit-up (sit-up_up, sit-up_down)

Jumping Jack (jack_open, jack_close)

Squat (squat_up, squat_down)

Annotations:

3D coordinates (x, y, z) of key body points for each exercise frame.

Each exercise is represented by two terminal pose classes (e.g., "up" and "down").

🔄 Pipeline Overview
1. 📷 Image Acquisition
Task: Capture an image or extract a frame showing a person performing an exercise.

Requirement: The person must be clearly visible for accurate pose estimation.

2. 🧍‍♂️ Person Detection with YOLO
Task: Detect and localize the person using a pretrained YOLO model.

Output: Bounding box around the person in the image.

3. 🧠 3D Pose Estimation with MediaPipe
Task: Crop the image using YOLO's bounding box and estimate 3D body landmarks using MediaPipe (33 landmarks).

Output: 3D landmark coordinates (x, y, z) for key body points.

Visualization: Overlay landmarks on the original image to illustrate the pose.

4. 🏋️ Exercise Classification Using Custom CNN
Task: Build and train a custom Convolutional Neural Network (CNN) that classifies exercises based on the 3D landmark data.

Input: 3D coordinates of 33 body landmarks.

Model Architecture: Custom CNN tailored for 3D spatial features.

Training: Train using the labeled dataset and ensure generalization.

Evaluation Metrics:

Accuracy

Precision

Recall

F1-Score

5. 🖼️ Mapping and Visualization
Task: Overlay predicted exercise label and 3D landmarks onto the original image.

Goal: Provide an intuitive visual output showing both detection and classification results.

🚀 Getting Started
Requirements
Python 3.8+

OpenCV

PyTorch / TensorFlow

MediaPipe

YOLOv5 (or equivalent)

Matplotlib / Seaborn (for visualization)
