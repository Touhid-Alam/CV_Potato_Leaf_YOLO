# README: Precise Potato Leaf Disease Detection with YOLO Models

## Overview
This repository contains the implementation of **You Only Look Once (YOLO)** models for detecting potato leaf diseases, including **early blight**, **late blight**, and **healthy leaves**. The study evaluates the performance of **YOLOv8**, **YOLOv9**, **YOLOv10**, and **YOLOv11** on a dataset of **2,152 images**. Among these, **YOLOv11** demonstrated the highest performance, achieving a **mAP50 of 99.5%**, **precision of 98.1%**, and **recall of 97.1%**. The results highlight the effectiveness of YOLOv11 in accurately detecting potato leaf diseases, contributing to improved agricultural productivity and sustainability.

---

## Key Features
- **High Accuracy**: YOLOv11 achieves **99.5% mAP50**, outperforming other YOLO models.
- **Efficient Detection**: YOLOv11 requires only **2.6 million trainable parameters**, making it computationally efficient.
- **Robust Generalization**: The model demonstrates excellent precision-recall tradeoff and F1-confidence curves.
- **Real-Time Detection**: Suitable for real-time applications in agricultural settings.
- **Comprehensive Evaluation**: Metrics include **precision**, **recall**, **mAP50**, **mAP50-95**, and **F1 score**.

---

## Dataset
The **Potato Leaf Disease Dataset** used in this study is sourced from [Kaggle](https://www.kaggle.com/datasets/muhammadarslanputra/potato-leaf-disease-dataset). It contains **2,152 images** categorized into three classes:
- **Early Blight**: 1,000 images
- **Late Blight**: 1,000 images
- **Healthy Leaves**: 152 images

The images were resized to **128x128 pixels** for uniformity during training.

---

## Methodology
![Fig1](https://github.com/user-attachments/assets/62494d2f-095b-42c7-a028-360bde542c0d)

### 1. **Data Preparation**
- **Annotation**: Each image was annotated with bounding box coordinates in `.txt` files.
- **Resizing**: Images were resized to **128x128 pixels** for consistent input dimensions.

### 2. **Model Architecture**
- **YOLOv8**: Utilizes a modified CSPDarknet53 backbone with a C2f module and SPPF layer.
- **YOLOv9**: Introduces Programmable Gradient Information (PGI) and Generalized Efficient Layer Aggregation Network (GELAN).
- **YOLOv10**: Features anchor-free detection and SWISH activation.
- **YOLOv11**: Incorporates **C3k2 Block**, **SPPF**, and **C2PSA** for enhanced feature extraction and attention mechanisms.

### 3. **Training**
- **Epochs**: 50
- **Batch Size**: 16
- **Image Size**: 128x128 pixels
- **Evaluation Metrics**: Precision, recall, mAP50, mAP50-95, and F1 score.

### 4. **Evaluation Metrics**
- **Precision**: Measures the accuracy of positive predictions.
- **Recall**: Measures the ability to identify all relevant instances.
- **mAP50**: Mean Average Precision at 50% IoU threshold.
- **mAP50-95**: Mean Average Precision across IoU thresholds from 50% to 95%.
- **F1 Score**: Harmonic mean of precision and recall.

---

## Results
### Model Performance Comparison
| Model     | Precision | Recall | mAP50  | mAP50-95 |
|-----------|-----------|--------|--------|----------|
| YOLOv8    | 88.7%     | 91.8%  | 98.3%  | 94.1%    |
| YOLOv9    | 97.6%     | 97.8%  | 99.5%  | 91.9%    |
| YOLOv10   | 83.2%     | 91.2%  | 96.1%  | 93.9%    |
| YOLOv11   | 98.1%     | 97.1%  | 99.5%  | 99.0%    |
## Examples of detection
![Fig07](https://github.com/user-attachments/assets/275fc76a-5b04-4f96-9127-f062b9953963)


### Key Findings
- **YOLOv11** outperformed all other models, achieving the highest **precision (98.1%)**, **recall (97.1%)**, and **mAP50-95 (99.0%)**.
- The model demonstrated excellent generalization ability, as shown by the **F1-confidence curve** and **precision-recall tradeoff**.
- **YOLOv11** achieved a **99.5% mAP50**, indicating superior object detection and classification performance.

---
