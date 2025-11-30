# ATM Security System Using Acoustic AI

### **Real-Time Threat Detection Using Hybrid Deep Learning (CRNN)**

This project introduces an intelligent **acoustic-based ATM security system** designed to detect physical attacks such as drilling, sawing, and hammering — *in real time*.
Unlike traditional vibration sensors that generate false alarms, this system **listens to the environment** and identifies real threats using deep learning.

---

##  Features

* **Hybrid CRNN Architecture**
  Combines CNN (spatial feature extraction) + Bidirectional RNN (temporal rhythm analysis).

* **Real-Time Audio Threat Detection**
  Classifies *Normal* vs *Anomaly* sounds live.

* **MFCC-Based Feature Engineering**
  Converts raw sound into spectral fingerprints.

* **Data Augmentation**
  Gaussian noise injection to expand training samples.

* **Streamlit Dashboard**
  Live monitoring interface with real-time predictions.

* **High Accuracy**
  Achieved **94.65% accuracy** on full dataset (UrbanSound8K + Industrial sounds).

---

## Project Structure

```
├── 1_raw_data/                 # (Sample Only) Raw .wav files  
├── 2_processed_data/           # Organized Normal vs Anomaly  
├── 3_features/                 # MFCC numpy arrays (.npy)  
├── 4_models/                   # Saved models + training plots  
├── 01_data_preparation.py      # Data sorting & labeling  
├── 02_feature_extraction.py    # Converts audio → MFCC  
├── 04_train_enhanced_model.py  # Hybrid CRNN training script  
├── 07_dashboard.py             # Streamlit real-time dashboard  
├── requirements.txt            # Dependencies  
└── README.md                   # Documentation  
```

---

##  Important Note About Dataset

Due to file-size limits, the repository contains only a **small sample** of the original dataset in the `1_raw_data/` folder.

---
## Full Dataset Contents
* cnc cutting dataset/ *
* Drilling/ *
* Glassbreaking/ *
* hand_saw/ *
* UrbanSound8K/ *

---
## Installation

### Step:1️ Clone the repository

```bash
git clone https://github.com/Abishek2k04/AcousticAI.git
cd AcousticAI
```

### Step:2️ Install required packages

```bash
pip install -r requirements.txt
```

---

## How to Run 

### **Step 1 — Data Preparation**

Sorts raw audio into *Normal* and *Anomaly* folders.

```Terminal
python 01_data_preparation.py
```

### **Step 2 — Feature Extraction**

Generates `X_data.npy` (MFCC), `y_labels.npy` (Labels).

```Terminal
python 02_feature_extraction.py
```

### **Step 3 — Train Hybrid CRNN Model**

(Trains with sample dataset; accuracy will be lower.)

```Terminal
python 04_train_enhanced_model.py
```

### **Step 4 — Launch Dashboard**

Run the real-time monitoring interface:

```Terminal
streamlit run 07_dashboard.py
```

---

## 📊 Results (Using Full Dataset)

| Metric    | Score      |
| --------- | ---------- |
| Accuracy  | **94.65%** |
| Precision | ~95%       |
| Recall    | High       |

### Confusion Matrix Highlights

* Correctly detected **109 / 116** threat events
* Only **6 false alarms** out of 127 normal samples

---

## Technologies Used

* **Python**
* **TensorFlow / Keras** – Deep Learning
* **Librosa** – Audio Processing
* **NumPy, Pandas**
* **Matplotlib, Seaborn**
* **Streamlit, Ngrok** – Deployment/UI

---

##  Author

**ABISHEK A**

**B.Tech Computer Science and Engineering Spec in Data Science**

**Github:** https://www.github.com/Abishek2k04

---
**Confusion Matrix**

<img width="350" height="350" alt="Confusion Matrix" src="https://github.com/user-attachments/assets/6615fa1c-971c-4fea-b937-81b9f0b17c25"/>

---
**This Comparison Shows CNN vs CRNN**

<img width="350" height="350" alt="final_comparison_chart" src="https://github.com/user-attachments/assets/5e61b8dd-469e-4f29-8aed-2e6dcaf37234" />

---
**Training and Testing Accuracy&Loss**

<img width="350" height="350" alt="training_plot" src="https://github.com/user-attachments/assets/9d24dfe1-4adb-4989-bb3a-6623cc21fadf" />

---

**if you occur any query just mail**
<p>
  <a href="mailto:abishekofficial204@gmail.com?subject=System%20Project%20Inquiry">
    Send Email
  </a>
</p>

