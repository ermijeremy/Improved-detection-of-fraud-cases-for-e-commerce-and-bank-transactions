# 🧠 Fraud Detection and Explainability using Machine Learning

This project focuses on building a robust fraud detection pipeline using real-world financial transaction data. We explore data analysis, feature engineering, modeling, evaluation, and explainability with SHAP to detect fraudulent transactions effectively.

---

## 📌 Project Objectives

- Build a clean, enriched dataset combining user transactions and geolocation data.
- Engineer informative features to improve fraud prediction.
- Develop, train, and evaluate machine learning models to detect fraudulent behavior.
- Deploy the model through an API using FastAPI.
- Ensure reproducibility, testing, and documentation best practices.

---

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

