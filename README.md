# 🚗 Semantic Segmentation on Cityscapes

## 📌 Overview
This project implements a **semantic segmentation pipeline** to classify each pixel of an image into predefined categories, using the **Cityscapes** dataset.  
The model is designed for **urban scene understanding**, distinguishing between **road, cars, pedestrians, buildings, sky**, and other urban elements.

## 🎯 Tasks:
   - Train U-Net from scratch  
   - Train ASPP from scratch  
   - Train ResNet from scratch  
   - Fine-tune DeepLabv3+ on Cityscapes  
   - Transfer learning on SUIM dataset

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
3. **Model Architectures:** U-Net, Res-Net, ASPP, DeepLabv3+ (tested separately)
4. **Training:**  
   - Losses: `CrossEntropyLoss` (weighted by class frequency), `Focal Loss`, `Generalized Dice Loss`
   - Optimizer: Adam / SGD  
   - Scheduler: StepLR  
5. **Evaluation:**  
   - Metrics: mIoU, Precision, Recall, F1. 
   - Visualization of segmentation masks.  

## 📊 Best Results
| Metric         | Value        |
|----------------|--------------|
| **Macro**      | 0.4492       |
| **Micro**      | 0.8209       |
| **Weighted**   | 0.8345       |

<br>

<center>
   <img width="1257" height="276" alt="image" src="https://github.com/user-attachments/assets/ea2993a6-078f-4294-a58d-a058d4d226a2" />
</center>
<center>
  <img width="854" height="534" alt="image" src="https://github.com/user-attachments/assets/c98bc89e-4e5a-407a-bbec-0befc9763ab3" />
</center>

<br><br>

<center>
  <img width="1271" height="708" alt="image" src="https://github.com/user-attachments/assets/f7f1cb92-57f8-40b6-ab64-436f2bf33b7a" />
</center>

---

## 🏆 Best and Worst Classes 
<div style="text-align: center;">
  <div style="display: inline-block; margin-right: 100px; vertical-align: top;">
    <h4>Best Classes</h4>
    <table border="1">
      <tr><th>Class</th><th>Precision</th><th>Recall</th><th>F1-score</th></tr>
      <tr><td>road</td><td>0.97</td><td>0.97</td><td>0.97</td></tr>
      <tr><td>car</td><td>0.92</td><td>0.95</td><td>0.94</td></tr>
      <tr><td>sky</td><td>0.90</td><td>0.94</td><td>0.92</td></tr>
      <tr><td>building</td><td>0.88</td><td>0.94</td><td>0.91</td></tr>
      <tr><td>vegetation</td><td>0.92</td><td>0.89</td><td>0.91</td></tr>
    </table>
  </div>

  <div style="display: inline-block; margin-left: 100px; vertical-align: top;">
    <h4>Worst Classes</h4>
    <table border="1">
      <tr><th>Class</th><th>Precision</th><th>Recall</th><th>F1-score</th></tr>
      <tr><td>wall</td><td>0.60</td><td>0.29</td><td>0.39</td></tr>
      <tr><td>fence</td><td>0.43</td><td>0.44</td><td>0.44</td></tr>
      <tr><td>pole</td><td>0.60</td><td>0.39</td><td>0.47</td></tr>
      <tr><td>train</td><td>0.81</td><td>0.36</td><td>0.50</td></tr>
      <tr><td>traffic sign</td><td>0.74</td><td>0.49</td><td>0.59</td></tr>
    </table>
  </div>
</div>

## 📘 More Details
Learn more about the project in the [full presentation](./Presentazione.pdf).

---

## 👥 Contributors

- [@Vincenzo D'Angelo](https://github.com/vincenzodan)
- [@Giorgio Di Costanzo](https://github.com/GiorgioDiCostanzo)
