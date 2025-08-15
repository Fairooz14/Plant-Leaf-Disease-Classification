# 🌿 Comparative Study of CNN-Based Architectures for Plant Leaf Disease Classification

## 📌 Overview
Plant leaf diseases are a major threat to global agricultural productivity.  
Early and accurate detection is essential for preventing crop damage and ensuring food security.  
This project presents a **comparative analysis** of five Convolutional Neural Network (CNN) architectures for automated plant leaf disease classification using a publicly available dataset.

We implemented and evaluated:
- **Basic CNN**
- **VGG16**
- **VGG19**
- **ResNet50**
- **InceptionResNetV2**

The dataset was preprocessed with normalization, augmentation, and class balancing to improve generalization.  
Models were trained under **identical experimental conditions** to ensure fair comparison.

---

## 📂 Dataset
- **Source:** [Plant Disease Recognition Dataset](https://www.kaggle.com/datasets/rashikrahmanpritom/plant-disease-recognition-dataset)
- **Classes:** Multiple plant disease categories + healthy leaves
- **Data Splits:** Train / Validation / Test
- **Image Size:** 224 × 224 pixels
- **Augmentation Techniques:**
  - Random Flip
  - Random Rotation
  - Random Zoom
  - Random Contrast

---

## 📊 Results

After training all models on the Plant Disease Recognition Dataset, we evaluated them using Accuracy, Precision, Recall, and F1-Score.  
The table below summarizes the performance of each architecture:

| Model              | Accuracy | Precision | Recall | F1-Score |
|--------------------|----------|-----------|--------|----------|
| **Basic CNN**      | **93.99**| **0.93**  | **0.92** | **0.92** |
| VGG16              | 80.67    | 0.82      | 0.80   | 0.80     |
| VGG19              | 84.67    | 0.85      | 0.84   | 0.84     |
| ResNet50           | 36.67    | 0.26      | 0.36   | 0.25     |
| InceptionResNetV2  | 92.00    | 0.92      | 0.92   | 0.92     |

**Key Observations:**
- The **Basic CNN** achieved the highest accuracy (93.99%) while maintaining low computational complexity, making it suitable for real-time and resource-limited applications.
- **InceptionResNetV2** performed competitively with 92% accuracy, excelling in complex feature extraction but requiring more computational resources.
- **VGG16** and **VGG19** achieved moderate accuracy, performing well on high-contrast lesions but struggling with subtle disease symptoms.
- **ResNet50** performed poorly on this dataset due to insufficient domain-specific fine-tuning, with an accuracy of only 36.67%.

**Visual Evaluation:**
- Confusion matrices were plotted for each model to analyze per-class performance.
- Predicted image samples demonstrated that Basic CNN and InceptionResNetV2 made consistent predictions across disease classes.

