# 🕵️‍♂️ Fraud Detection and IP-Based Country Enrichment

This project is part of the 10 Academy KAIM Week 8–9 challenge. It focuses on building a data-driven fraud detection pipeline using historical transaction data and enriching it with geolocation information derived from IP address ranges. 

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

## 📌 Project Objectives

- Build a clean, enriched dataset combining user transactions and geolocation data.
- Engineer informative features to improve fraud prediction.
- Develop, train, and evaluate machine learning models to detect fraudulent behavior.
- Deploy the model through an API using FastAPI.
- Ensure reproducibility, testing, and documentation best practices.

---