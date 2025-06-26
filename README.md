# 🕳️ Road Pothole Detection and Segmentation using YOLOv8
This repository contains a complete pipeline for detecting and segmenting road potholes using deep learning, built as part of the Machine Vision coursework for the B.Sc. (Hons) in Artificial Intelligence and Data Science at Robert Gordon University.

## 🚀 Overview
Potholes pose significant safety hazards and financial burdens due to vehicle damage and accidents. This project presents a real-time, automated solution using the YOLOv8n-seg model to accurately detect and segment potholes in both road images and video streams.

### Key Features:

🔍 Instance Segmentation of potholes using YOLOv8n-seg
📸 Real-time damage severity classification (Minor / Moderate / Severe)
🧪 Evaluated on 1,000+ test images with high mAP and F1 scores
📊 Full training pipeline with visualization of evaluation metrics

### 📁 Dataset
1. Combined from:
    - Kaggle Dataset (780 images) - https://www.kaggle.com/datasets/farzadnekouei/pothole-image-segmentation-dataset 
    - Roboflow Dataset (4,376 images) - https://universe.roboflow.com/thien-bk-1dkcf/pothole-detection-system-rnoh4/dataset/2

2. YOLOv8 format with segmentation masks
3. Preprocessing includes:
    - Resizing to 640×640
    - Augmentation: flips, cropping, rotation, brightness/exposure, etc.

### 🧠 Model Architecture
- Model: YOLOv8n-seg (Nano variant of YOLOv8 segmentation)
- Layers: 151
- Parameters: ~3.4M
- Chosen for its speed-accuracy tradeoff in real-time embedded systems

### ⚙️ Training Configuration
- Epochs: 150 (Early stopping: 15)
- Optimizer: AdamW
- Learning Rate: 0.0001 (multiplier 0.01)
- Dropout: 0.25
- Batch size: 16

- Hardware: Google Colab (GPU)

### 🎥 Real-Time Assessment
- Image-based: Computes percentage of damage area and classifies severity
- Video-based: Applies YOLOv8 frame-by-frame with damage smoothing across frames

### 🔧 Requirements
- Python 3.8+
- Ultralytics YOLOv8
- OpenCV
- NumPy, Matplotlib

### 📌 Limitations & Future Work
- Limited negative/background-only samples can cause false positives
- Google Colab resource constraints limited training flexibility

Future improvements:
1. Add diverse datasets with background images
2. Use dedicated GPU/cloud platforms
3. Deploy on edge devices for on-road testing

### ✍️ Author
Kavindya Koralegei
Informatics Institute of Technology (IIT), Colombo
Robert Gordon University – BSc (Hons) in AI & Data Science
