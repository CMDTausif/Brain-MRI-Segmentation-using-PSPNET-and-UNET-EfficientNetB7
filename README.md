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
 

### **Code Link**
- **Source**:

-https://www.kaggle.com/code/chaudhurimdtausif/psp-net-pytorch

-https://www.kaggle.com/code/chaudhurimdtausif/pspnet-from-scratch

-https://www.kaggle.com/code/chaudhurimdtausif/efiicientnetb7-v2

-https://www.kaggle.com/code/chaudhurimdtausif/implementation3-v4





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


---

### **Graphs**
1. **Accuracy vs Epochs**
   ![image](https://github.com/user-attachments/assets/7107d1f8-7600-4c4d-ae64-e77a14593a43)
   ![image](https://github.com/user-attachments/assets/ac26f68f-e9b7-465e-abc4-9701c5582697)


   
2. **Loss vs Epochs**
   ![image](https://github.com/user-attachments/assets/37394d9d-3129-46ff-9c27-158b7435b85b)
   ![image](https://github.com/user-attachments/assets/9a947e8b-5642-43f5-9f94-c0e22543af5e)



3. **Dice Score vs Epochs**
   ![image](https://github.com/user-attachments/assets/f051038e-c48e-4832-aab1-8862331a11fe)
   ![image](https://github.com/user-attachments/assets/0776e9c4-512e-4471-9372-a77c05872128)


4. **IOU Score vs Epochs**
   ![image](https://github.com/user-attachments/assets/4fe22558-aae8-48aa-a217-eeb342d563c1)
   ![image](https://github.com/user-attachments/assets/235e74ec-53e0-4ce6-a82d-58a7d5e9df94)


## **Discussion**

### **Key Insights**
1. **Transfer Learning Advantage**:
   - PSPNet and UNet-EfficientNetB7 with pre-trained weights converged faster.
   - Achieved higher segmentation metrics compared to scratch models.
2. **Model Comparison**:
   - UNet-EfficientNetB7 outperformed PSPNet in Dice and IoU scores across datasets.
3. **Limitations**:
   - High computational cost for scratch models.
   - Dataset limited to LGGs only.

---

## **Conclusion**
- Transfer learning significantly enhances segmentation performance.
- UNet-EfficientNetB7 is recommended for brain tumor segmentation tasks.
- Future research can extend to 3D segmentation and multi-class tumor segmentation.

---


   




