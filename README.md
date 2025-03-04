# DL_PracticeLabAssignment_2

## OCR Transfer Learning Pipeline

This project implements an OCR pipeline using transfer learning, inspired by the research paper:

> **Leveraging Transfer Learning and GAN Models for OCR from Engineering Documents**  
> *Wael Khallouli et al., IEEE*

---

## 📌 Overview

### 🎯 Objective:
Adapt a pre-trained **ResNet101** model for OCR tasks by fine-tuning its top layers.  
This notebook demonstrates the end-to-end process—from dataset preparation to model evaluation—using the **ICDAR 2015** dataset.

### 📂 Dataset:
- **Dataset Name:** ICDAR 2015  
- **Source:** [ICDAR 2015 on Roboflow](https://universe.roboflow.com/jeevan-m/icdar-2015/browse?queryText=&pageSize=50&startingIndex=0&browseQuery=true)  
- **Preprocessing Steps:**
  - Resized images to **224×224** pixels
  - Converted images to **grayscale**
  - Normalized pixel values to **[0, 1]**
- **Data Augmentation:** Applied transformations using **Keras' ImageDataGenerator** (rotation, width/height shifts, zoom, and flips).

### 🏗️ Model:
- The **ResNet101** model (pre-trained on ImageNet) is used as the backbone.
- Initially, the entire model is **frozen** to preserve learned features.
- Later, the top layers are **unfrozen** for fine-tuning with a **lower learning rate**.
- Feature maps are visualized to inspect how the model perceives text at different layers.

### 📊 Evaluation:
- The model is assessed using **classification metrics**:
  - ✅ **Accuracy**
  - ✅ **Precision**
  - ✅ **Recall**
  - ✅ **F1-score**
  - ✅ **Confusion Matrix**
- Training and validation trends are plotted to monitor performance.

---


