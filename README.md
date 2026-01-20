# Unmasking The Unreal — Deepfake Detection

## Short Description

A lightweight, CPU-friendly deepfake detection system implemented in a **single Python script (`complete.py`)**, designed to detect manipulated facial videos using MediaPipe-based face extraction and an EfficientNet-B0 deep learning classifier. The project prioritizes simplicity, reproducibility, and execution on limited compute (Kaggle CPU).

---

## Project Overview

This repository hosts a **minimal GitHub version** of the project **"Unmasking The Unreal: Deepfake Detection Using Deep Learning"**.

All preprocessing, training, and evaluation logic is consolidated into **one file: `complete.py`**. The full experimental workflow, visualizations, and exploratory steps were originally developed and executed on Kaggle.

📌 **Original Kaggle Notebook (full workflow & results):**
[https://www.kaggle.com/code/annanyasahoo/complete](https://www.kaggle.com/code/annanyasahoo/complete)

---

## Key Characteristics

* **Single-file implementation** (`complete.py`)
* **CPU-only compatible** (tested on Kaggle CPU runtime)
* **Face-centric approach** using MediaPipe
* **EfficientNet-B0** with ImageNet pretrained weights
* **Video-level data splitting** to prevent data leakage
* **Threshold tuning** for optimal classification performance

---

## Dataset Summary

* Dataset: DeepFake Detection (DFD) dataset (subset)
* Videos used:

  * 363 Real
  * 363 Fake
* Frames sampled: 10 per video
* Total face images: ~4,750
* Split: Train / Validation / Test (video-wise)

⚠️ **Dataset is NOT included in this repository.**
Refer to the Kaggle notebook for dataset access and preprocessing details.

---

## File Structure

```
.
├── complete.py    # End-to-end deepfake detection pipeline
├── README.md
└── .gitignore
```

---

## How to Run

```bash
pip install tensorflow mediapipe opencv-python numpy pandas scikit-learn matplotlib tqdm pillow
python complete.py
```

> Note: Paths inside the script may need adjustment depending on local dataset location.

---

## Results (From Kaggle Experiments)

* **AUC**: ~0.956
* **Accuracy**: ~92.8%
* **Optimal Decision Threshold**: ~0.36

These results were obtained on a balanced subset of the DFD dataset using a CPU-only training setup.

---

## Important Notes

* This repository intentionally contains **only the core script**.
* Large datasets and trained model weights are excluded.
* For full experimentation, plots, and explanations, refer to the Kaggle notebook link above.

---

## License

MIT License

---

## Author

**Annanya Priyadarshini Sahoo**

Developed as part of a deep learning project focused on practical and efficient deepfake detection.
