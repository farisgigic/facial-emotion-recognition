cat << 'EOF' > README.md
# 📘 Facial Emotion Recognition Using Classical Machine Learning
*A lightweight, interpretable, and resource-efficient approach to emotion classification.*

## 📌 Overview
This project investigates whether **handcrafted facial features** (HOG and optionally facial landmarks) combined with **classical machine learning algorithms** (primarily SVM) can accurately classify human emotions from facial images.

While modern emotion recognition systems typically use deep learning (CNNs), this project focuses on a more interpretable, efficient, and educational approach suitable for devices with limited computational power.

---

## ❓ Research Question
**Can handcrafted facial features combined with classical machine learning algorithms provide sufficient information to accurately classify human emotions from images?**

---

## 📂 Dataset
The project uses the **FER2013 Dataset**, containing **35,887 grayscale facial images (48×48 pixels)** labeled with seven emotion categories.

---

## 🧠 Methodology

### **1. Data Preparation**
- Load and normalize 48×48 grayscale images
- Split into training and testing sets

### **2. Feature Extraction – HOG**
Histogram of Oriented Gradients captures:
- edges  
- gradients  
- facial structure  

Producing ~1296 features per image.

### **3. SVM Classification**
A Support Vector Machine (RBF kernel) is trained on the HOG features.

### **4. Model Evaluation**
Measured using:
- Accuracy  
- F1-score  
- Precision/Recall  
- Confusion Matrix  

---

## 📊 Results Summary

| Emotion | Precision | Recall | F1-score |
|--------|-----------|--------|----------|
| Angry | 0.45 | 0.36 | 0.40 |
| Disgust | 1.00 | 0.23 | 0.37 |
| Fear | 0.46 | 0.31 | 0.37 |
| Happy | 0.64 | 0.80 | 0.71 |
| Neutral | 0.46 | 0.54 | 0.49 |
| Sad | 0.46 | 0.39 | 0.42 |
| Surprise | 0.67 | 0.72 | 0.69 |

Key findings:
- **Happy** performs best  
- **Fear** and **Disgust** perform worst  
- Classical ML performs **moderately**, but not on par with deep learning  

---

## 🔍 Key Takeaways

### ✅ Strengths
- Interpretable  
- Fast and lightweight  
- Good baseline  
- Works on low-resource systems  

### ❗ Limitations
- Struggles with subtle expressions  
- Dataset imbalance  
- Low-resolution images limit detail  

---

## 🛠️ Technologies Used
- Python  
- scikit-image  
- cuML (GPU SVM)  
- NumPy  
- Matplotlib / Seaborn  
- FER2013 dataset

---

## 📁 Project Structure

