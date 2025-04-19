
# Waste Material Segregation Using CNN

## 📌 Objective

The aim of this project is to build a deep learning model using CNNs and transfer learning to automatically classify different types of waste materials. This helps in promoting sustainable waste management and improving recycling efficiency.

---

## 🧠 Problem Statement

Manual waste segregation is inefficient and error-prone. Automating this task using computer vision can significantly improve waste processing and recycling. The project classifies images into 7 categories:

- Cardboard  
- Glass  
- Metal  
- Paper  
- Plastic  
- Food Waste  
- Other  

---

## 📂 Dataset Overview

- The dataset is organized into folders, one for each waste category.
- Each folder contains multiple images representing that waste type.
- Images vary in shape but were resized to `(128, 128)` for training.

---

## 🧪 Tech Stack & Libraries

- **Python**
- **TensorFlow 2.x / Keras**
- **scikit-learn**
- **Matplotlib, Seaborn**
- **Pillow (PIL)**

---

## 🧹 Steps Followed

### 1. 📦 Data Preparation

- Loaded and resized all images to a fixed shape (128x128x3).
- Encoded labels using `LabelEncoder`.
- Visualized class distribution to understand imbalance.

### 2. 🧼 Preprocessing

- Normalized images using `ImageDataGenerator`.
- Applied real-time data augmentation:
  - Rotation, Zoom, Shearing
  - Horizontal and vertical flipping

### 3. 🧠 Model Building

- Started with a custom CNN but accuracy was low (~32%).
- Switched to **MobileNetV2** for transfer learning.
- Used dropout layers and global average pooling.
- Compiled with `Adam` optimizer and cross-entropy loss.

### 4. 🏋️ Model Training

- Trained on augmented data with:
  - `EarlyStopping`
  - `ReduceLROnPlateau`
  - `ModelCheckpoint`
- Achieved up to **65% validation accuracy**.

### 5. 🧪 Model Testing

- Evaluated on a test split (~10% data).
- Test accuracy was **~18%**, likely due to domain shift or class imbalance.
- Classification report and confusion matrix were plotted.

---

## 📈 Results

| Dataset Split | Accuracy |
|---------------|----------|
| Training       | ~58.6%   |
| Validation     | ~65.3%   |
| Test           | ~18.7%   |

---

## 📌 Key Learnings

- Transfer learning significantly outperformed custom CNNs.
- Data augmentation helped reduce overfitting.
- Class imbalance and low inter-class variation likely affected test performance.
- Future improvements could include better dataset balancing, ensemble models, or using attention mechanisms.

---

## ✅ Conclusion

This project shows how CNNs and transfer learning can be used to automate waste segregation. While validation accuracy was strong, further work is needed to improve generalization. This type of system can be deployed in real-world recycling systems or smart bins.

**Simhadri Sai Krishna**  
Date: April 19, 2025
