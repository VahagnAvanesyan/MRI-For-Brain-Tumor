# 🧠 Brain Tumor Classification using CNN

<div align="center">

A Deep Learning project for classifying brain MRI images into different tumor categories using a Convolutional Neural Network (CNN).

</div>

---

## 📌 Project Overview

This project uses **Deep Learning** and **Computer Vision** techniques to classify brain MRI images.

The goal is to build a CNN model that can identify whether an MRI image belongs to one of four categories:

* 🧬 **Glioma**
* 🧬 **Meningioma**
* ✅ **No Tumor**
* 🧬 **Pituitary Tumor**

The model learns visual patterns from MRI scans and predicts the corresponding class.

---

## 🚀 Technologies Used

| Technology            | Purpose                    |
| --------------------- | -------------------------- |
| 🐍 Python             | Programming language       |
| 🧠 TensorFlow / Keras | Deep Learning framework    |
| 🖼️ CNN               | Image classification model |
| 📊 Matplotlib         | Data visualization         |
| 🔢 NumPy              | Numerical operations       |
| 📚 Scikit-learn       | Machine learning utilities |
| 📓 Jupyter Notebook   | Development environment    |

---

## 📂 Dataset

The dataset contains brain MRI images separated into:

```
Dataset/
│
├── Training/
│   ├── Glioma/
│   ├── Meningioma/
│   ├── No Tumor/
│   └── Pituitary/
│
└── Validation/
    ├── Glioma/
    ├── Meningioma/
    ├── No Tumor/
    └── Pituitary/
```

### Image Processing

Before training:

* Images resized to **128×128 pixels**
* Pixel values normalized to range **0-1**
* Data loaded using TensorFlow image dataset utilities

---

## 🏗️ Model Architecture

The model is a custom Convolutional Neural Network:

```
Input Image
     │
     ▼
Rescaling Layer
     │
     ▼
Conv2D + MaxPooling
     │
     ▼
Conv2D + MaxPooling
     │
     ▼
Conv2D + MaxPooling
     │
     ▼
Flatten
     │
     ▼
Dense Layer
     │
     ▼
Dropout
     │
     ▼
Softmax Output (4 Classes)
```

---

## ⚙️ Training Configuration

| Parameter      | Value                           |
| -------------- | ------------------------------- |
| Image Size     | 128 × 128                       |
| Batch Size     | 32                              |
| Optimizer      | Adam                            |
| Loss Function  | Sparse Categorical Crossentropy |
| Epochs         | 15                              |
| Output Classes | 4                               |

---

## 📈 Model Performance

The model was evaluated on the validation dataset.

Metrics:

* Accuracy
* Loss
* Validation Accuracy
* Validation Loss

Training and validation curves were visualized to analyze model performance.

---

## 🔮 Prediction Example

The trained model can predict a new MRI image:

Example output:
![Prediction Example](https://github.com/user-attachments/assets/11c2df25-f3c4-4d78-9bda-705e53e7f313)


---

## 📁 Project Structure

```
Brain-Tumor-Classification/
│
├── Brain_Tumor_Classification.ipynb
│
├── README.md
├── requirements.txt
├── .gitignore
│
└── Dataset/
    ├── Training/
    └── Validation/
```

---

## ▶️ Installation & Usage

### 1. Clone repository

```bash
git clone <repository_url>
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run Jupyter Notebook

```bash
jupyter notebook
```

Open the notebook and run all cells.

---

## 💾 Model Saving

After training, the model can be saved:

```python
model.save("brain_tumor_model.keras")
```

and loaded later for predictions.

---

## ⚠️ Disclaimer

This project is created for educational purposes only.

The model is not intended for medical diagnosis or clinical usage.

---

## 👨‍💻 Author

**Vahagn Avanesyan**

GitHub:
https://github.com/VahagnAvanesyan

---

⭐ If you find this project useful, consider giving it a star!
