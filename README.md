# 🤟 Urdu Sign Language (USL) Recognition System

A real-time Urdu Sign Language (USL) alphabet recognition system developed using multiple deep learning and machine learning approaches. The project compares CNN-based models, transfer learning techniques, and an Artificial Neural Network trained on MediaPipe hand landmarks to identify Urdu sign language alphabets from webcam input.

---

## 📌 Project Overview

Communication barriers remain a significant challenge for the deaf and hard-of-hearing community. This project aims to bridge that gap by recognizing Urdu Sign Language hand gestures in real time using computer vision and machine learning.

Before any classification takes place, **MediaPipe Hands** is used to detect the hand and extract the region of interest, allowing the models to focus on the gesture while reducing the impact of varying backgrounds and lighting conditions.

The project evaluates multiple models and compares their performance to determine the most effective approach for USL alphabet recognition.

---

## 📊 Dataset

A custom Urdu Sign Language dataset was collected specifically for this project.

### Dataset Highlights

| Property | Value |
|----------|-------|
| Language | Urdu Sign Language |
| Classes | Urdu Alphabet Signs |
| Source | Custom Dataset |
| Preprocessing | MediaPipe Hand Detection & Cropping |
| Image Sizes | 128×128 and 224×224 |

Dataset preprocessing included:

- Hand detection using MediaPipe
- Automatic hand cropping
- Image resizing
- Dataset splitting into Train, Validation, and Test sets
- Data augmentation for improved generalization

---

## 🧠 Models Implemented

### 1. Custom CNN

A Convolutional Neural Network trained from scratch on the processed USL dataset.

Features include:

- Multiple convolutional layers
- Batch Normalization
- Max Pooling
- Dropout regularization
- Softmax output layer

---

### 2. Transfer Learning Models

Several pretrained CNN architectures were evaluated and fine-tuned for Urdu Sign Language recognition, including:

- EfficientNetB0
- EfficientNetB3
- ResNet50
- MobileNetV2

Transfer learning was performed using ImageNet-pretrained weights followed by selective fine-tuning of deeper layers.

---

### 3. Artificial Neural Network (ANN)

Instead of raw images, this approach uses **MediaPipe** to extract 21 hand landmarks.

Each hand is represented by:

- 21 landmarks
- (x, y, z) coordinates
- 63-dimensional feature vector

These landmark features are then used to train a fully connected Artificial Neural Network for lightweight and efficient classification.

---

## ⚙️ Technologies Used

- Python
- TensorFlow / Keras
- OpenCV
- MediaPipe
- NumPy
- Pandas
- Matplotlib
- Scikit-learn

---

## 📈 Model Evaluation

The notebook includes comprehensive evaluation using:

- Training & Validation Accuracy
- Loss Curves
- Confusion Matrix
- Precision
- Recall
- F1-Score
- Classification Report
- Confidence Analysis
- Model Comparison

The best-performing model was selected based on both classification performance and real-world inference capability.

---

## 🎯 Features

- Real-time webcam prediction
- Automatic hand detection
- Hand cropping using MediaPipe
- Multiple deep learning architectures
- ANN using hand landmarks
- Performance comparison across models
- Detailed visualization and analysis

---

## 📂 Project Workflow

1. Dataset Collection
2. Image Preprocessing
3. MediaPipe Hand Detection
4. Dataset Preparation
5. Model Training
6. Model Evaluation
7. Model Comparison
8. Real-Time Prediction

---

## 👥 Team Members

- Umaima Khan
- Assamir Zafar
- Fasih Ahmed Khan
- Umar Saleem

**Course:** CS-324 Machine Learning

**Instructor:** Dr. Maria Waqas

---

## 📄 License

This project is intended for educational and research purposes.
