# EE563 – Midterm Project

This project implements two computer vision tasks using MediaPipe in Python/Google Colab.
#Q1 – Pose Detection (Arm Up Classification)

A pose estimation model (Pose Landmarker) is used to detect body landmarks from input images.
The script classifies which arm is raised by comparing the relative positions of the wrist, elbow, and shoulder:

Output: "left", "right", "both", or "None".
If the wrist and elbow are higher (smaller y value) than the shoulder, that arm is considered “up”.
#Q2 – Face Direction Detection

A face detection model (Face Detector) is used to locate faces in images.
For each detected face, the algorithm estimates whether the person is looking left, right, or straight based on the nose tip position relative to the bounding box center:

Output: "left", "right", or "straight".
