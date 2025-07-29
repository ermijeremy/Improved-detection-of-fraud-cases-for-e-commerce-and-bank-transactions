# 🧠 Fraud Detection and Explainability using Machine Learning

This project focuses on building a robust fraud detection pipeline using real-world financial transaction data. We explore data analysis, feature engineering, modeling, evaluation, and explainability with SHAP to detect fraudulent transactions effectively.

## 📌 Project Overview

Financial fraud is a major issue in the digital world. This project aims to:

- Detect fraudulent transactions using supervised machine learning techniques.
- Handle imbalanced data using SMOTE.
- Engineer insightful features like transaction time, frequency, velocity, and time since signup.
- Compare models (Logistic Regression vs Random Forest) based on classification metrics.
- Use SHAP (SHapley Additive Explanations) to interpret the model and build trust in predictions.

The work is divided into 3 major tasks:

- **Task 1: Data Analysis and Feature Engineering**
- **Task 2: Modeling, Evaluation, and Comparison**
- **Task 3: Explainability with SHAP**

---
---
## 📌 Project Objectives

- Build a clean, enriched dataset combining user transactions and geolocation data.
- Engineer informative features to improve fraud prediction.
- Develop, train, and evaluate machine learning models to detect fraudulent behavior.
- Deploy the model through an API using FastAPI.
- Ensure reproducibility, testing, and documentation best practices.

---

## Model Comparison

| Metric               | Linear Regression | Random Forest | Winner | Key Insight                                   |
|----------------------|-------------------|---------------|--------|-----------------------------------------------|
| **Accuracy**         | 57.49%           | 95.16%        | RF     | RF dominates due to ensemble learning.        |
| **Precision (Class 1)** | 0.09          | 0.91          | RF     | RF correctly predicts 91% of class `1` (vs. 9% for LR). |
| **Recall (Class 1)**    | 0.41          | 0.54          | RF     | RF captures 54% of class `1` (vs. 41% for LR). |
| **F1-Score (Class 1)**  | 0.15          | 0.68          | RF     | RF’s balance between precision/recall is 4.5x better. |
| **AUC-ROC**            | 0.50          | 0.77          | RF     | RF distinguishes classes; LR performs at random. |
| **Confusion Matrix (Class 1)** | 1170 TP, 1680 FN | 1549 TP, 1301 FN | RF | RF has **higher TP** and **lower FN**. |
| **R² Score**           | -3.98         | 0.43          | RF     | LR is worse than a baseline model.            |

### Key Takeaways
1. **Random Forest outperforms Linear Regression** in all classification metrics.
2. **LR is unsuitable for this classification**.
3. **SMOTE improves minority class detection**, but RF benefits more due to non-linear splits.



## 🛠 Project Structure

fraud-detection-project/
│
├── data/  
│ ├── fraud.csv  
│ └── ipAddress_to_country.csv  
│
├── notebooks/  
│ ├── 1.0_analysis.ipynb # EDA and Feature Engineering  
│ ├── 2.0_modeling.ipynb # Modeling and Evaluation  
│ └── 3.0_explainability.ipynb # SHAP-based Explainability  
├──src/  
├── requirements.txt   
├── README.md  
└── .gitignore  


---

## ⚙️ Environment Setup

### 📦 Install Python Packages

# Clone the repo
git clone https://github.com/ermijeremy/Improved-detection-of-fraud-cases-for-e-commerce-and-bank-transactions.git

cd fraud-detection-project

# Create a virtual environment
python -m venv venv
source venv/source/activate  

# Install dependencies
pip install -r requirements.txt

