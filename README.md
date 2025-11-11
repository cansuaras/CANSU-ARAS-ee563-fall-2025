# EE563 – Midterm Project

This project includes two computer vision tasks implemented in **Python (Google Colab)** using **MediaPipe**.

---

## Q1 – Pose Detection (Arm Up Classification)

The **Pose Landmarker** model from MediaPipe is used to detect human body landmarks in static images.

The algorithm compares the relative positions of the wrist, elbow, and shoulder to determine which arm is raised.

**Logic:**
- If the wrist and elbow are positioned higher (smaller `y` value) than the shoulder, that arm is considered **up**.
- If both arms satisfy the condition, the output is `"both"`.
- Otherwise, `"left"`, `"right"`, or `"None"`.

**Output:**  
`left`, `right`, `both`, or `None`

---

## Q2 – Face Direction Detection

The **Face Detector** model is used to find faces in each image.

For every detected face, the direction of the face is estimated based on the **nose tip position** relative to the bounding box center.

**Logic:**
- If the nose tip is shifted to the right → `"right"`
- If the nose tip is shifted to the left → `"left"`
- If the offset is small → `"straight"`

**Output:**  
`left`, `right`, or `straight`

---

## ⚙️ Environment and Dependencies
- Python (Google Colab)
- Libraries:
  - `mediapipe`
  - `opencv-python`
  - `numpy`

---

##  How to Run

1. Open the notebook in **Google Colab**.  
2. Upload the test images using:
   ```python
   from google.colab import files
   uploaded = files.upload()
