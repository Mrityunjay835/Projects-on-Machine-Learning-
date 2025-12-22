# AI-Powered Medical Image Analysis: Pneumonia Detection 🏥

## Overview
This project is an end-to-end deep learning system designed to assist radiologists in detecting pneumonia from chest X-ray images. Utilizing a ResNet50 backbone and transfer learning, the model emphasizes high sensitivity so potential anomalies are flagged for professional review with minimal latency.

## Key Highlights
- Target Accuracy: 94.2%
- Inference Speed: < 0.3 s per image
- Explainability: Integrated Grad-CAM heatmaps to visualize regions of interest for clinical trust
- Production Ready: Containerized with Docker and prepared for AWS deployment

## 🛠️ Tech Stack
- Deep Learning: TensorFlow, Keras  
- Computer Vision: OpenCV (CLAHE preprocessing), Pillow  
- Backend API: Flask / FastAPI  
- DevOps: Docker, AWS (S3 / ECR)  
- Data Analysis: Pandas, NumPy, Matplotlib

## 📊 Dataset
- Dataset: Chest X-Ray Images (Pneumonia) by Paul Mooney  
- Total Images: 5,856  
- Categories: Normal, Bacterial Pneumonia, Viral Pneumonia  
- Split Strategy: 70% train, 20% validation, 10% test

## 🧬 Project Architecture
- Preprocessing: 16-bit to 8-bit conversion, CLAHE (Contrast Limited Adaptive Histogram Equalization) to enhance lung opacities, and normalization to [0, 1].  
- Model Backbone: ResNet50 (pre-trained on ImageNet)  
- Custom Head: Global Average Pooling -> Dense(256, ReLU) -> Dropout(0.5) -> Dense(1, Sigmoid)  
- Inference: Flask-based REST API accepting image uploads and returning JSON predictions

## 📈 Evaluation Metrics
Because this is a clinical application, recall (sensitivity) is prioritized to reduce false negatives:
- Accuracy: 94.2%  
- Recall (Sensitivity): 96.1%  
- Precision: 91.5%  
- F1-Score: 93.7%

## 🖼️ Explainable AI (XAI)
The system generates Grad-CAM heatmaps highlighting lung regions that influenced predictions, helping clinicians review model decisions.

## 🚀 Getting Started

1. Clone the repository