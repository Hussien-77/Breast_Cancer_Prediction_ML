# 🧬 Breast Cancer Wisconsin (Diagnostic) EDA & Predictive Modeling

This project performs a complete **Exploratory Data Analysis (EDA)**, **data preprocessing**, and **machine learning modeling pipeline** on the **Breast Cancer Wisconsin (Diagnostic)** dataset.  
The goal is to predict whether a tumor is **benign (B)** or **malignant (M)** based on cell nucleus measurements.

---

## 📁 Dataset

- **Source:** https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data
- **File:** `data.csv`
- **Samples:** 569
- **Features:** 30 numeric features + diagnosis label (`M` or `B`)

Each record describes characteristics of the cell nuclei present in an image of a fine needle aspirate (FNA) of a breast mass.

---

## ⚙️ Project Workflow

### 1. **Data Exploration (EDA)**
- Inspected dataset structure, data types, and missing values  
- Analyzed class distribution (Malignant vs Benign)  
- Examined correlations between numerical features  
- Visualized relationships using histograms, pairplots, and heatmaps  
- Identified most influential features:
  - `concave points_worst`
  - `perimeter_worst`
  - `radius_worst`
  - `area_worst`

### 2. **Data Preprocessing**
- Removed irrelevant columns (`id`, unnamed columns)
- Encoded target variable (`M` → 1, `B` → 0)
- Scaled features using `StandardScaler`
- Split data into train/test sets (80/20)

### 3. **Modeling**
Built and evaluated multiple models using a unified **pipeline**:
- Logistic Regression  
- Random Forest  
- Support Vector Machine (SVM)  
- XGBoost  

Metrics compared:
- Accuracy  
- Precision  
- Recall  
- F1-Score  
- ROC-AUC  

### 4. **Model Selection**
The best model was automatically selected based on the highest **F1-score**, balancing precision and recall.  
Justification and metric visualization are printed dynamically in the notebook.

### 5. **Explainability (SHAP)**
Used **SHAP (SHapley Additive exPlanations)** to interpret model predictions:
- **Global interpretation:** identifies top features influencing the model.  
- **Local interpretation:** explains individual predictions and feature contributions.


## 🧠 Insights
- Tumors with higher **radius**, **perimeter**, and **concavity points** are more likely to be malignant.  
- The dataset is moderately imbalanced (212 malignant vs 357 benign).  
- Tree-based models like Random Forest and XGBoost often perform best on this dataset due to feature interactions.

---

## 🧩 Tools & Libraries
- **Python 3.10+**
- **Pandas**, **NumPy**, **Matplotlib**, **Seaborn**
- **Scikit-learn**
- **XGBoost**
- **SHAP**
- **Joblib** (optional: for model saving)

---

## 🚀 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/<your-username>/breast-cancer-eda-ml.git
   cd breast-cancer-eda-ml
