# Segmentation of Brain MRI Using Advanced Deep Learning Models: PSPNet and UNet-EfficientNetB7

---

## **Abstract**
Brain tumor segmentation is a critical task in medical imaging. This project focuses on segmenting Low-Grade Gliomas (LGGs) in brain MRI scans using advanced deep learning models, PSPNet and UNet-EfficientNetB7. The models were evaluated for segmentation performance using Dice score, IoU, and accuracy. The project demonstrated that transfer learning significantly outperforms models trained from scratch.

---

## **Table of Contents**
1. [Introduction](#introduction)
2. [Literature Review](#literature-review)
3. [Methodology](#methodology)
4. [Results](#results)
5. [Discussion](#discussion)
6. [Conclusion](#conclusion)
7. [How to Use](#how-to-use)
8. [Acknowledgements](#acknowledgements)

---

## **Introduction**

### **Research Problem Definition**
Brain tumors are among the deadliest cancers due to their unpredictable growth patterns and difficulty in segmentation. This project focuses on using deep learning techniques for accurately segmenting brain MRI images, specifically targeting LGGs. The research compares models trained from scratch with those utilizing transfer learning.

### **Research Aim and Objectives**
- **Aim**: To evaluate the performance of advanced deep learning models (PSPNet and UNet-EfficientNetB7) for brain MRI segmentation.
- **Objectives**:
  1. Conduct a literature review of suitable deep learning models.
  2. Process and prepare the brain MRI dataset for segmentation tasks.
  3. Train and evaluate models on segmentation performance metrics.

### **Research Questions**
1. How effective are PSPNet and UNet-EfficientNetB7 in segmenting brain tumors?
2. Does transfer learning outperform models trained from scratch?
3. Which architecture generalizes better across datasets?

---

## **Literature Review**

### **Key Findings**
1. **CNN-Based Approaches**: Highlighted models like AlexNet, ResNet, and InceptionV3 for medical imaging tasks.
2. **Transfer Learning**: Demonstrated significant improvements in segmentation accuracy and efficiency.
3. **Research Gap**: Existing methods face challenges in boundary precision and computational efficiency.

---

## **Methodology**

### **Dataset**
- **Source**: [Kaggle - LGG Brain MRI Segmentation Dataset](https://www.kaggle.com/datasets/mateuszbuda/lgg-mri-segmentation).
- **Description**:
  - Contains MRI images and segmentation masks for LGGs.
  - Includes 110 patients with genomic cluster data.

### **Data Preprocessing**
1. **Handling Missing Data**: Used Python's `SimpleImputer` to fill missing values.
2. **Train-Test Split**:
   - Training: 70%.
   - Validation: 15%.
   - Test: 15%.

### **Models**
1. **PSPNet**:
   - **From Scratch**: Built complete architecture without pre-trained weights.
   - **Transfer Learning**: Integrated ResNeXt50-32x4d encoder pre-trained on ImageNet.
2. **UNet-EfficientNetB7**:
   - Combined UNet’s segmentation capabilities with EfficientNetB7’s feature extraction.

### **Performance Metrics**
- **Dice Score**: Measures overlap between predicted and ground truth masks.
- **IoU (Intersection over Union)**: Evaluates segmentation accuracy.
- **Accuracy**: Percentage of correctly classified pixels.

---

## **Predicted Images by PSPNet From Scratch** 

![image](https://github.com/user-attachments/assets/c85aadd1-342c-4838-9840-8aa7df9dc602)
![image](https://github.com/user-attachments/assets/d8099080-823a-486c-b241-5b2d27bce355)

---


## **Predicted Images By PSPNet-Resnext50_32x4d and UNet-EfficientNetB7**

![image](https://github.com/user-attachments/assets/177f45d9-c8ec-4c53-97d6-f98e0490e50d)
![image](https://github.com/user-attachments/assets/43b36db2-59d1-4d73-8a5d-e67d616f60e1)

---







## **Results**

### **Performance Metrics**
| **Model**                | **Dice Score (Test)** | **IoU (Test)** | **Accuracy (Test)** |
|--------------------------|-----------------------|----------------|---------------------|
| PSPNet (Scratch)         | 0.8054               | 0.7815         | 99.51%             |
| PSPNet (Transfer)        | 0.9064               | 0.8763         | 99.78%             |
| UNet-EfficientNetB7      | 0.9262               | 0.9007         | 99.83%             |

### **Graphs**
1. **Accuracy vs Epochs**
   ![Accuracy](evaluation/results/graphs/accuracy_vs_epoch.png)
   


