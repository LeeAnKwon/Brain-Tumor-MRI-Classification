# Brain Tumor MRI Classification

## Overview
This project focuses on multi-class classification of brain tumor MRI images using deep learning models.
The task is to classify brain MRI scans into four categories:
- Glioma
- Meningioma
- Pituitary tumor
- Healthy

Various neural network architectures were implemented and compared to analyze performance differences.

---

## Dataset
- Total images: 16,269
- Classes:
  - Glioma: 3,325
  - Meningioma: 3,266
  - Pituitary: 2,974
  - Healthy: 6,704
- Data split:
  - Train: 70%
  - Validation: 15%
  - Test: 15%

> Note: The dataset is not included in this repository due to size and licensing issues.

---

## Data Preprocessing & Augmentation
- Offline augmentation applied only to training data (4× increase):
  - Rotation (±20°)
  - Width/height shift (±10%)
  - Shear (10%)
  - Zoom (10%)
  - Horizontal flip
- Online augmentation during training:
  - Rescaling (1/255)
  - Rotation (±15°)
  - Zoom (20%)
  - Width/height shift (20%)
  - Horizontal flip

---

## Models Implemented
- MLP / DNN
- RNN
- LSTM
- GRU
- CNN (V1 ~ V3)
- CNN + LSTM
- ResNet50
- MobileNet

All models were implemented using TensorFlow/Keras.

---

## Results
- Best performing model: **LSTM**
- Test accuracy: **97.38%**

Model performance was evaluated using classification accuracy on the test dataset.

---

## Repository Struct
brain-tumor-mri-classification/
├─ notebooks/ # Jupyter notebooks for each model
├─ data/ # Dataset directory (not included)
├─ results/ # Experiment outputs
├─ reports/ # Project report (PDF)
├─ README.md
└─ .gitignore


---

## How to Run
1. Prepare the dataset with the following directory structure:
data/
├─ train/
├─ val/
└─ test/

2. Open the desired notebook in `notebooks/`
3. Run the notebook sequentially (Google Colab recommended)

---

## Notes
- This project was conducted as part of a deep learning course.
- The focus is on model comparison and experimental analysis rather than deployment.

