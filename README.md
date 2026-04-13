# 🧠 Hyperthyroidism Prediction with Machine Learning

> A clinical data analysis project that uses Machine Learning to predict hyperthyroidism, supporting early diagnosis in healthcare settings.

---

## 📌 Project Overview

This project simulates a real-world healthcare data science scenario. Using a clinical dataset with patient information, I built and evaluated predictive classification models capable of identifying hyperthyroidism cases based on lab results and medical indicators.

The goal was to apply the full data science pipeline — from raw data to a validated model — in a context where early detection has real clinical impact.

---

## 🎯 Objectives

- Perform in-depth Exploratory Data Analysis (EDA) on clinical data
- Handle missing values and categorical variables appropriately
- Apply preprocessing and feature engineering techniques
- Build and compare classification models
- Evaluate model performance with relevant healthcare metrics

---

## 🗂️ Dataset

The dataset contains patient clinical records, including:

| Feature | Description |
|---|---|
| Age | Patient age |
| Sex | Biological sex |
| Lab results | Hormone levels (TSH, T3, T4, etc.) |
| Medical indicators | Clinical flags and binary diagnostic markers |

> Source: UCI Machine Learning Repository — Thyroid Disease Dataset

---

## ⚙️ Tech Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557c?style=for-the-badge)
![Seaborn](https://img.shields.io/badge/Seaborn-4c9be8?style=for-the-badge)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

---

## 🔎 Project Pipeline

### 1. Exploratory Data Analysis (EDA)
- Distribution analysis for numerical and categorical features
- Class imbalance detection
- Correlation heatmap between clinical variables
- Identification of the most predictive features

### 2. Preprocessing
- Missing value imputation
- Label encoding for categorical variables
- Feature standardization with `StandardScaler`
- Train/test split with stratification to preserve class balance

### 3. Modeling
Multiple classification algorithms were tested and compared:
- Logistic Regression (baseline)
- Decision Tree
- **Random Forest** ← selected model
- K-Nearest Neighbors

### 4. Evaluation

The final model was assessed using classification metrics appropriate for healthcare use cases, where false negatives are costly:

| Metric | Score |
|---|---|
| Accuracy | ~99.4% |
| Precision | ~98.6% |
| Recall | ~99.6% |
| F1-Score | ~99.1% |

> The **Random Forest** classifier was selected as the final model due to its superior performance on recall and F1-score — critical metrics when the cost of missing a positive case is high.

---

## 📊 Results

The Random Forest model demonstrated outstanding performance on the test set:

- **484** true positives and **42** true negatives
- Only **1** false negative and **2** false positives
- Near-perfect recall — critical in a medical screening context where missing a diagnosis is the costliest error

![Confusion Matrix](images/model_results.png)

---

## 🚀 How to Run

```bash
# Clone the repository
git clone https://github.com/hGALANTp/Project_hypothyroid.git

# Navigate to the project folder
cd Project_hypothyroid

# Install dependencies
pip install -r requirements.txt

# Launch the notebook
jupyter notebook
```

---

## 📁 Project Structure

```
Project_hypothyroid/
│
├── Data/                        # Raw and processed datasets
├── Analise_Hipertiroidismo.ipynb  # Main analysis notebook
├── requirements.txt             # Python dependencies
└── README.md                    # Project documentation
```

---

## 💡 Key Learnings

- Clinical datasets often have significant class imbalance — handling it correctly is critical for model reliability
- Recall matters more than accuracy in medical screening: a missed diagnosis is more harmful than a false alarm
- Feature selection based on domain knowledge (endocrinology) improved model interpretability

---

## 👤 Author

**Helton Galant**
Data Scientist | Python · Machine Learning · Finance Background

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/helton-galant)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/hGALANTp)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).