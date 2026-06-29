# 🫀 SmartECG-HD
### Smart ECG-Based Early Heart Disease Prediction System using Deep Learning

> An AI-powered wearable cardiac monitoring system for real-time ECG analysis, early heart disease prediction, and intelligent clinical decision support.

---

## 📌 Project Overview

SmartECG-HD is an intelligent cardiac monitoring system that combines:

- 📈 Wearable ECG acquisition
- 🤖 Deep Learning-based ECG analysis
- 🩺 Automated heart disease prediction
- ☁️ Cloud-based processing
- 📊 Clinical dashboard visualization

The system is designed to assist healthcare professionals by automatically analyzing ECG signals and detecting potential cardiac abnormalities at an early stage.

Unlike traditional ECG interpretation, SmartECG-HD leverages a Hybrid CNN + BiLSTM architecture to learn both morphological and temporal ECG characteristics for accurate prediction.

---

# 🎯 Objectives

- Continuous ECG monitoring using a wearable chest band
- Automated ECG preprocessing
- Beat segmentation and feature extraction
- Multi-class heartbeat classification (AAMI Standard)
- Early heart disease prediction
- Risk score generation
- Clinical decision support
- Dashboard integration

---

# 🩺 Diseases Covered

The system is designed to detect and assist in identifying:

- Arrhythmia
- Atrial Fibrillation (AF)
- Premature Ventricular Contractions (PVC)
- Bradycardia
- Tachycardia
- ST Segment Abnormalities
- Myocardial Infarction Indicators

---

# 🧠 Machine Learning Pipeline

```
Raw ECG Signal
        │
        ▼
Data Acquisition
        │
        ▼
Signal Preprocessing
        │
        ▼
R-Peak Detection
        │
        ▼
Beat Segmentation
        │
        ▼
Dataset Generation
        │
        ▼
CNN + BiLSTM Model
        │
        ▼
Prediction
        │
        ▼
Risk Score
        │
        ▼
Clinical Report
```

---

# 📂 Project Structure

```
SmartECG-HD/

│
├── datasets/
│
├── processed/
│
├── models/
│
├── reports/
│
├── notebooks/
│   ├── 01_data_acquisition.ipynb
│   ├── 02_signal_preprocessing.ipynb
│   ├── 03_model_training.ipynb
│   ├── 04_model_evaluation.ipynb
│   ├── 05_inference.ipynb
│   ├── 06_decision_engine.ipynb
│   └── 07_report_generation.ipynb
│
├── src/
│   ├── __init__.py
│   ├── config.py
│   ├── data_loader.py
│   ├── preprocessing.py
│   ├── label_generator.py
│   ├── dataset_builder.py
│   ├── feature_engineering.py
│   ├── model.py
│   ├── inference.py
│   ├── decision_engine.py
│   ├── report_generator.py
│   └── save_utils.py
│
├── figures/
│
├── logs/
│
└── README.md
```

---

# 📊 Datasets Used

## PhysioNet

- MIT-BIH Arrhythmia Database
- MIT-BIH Atrial Fibrillation Database
- Long-Term ST Database
- PTB-XL ECG Dataset
- PTB Diagnostic ECG Database

## Hospital Dataset

Collected from:

Arneja Heart & Multispeciality Hospital, Nagpur

Contains:

- ECG paper images
- ECG interpretations
- Clinical reports
- Angiography reports

---

# ⚙️ ECG Preprocessing

The preprocessing pipeline includes:

- Bandpass Filtering (0.5–40 Hz)
- Noise Removal
- Baseline Wander Removal
- Signal Normalization
- R-Peak Detection
- Beat Segmentation
- Dataset Generation

---

# ❤️ Beat Classification

The model follows the AAMI EC57 Standard.

| Class | Description |
|--------|-------------|
| N | Normal Beat |
| S | Supraventricular Beat |
| V | Ventricular Beat |
| F | Fusion Beat |
| Q | Unknown/Paced Beat |

---

# 🧠 Deep Learning Architecture

The prediction model uses a Hybrid CNN + BiLSTM network.

### CNN

- Conv1D
- Batch Normalization
- Max Pooling
- Dropout

### BiLSTM

Captures temporal ECG dependencies.

### Dense Layers

Fully connected layers for final classification.

### Output

Softmax (5 Classes)

---

# 📈 Model Training

Training Parameters

| Parameter | Value |
|-----------|-------|
| Optimizer | Adam |
| Learning Rate | 0.001 |
| Epochs | 20+ |
| Batch Size | 64 |
| Loss | Categorical Crossentropy |
| Validation Split | 20% |

---

# 📊 Evaluation Metrics

The model is evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC Curve
- AUC Score
- Confusion Matrix

---

# 📋 Generated Outputs

The system produces:

- Trained Model (.keras)
- Label Encoder
- Training History
- Confusion Matrix
- Classification Report
- Prediction Reports
- Risk Score
- Clinical Recommendations

---

# 📄 Example Prediction Output

```json
{
    "Prediction": "Normal",
    "Confidence": 98.42,
    "Risk Score": 3.7,
    "Heart Rate": 74,
    "Signal Quality": "Good",
    "Recommendation": "No immediate cardiac abnormality detected."
}
```

---

# 💻 Technology Stack

## Programming

- Python

## Machine Learning

- TensorFlow
- Keras
- Scikit-learn
- NumPy
- Pandas

## Signal Processing

- WFDB
- NeuroKit2
- SciPy

## Visualization

- Matplotlib

## Development

- Google Colab
- GitHub

---

# 🚀 Future Improvements

- Multi-lead ECG Support
- Transformer-based ECG Models
- Explainable AI (XAI)
- Real-time Streaming Inference
- TinyML Deployment
- Edge AI on ESP32
- Multi-Hospital Validation
- Clinical Trials

---

# 👨‍💻 Contributors

Final Year B.Tech Project

Computer Science & Design

Yeshwantrao Chavan College of Engineering (YCCE), Nagpur

---

# 📚 References

- PhysioNet
- MIT-BIH Arrhythmia Database
- PTB-XL ECG Dataset
- NeuroKit2 Documentation
- TensorFlow Documentation
- WFDB Python Package

---

# 📜 License

This project is developed for academic research and educational purposes.

Future versions may be extended for clinical validation and deployment.

---

# ⭐ Acknowledgements

We sincerely acknowledge:

- PhysioNet
- Arneja Heart & Multispeciality Hospital
- TensorFlow Team
- NeuroKit2 Developers
- Open Source Community

---

## 🌟 Project Vision

Our vision is to build an affordable AI-powered cardiac monitoring system capable of assisting clinicians through continuous ECG monitoring, intelligent disease prediction, and real-time clinical decision support, making advanced cardiac care more accessible.
