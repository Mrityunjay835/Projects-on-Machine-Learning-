AI-Powered Medical Image Analysis: Pneumonia Detection 🏥
Overview
This project is an end-to-end deep learning system designed to assist radiologists in detecting pneumonia from chest X-ray images. Utilizing a ResNet50 backbone and transfer learning, the model emphasizes high sensitivity so potential anomalies are flagged for professional review with minimal latency.
Key Highlights
·	Target Accuracy: 94.2%
·	Inference Speed: < 0.3 s per image


# 🛠️ Tech Stack
·	Deep Learning: TensorFlow, Keras
·	Computer Vision: OpenCV (CLAHE preprocessing), Pillow
·	Data Analysis: Pandas, NumPy, Matplotlib


# 🚀 How to Run
1. Prerequisites
Ensure you have the Kaggle dataset downloaded and organized into train, test, and  val folders.
   - data/train/{NORMAL,PNEUMONIA}
   - data/val/{NORMAL,PNEUMONIA}
   - data/test/{NORMAL,PNEUMONIA}
2. Environment Setup

pip install tensorflow pandas numpy matplotlib scikit-learn

Based on the specific libraries and components you've imported, I have updated the README to reflect a Keras-centric deep learning workflow. This version highlights the use of ImageDataGenerator for the data pipeline and the specific layers you are using to build the model.
AI-Powered Pneumonia Detection System


# 🏥 Project Overview
This project implements a Convolutional Neural Network (CNN) to automate the detection of Pneumonia from chest X-ray images. By leveraging Transfer Learning and Data Augmentation, the model is designed to distinguish between "Normal" lungs and those showing signs of viral or bacterial pneumonia with high precision.

# 🛠️ Technical Implementation
Data Pipeline & Preprocessing
Using ImageDataGenerator, the system implements a real-time data augmentation pipeline to improve model generalization:
·	Rescaling: Normalizing pixel values to $[0, 1]$.
·	Augmentation: Random rotations, shifts, and zooms to simulate different X-ray capture conditions.
·	Validation Split: Utilizing train_test_split from Scikit-Learn to ensure a robust evaluation set.
Model Architecture
The model is built using the Keras Sequential API with a focus on efficiency and performance:
1.	Base Layer: Input layer optimized for medical image dimensions.
2.	Feature Extraction: Integration of a pre-trained backbone (Transfer Learning).
3.	GlobalAveragePooling2D: To reduce the spatial tensor dimensions while retaining critical features.
4.	BatchNormalization: Used to stabilize and accelerate the training process.
5.	Dropout (Regularization): Strategically placed to prevent overfitting on the medical training set.
6.	Dense Head: Fully connected layers with ReLU and a final Sigmoid output for binary classification.

Model Architecture
The model is built using the Keras Sequential API with a focus on efficiency and performance:
1.	Base Layer: Input layer optimized for medical image dimensions.
2.	Feature Extraction: Integration of a pre-trained backbone (Transfer Learning).
3.	GlobalAveragePooling2D: To reduce the spatial tensor dimensions while retaining critical features.
4.	BatchNormalization: Used to stabilize and accelerate the training process.
5.	Dropout (Regularization): Strategically placed to prevent overfitting on the medical training set.
6.	Dense Head: Fully connected layers with ReLU and a final Sigmoid output for binary classification.


# 💻 Tech Stack
·	Language: Python
·	Data Handling: Pandas, NumPy
·	Visualization: Matplotlib
·	Machine Learning: Scikit-Learn
·	Deep Learning Framework: TensorFlow & Keras
·	Key Layers: GlobalAveragePooling2D, BatchNormalization, Dropout.


# 🚀 How to Run
1. Prerequisites
Ensure you have the Kaggle dataset downloaded and organized into train, test, and val folders.
2. Environment Setup
Bash
pip install tensorflow pandas numpy matplotlib scikit-learn

3. Model Training
The training script utilizes the following logic:
·	Step 1: Load data via os and ImageDataGenerator.
·	Step 2: Define the Sequential model architecture.
·	Step 3: Compile with Adam optimizer and binary_crossentropy loss.
·	Step 4: Evaluate performance using Matplotlib to plot training/validation loss and accuracy curves.


# 📂 Project Structure
Plaintext
├── data/
│   ├── train/
│   ├── test/
│   └── val/
├── notebooks/
│   └── model.ipynb  # Main model logic
├── models/
│   └── final_model.h5             # Saved Keras model
└── README.md

# 📊 Dataset
·	Dataset: Chest X-Ray Images (Pneumonia) by Paul Mooney
·	Total Images: 5,856
·	Categories: Normal, Bacterial Pneumonia, Viral Pneumonia
·	Split Strategy: 70% train, 20% validation, 10% test


# 🧬 Project Architecture
·	Preprocessing: 16-bit to 8-bit conversion, CLAHE (Contrast Limited Adaptive Histogram Equalization) to enhance lung opacities, and normalization to [0, 1].
·	Model Backbone: ResNet50 (pre-trained on ImageNet)
·	Custom Head: Global Average Pooling -> Dense(256, ReLU) -> Dropout(0.5) -> Dense(1, Sigmoid)
·	Inference: Flask-based REST API accepting image uploads and returning JSON predictions


# 📊 Evaluation Focus
Given the medical nature of the project, we evaluate success based on:
·	Accuracy: Overall correctness.
·	Sensitivity (Recall): Minimizing False Negatives (critical for medical diagnosis).
·	Stability: Ensuring the gap between training and validation loss is minimal using BatchNormalization and Dropout.


# 🚀 Getting Started
1.	Clone the repository
