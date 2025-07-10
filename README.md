# 🕳️ Pothole Detection and Mitigation System using YOLOv10n

This project presents an efficient and lightweight deep learning pipeline for real-time **pothole detection** and potential **road mitigation planning**. It leverages the **YOLOv10n model** for object detection, trained on a custom-annotated dataset, with end-to-end code implementation in **Google Colab**.

---

## 📖 Overview

The goal of this project is to create a lightweight and scalable system to detect potholes on roads using deep learning. We implemented this system using the **YOLOv10n (nano version)** model to ensure deployment feasibility even on edge or mobile devices.

---

## 📂 Dataset

- The dataset used was sourced from open road scene images with varying pothole types.
- Since the dataset was unannotated, **manual annotations were performed** using **[Roboflow](https://roboflow.com/)**.
- The final dataset included annotations in **YOLO format** suitable for training with YOLOv10.

---

## 🖊️ Annotation Process

- Annotation was done manually for accurate bounding boxes around potholes.
- We used Roboflow to:
  - Upload and manage images.
  - Annotate bounding boxes.
  - Export in YOLOv5/YOLOv10 compatible format.
  - Split data into training, validation, and test sets.

---

## 🧠 Model Architecture

- **Model**: YOLOv10n (nano version)
- **Framework**: Ultralytics-style YOLOv10 (compatible with PyTorch backend)
- **Training Environment**: Google Colab
- **Input Resolution**: 640x640
- **Anchor-free detection** for lightweight and faster inference

---

## 🏋️ Training and Testing

- Model was trained using:
  - ✅ Custom annotated dataset
  - ✅ Google Colab with GPU backend
- Loss convergence and mAP (mean Average Precision) were monitored.
- Inference results were visualized on test images with bounding boxes over potholes.

---

## 📊 Results

- The model achieved high precision and recall on test data.
- Real-time detection was possible with minimal latency, making it viable for real-world use in road surveillance and municipal planning.

---

## ⚙️ Installation

Clone the repo:

```bash
git clone https://github.com/<your-username>/pothole-detection-and-mitigation.git
cd pothole-detection-and-mitigation
```

Install required libraries:

```bash
pip install -r requirements.txt
```

---

## ▶️ Usage

Run training:

```bash
python src/train.py
```

Run inference:

```bash
python src/detect.py
```

---

## 🗂️ Project Structure

```
├── data/                   # Annotated dataset (from Roboflow)
├── models/                 # YOLOv10n weights
├── notebooks/              # Google Colab notebook
├── src/                    # Scripts for training, detection
│   ├── train.py
│   ├── detect.py
│   └── utils.py
├── results/                # Inference outputs, graphs
├── requirements.txt
├── README.md
└── .gitignore
```

---

## 🔭 Future Work

- Integrate pothole severity estimation using bounding box size and depth estimation.
- GPS tagging of potholes for location mapping.
- Mobile app deployment using TensorFlow Lite or ONNX.
- Real-time deployment on road surveillance drones.
- Integrate LiDAR for accurate measurement of pothole dimensions (depth, width, volume).

---

## 👥 Contributors

- Sarvesh Hampali  
- Team CIM  

---

## 📄 License

This project is licensed under the MIT License.
