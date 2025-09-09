# Weather Simulation and Object Detection: Evaluating YOLO and Faster-R-CNN Performance
---

## 📌 Overview

This project investigates the performance of leading object detection models—YOLO and Faster R-CNN—under challenging weather conditions such as fog and snow. As these environmental factors severely impact visibility, reliable object detection becomes a critical requirement for autonomous vehicles and other safety-critical applications.

In this project, we wanted to extend our exploration of object detection into a domain with significant real-world impact: autonomous driving in low-visibility scenarios.

---

## 🎯 Objectives

Address the scarcity of labeled adverse weather images for training.

Evaluate and compare YOLO and Faster R-CNN under synthetic and real-world weather conditions.

Analyze how synthetic data augmentation affects detection accuracy in extreme environments.

---

## 🧪 Methodology
### 1. Dataset Construction
- Base Dataset: Road Vehicle Images Dataset.
- Augmentation: Applied custom fog and snow transformations to generate synthetic weather conditions.
- Final Training and Validation Set: Over 6,000 images including augmented weather conditions.
- Test Set: Real-world images from the DAWN (Driving in Adverse Weather Nature) dataset.

### 2. Model Selection
- YOLO (You Only Look Once): Optimized for real-time object detection.
- Faster R-CNN: Known for high precision in detection tasks.

### 3. Training & Evaluation
- Models trained on augmented dataset.
- Performance compared using metrics such as mAP (mean Average Precision) and IoU (Intersection over Union).
- Evaluated on held-out DAWN images to assess real-world generalizability.

---

## 📊 Key Contributions
- Demonstrated that synthetic augmentation can effectively simulate adverse weather and enhance training data diversity.
- Provided a comparative analysis of YOLO vs. Faster R-CNN performance in degraded visibility.
- Highlighted practical trade-offs between speed (YOLO) and accuracy (Faster R-CNN) in adverse environments.

---

## 🔍 Results & Insights
- YOLO showed superior inference speed, making it suitable for real-time systems but with slight compromises in precision.
- Faster R-CNN outperformed in detection accuracy, especially in denser scenes, but at the cost of slower inference.
- Synthetic data improved robustness, though real-world domain gaps remain a challenge.

---

## 📁 Project Structure
```bash
project-root/
├── code/                       # Google Colab notebooks
│   ├── Preprocess_LabelTranformation.ipynb
│   ├── Preprocess_ImageNoiseGenerator_Start.ipynb
│   ├── Preprocess_ImageNoiseGeneration_Experiment.ipynb
│   ├── Training_FasterRCNN.ipynb
│   └── Training_YOLO.ipynb
│
├── README.md                   # Project documentation (this file)
```

--- 

## 📖 Citation
- Kenk, M. (2020). Dawn (Version 3) [Data set]. Mendeley Data. https://doi.org/10.17632/766ygrbt8y.3 
- Yeafi, A. (2023). Road Vehicle Images Dataset (Version 2) [Data set]. Retrieved from https://www.kaggle.com/datasets/ashfakyeafi/road-vehicle-images-dataset/data 
