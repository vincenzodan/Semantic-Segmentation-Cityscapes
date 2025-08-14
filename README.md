# 🚗 Semantic Segmentation on Cityscapes

## 📌 Overview
This project implements a **semantic segmentation pipeline** to classify each pixel of an image into predefined categories, using the **Cityscapes** dataset.  
The model is designed for **urban scene understanding**, distinguishing between **road, cars, pedestrians, buildings, sky**, and other urban elements.

## 🎯 Objectives
- Accurately segment urban street scenes.  
- Leverage deep learning architectures for pixel-wise classification.  
- Achieve high IoU (Intersection over Union) and mIoU scores across classes.

## 🗂 Dataset
- **Name:** [Cityscapes Dataset](https://www.cityscapes-dataset.com/)  
- **Location:** Germany (various cities)  
- **Images:** High-resolution (2048×1024)  
- **Labels:** 30 classes (19 for evaluation)

## 🛠️ Technologies
- Python  
- PyTorch & Torchvision  
- NumPy, Pandas  
- Matplotlib, Seaborn (visualization)  

## ⚙️ Model Pipeline
1. **Data Loading:** Reading and preprocessing images and labels.  
2. **Augmentation:** Random cropping, flipping, and normalization.  
3. **Model Architecture:** U-Net  
4. **Training:**  
   - Loss: `CrossEntropyLoss` (weighted by class frequency)  
   - Optimizer: Adam / SGD  
   - Scheduler: StepLR  
5. **Evaluation:**  
   - Metrics: mIoU, Precision, Recall, F1. 
   - Visualization of segmentation masks.  

## 📊 Results

| Metric         | Value  |
|----------------|--------|
| **Macro**      | 0.3584 |
| **Micro**      | 0.8062 |
| **Weighted**   | 0.8237 |

<div style="text-align: center;">
  <img width="1266" height="708" alt="Screenshot 2025-08-14 154956" src="https://github.com/user-attachments/assets/89801256-5a2e-4b86-b3a2-f004b2f7038f" />
</div>

<div style="text-align: center;">
  <img width="840" height="539" alt="Screenshot 2025-08-14 154911" src="https://github.com/user-attachments/assets/762e238c-f0a2-4c59-a4ff-b9f10227632e" />
</div>

---

## 🏆 Best and Worst Classes

<div style="text-align: center;">
  <div style="display: inline-block; margin-right: 100px; vertical-align: top;">
    <h4>Top 5 Classes</h4>
    <table border="1">
      <tr><th>Class</th><th>F1-score</th></tr>
      <tr><td>road</td><td>0.97</td></tr>
      <tr><td>sky</td><td>0.93</td></tr>
      <tr><td>vegetation</td><td>0.91</td></tr>
      <tr><td>building</td><td>0.90</td></tr>
      <tr><td>car</td><td>0.89</td></tr>
    </table>
  </div>

  <div style="display: inline-block; margin-left: 100px; vertical-align: top;">
    <h4>Bottom 5 Classes</h4>
    <table border="1">
      <tr><th>Class</th><th>F1-score</th></tr>
      <tr><td>rider</td><td>0.00</td></tr>
      <tr><td>bus</td><td>0.01</td></tr>
      <tr><td>motorcycle</td><td>0.02</td></tr>
      <tr><td>truck</td><td>0.11</td></tr>
      <tr><td>train</td><td>0.17</td></tr>
    </table>
  </div>
</div>

## 📘 More Details
Learn more about the project in the [full presentation](./Presentazione.pdf).

---
## 👥 Contributors

- [@Vincenzo D'Angelo](https://github.com/vincenzodan)
- [@Giorgio Di Costanzo](https://github.com/GiorgioDiCostanzo)
