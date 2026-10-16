# Heart Disease Prediction System 🫀

A machine learning-based web application for predicting the likelihood of heart disease based on patient clinical parameters. This project compares multiple ML algorithms and deploys the best-performing model through an interactive GUI.

![Python](https://img.shields.io/badge/Python-3.12-blue)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.5-orange)
![License](https://img.shields.io/badge/License-MIT-green)

---

## 📋 Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Dataset](#dataset)
- [Machine Learning Models](#machine-learning-models)
- [Model Performance](#model-performance)
- [Installation](#installation)
- [Usage](#usage)
- [GUI Application](#gui-application)
- [Project Structure](#project-structure)
- [Technologies Used](#technologies-used)
- [Disclaimer](#disclaimer)

---

## 🔍 Overview

This project implements an end-to-end machine learning pipeline to predict heart disease presence using the **UCI Heart Disease Dataset**. It covers:

- Data preprocessing & cleaning
- Exploratory data analysis
- Categorical encoding & feature scaling
- Training and evaluating **6 different ML models**
- Comparing model accuracy
- Deploying the best model (Random Forest) into a **Tkinter-based GUI** with PDF receipt generation and Excel record-keeping

---

## ✨ Features

- 🧹 **Data Preprocessing** — Handles missing values, duplicates, categorical encoding, and feature scaling
- 🤖 **Multiple ML Models** — Logistic Regression, SVM, KNN, Decision Tree, Random Forest, Gradient Boosting
- 📊 **Model Comparison** — Visual bar chart comparing accuracy across all models
- 🖥️ **Interactive GUI** — Modern dark-themed Tkinter interface with animated radar scan
- 📄 **PDF Receipt Generation** — Auto-generates a patient report in PDF format
- 📊 **Excel Logging** — Automatically saves every prediction into `patient_records.xlsx`
- 🎯 **Real-time Prediction** — Instant prediction with confidence score

---

## 📊 Dataset

The project uses the **UCI Heart Disease Dataset** (`heart.csv`) with **14 clinical features**:

| Feature | Description |
|---------|-------------|
| `age` | Age of the patient |
| `sex` | Gender (1 = Male, 0 = Female) |
| `cp` | Chest pain type (0–3) |
| `trestbps` | Resting blood pressure |
| `chol` | Serum cholesterol (mg/dl) |
| `fbs` | Fasting blood sugar > 120 mg/dl |
| `restecg` | Resting ECG results (0–2) |
| `thalach` | Maximum heart rate achieved |
| `exang` | Exercise-induced angina |
| `oldpeak` | ST depression induced by exercise |
| `slope` | Slope of peak exercise ST segment |
| `ca` | Number of major vessels (0–4) |
| `thal` | Thalassemia (1–3) |
| `target` | Heart disease (0 = No, 1 = Yes) |

**Total samples:** 302 (after removing duplicates)

---

## 🤖 Machine Learning Models

Six classification algorithms were trained and evaluated:

1. **Logistic Regression (LR)**
2. **Support Vector Machine (SVM)**
3. **K-Nearest Neighbors (KNN)** — with hyperparameter tuning (k = 1–39)
4. **Decision Tree (DT)**
5. **Random Forest (RF)** ⭐
6. **Gradient Boosting Classifier (GB)**

---

## 📈 Model Performance

| Model | Accuracy |
|-------|----------|
| Logistic Regression | 78.69% |
| Support Vector Machine | 80.33% |
| K-Nearest Neighbors | 63.93% |
| Decision Tree | 72.13% |
| **Random Forest** 🏆 | **85.25%** |
| Gradient Boosting | 81.97% |

**Best Model:** Random Forest with **85.25% accuracy** — saved as `Best_Heart_Diseases_Predict_Model` via `joblib`.

---

## ⚙️ Installation

### 1. Clone the repository
```bash
git clone https://github.com/your-username/heart-disease-prediction.git
cd heart-disease-prediction
```

### 2. Install dependencies
```bash
pip install pandas numpy scikit-learn matplotlib seaborn joblib pillow fpdf openpyxl
```

### 3. Ensure the model file exists
Make sure `Best_Heart_Diseases_Predict_Model` and `heart.csv` are in the project root.

---

## 🚀 Usage

### Run the Jupyter Notebook
Open `Heart_Diseases_Prediction_Using_Machine_Learning.ipynb` to:
- Explore data preprocessing steps
- Train and compare all 6 models
- View accuracy comparison chart

### Run the GUI Application
```bash
python app.py
```

---

## 🖥️ GUI Application

The Tkinter GUI provides a modern, user-friendly interface:

### Features
- 🌑 **Dark-themed UI** with custom heart graphic
- 📝 **13 input fields** for patient clinical parameters
- 🔄 **Animated radar scan** during prediction
- ✅ **Instant result display** with confidence/risk score
- 📄 **PDF receipt** auto-saved in `receipts/` folder
- 📊 **Excel record logging** in `patient_records.xlsx` (disease cases highlighted in red)
- 🔁 **Reset button** to clear the form

### Screenshot
```
┌─────────────────────────────────────────────────────┐
│  ❤️  Heart Diseases Prediction System               │
│     AI-assisted cardiac risk screening              │
├──────────────────────────────┬──────────────────────┤
│  Patient Name: [__________]  │   SCAN MONITOR       │
│                              │      ⭕              │
│  Age:        [__]            │    (radar)           │
│  Sex:        [__]            │                      │
│  CP:         [__]            │   Ready to scan      │
│  ... (13 fields)             │                      │
├──────────────────────────────┴──────────────────────┤
│  [PREDICT] [PRINT RECEIPT] [SAVE EXCEL] [RESET]     │
└─────────────────────────────────────────────────────┘
```

---

## 📁 Project Structure

```
heart-disease-prediction/
│
├── Heart_Diseases_Prediction_Using_Machine_Learning.ipynb  # Main notebook
├── app.py                                                  # GUI application
├── heart.csv                                               # Dataset
├── Best_Heart_Diseases_Predict_Model                       # Trained RF model (joblib)
├── patient_records.xlsx                                    # Auto-generated Excel log
├── receipts/                                               # Auto-generated PDF receipts
└── README.md
```

---

## 🛠️ Technologies Used

| Category | Tools |
|----------|-------|
| **Language** | Python 3.12 |
| **Data Handling** | Pandas, NumPy |
| **ML Framework** | scikit-learn |
| **Visualization** | Matplotlib, Seaborn |
| **GUI** | Tkinter, Pillow (PIL) |
| **PDF Generation** | FPDF |
| **Excel Logging** | openpyxl |
| **Model Persistence** | Joblib |

---

## ⚠️ Disclaimer

> **This project is for educational and research purposes only.**  
> The predictions made by this system are based on a machine learning model trained on a limited dataset and should **NOT** be considered as professional medical advice.  
> Always consult a **qualified cardiologist** for accurate diagnosis and treatment.

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!  
Feel free to fork the repo and submit a pull request.

---

## 📜 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/heart+disease) for the dataset
- scikit-learn community for excellent ML tools
- Open-source contributors of Tkinter, FPDF, and openpyxl

---

⭐ **If you found this project helpful, please give it a star!** ⭐
