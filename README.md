# **Traffic Detection using YOLOv8**

## **1. Project Overview**
This project focuses on **real-time vehicle detection** in traffic videos using **YOLOv8 (You Only Look Once)**, a deep-learning-based object detection model. The goal is to detect and count vehicles in a traffic video feed.

---

## **2. Setup & Model Loading**
- The script is implemented in **Python** using:
  - **Ultralytics YOLOv8** for object detection.
  - **OpenCV (cv2)** for video processing.
  - **Torch (PyTorch)** for deep learning computations.
  
- **Device Selection**:  
  - The model runs on **GPU (CUDA)** if available; otherwise, it defaults to **CPU**.

- **Model Used**:
  - `yolov8n.pt` (YOLOv8 Nano) – A lightweight version of YOLO for fast inference.

---

## **3. Video Processing Pipeline**
### **A. Reading the Traffic Video**
- The video file (`traffic.mp4`) is loaded using **OpenCV (`cv2.VideoCapture`)**.
- The frame dimensions are set to **640x480 pixels** for optimal processing.

### **B. Real-Time Object Detection**
- Each video frame is processed using the **YOLOv8 model**.
- The model returns **bounding boxes** around detected objects (vehicles).
- Vehicle count is determined based on the number of detected bounding boxes.

### **C. Visualization**
- **Bounding boxes** are drawn around detected vehicles.
- The total **vehicle count** is displayed on the frame.
- The processed frames are shown in a live window.

---

## **4. User Interaction**
- Press **'Q'** to exit the detection window and stop the program.

---

## **5. Insights & Applications**
- **Traffic Monitoring**: Real-time vehicle tracking in busy intersections.
- **Smart City Solutions**: Automated traffic management systems.
- **Surveillance**: Enhancing security and road safety.

---

## **6. Next Steps**
- Improve accuracy using **YOLOv8-m (Medium) or YOLOv8-l (Large)** models.
- Integrate with **license plate recognition** for further insights.
- Deploy as a **Flask or FastAPI service** for live video streaming.

---
