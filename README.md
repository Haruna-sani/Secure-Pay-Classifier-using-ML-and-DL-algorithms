# Secure-Pay-Classifier-using-ML-and-DL-algorithms
This project leverages both **Machine Learning (ML)** and **Deep Learning (DL)** techniques to detect fraudulent credit card transactions. The dataset was imbalanced, so appropriate resampling strategies were applied to ensure fair model training and evaluation.

---

## 📊 Dataset Handling

- **Problem**: Highly imbalanced dataset (fraud cases are rare).
- **Solution**:
  - Applied **SMOTE (Synthetic Minority Over-sampling Technique)** for ML models to balance class distribution.
  - Used **class weighting** for DL models to penalize misclassification of minority classes more heavily.

---
## 🤖 Models Implemented

### Machine Learning Models
- Random Forest (RF)
- XGBoost
- LightGBM
- **Ensemble Model**: Combination of RF + XGBoost + LightGBM

### Deep Learning Models
- Artificial Neural Network (ANN)
- Long Short-Term Memory (LSTM)
- Bidirectional LSTM (Bi-LSTM)

---

## 📈 Model Performance

| Model       | Accuracy | Precision | Recall | AUC-ROC |
|-------------|----------|-----------|--------|---------|
| **ANN**     | 97.00%   | 52%       | 94%    | 0.4869  |
| **LSTM**    | 99.78%   | 72%       | 92%    | 0.4983  |
| **Bi-LSTM** | 99.49%   | 62%       | 94%    | 0.4963  |
| **RF**      | 99.79%   | 72%       | 93%    | 0.9276  |
| **XGBoost** | 99.87%   | 79%       | 94%    | 0.9382  |
| **LightGBM**| 99.87%   | 80%       | 94%    | 0.9383  |
| **Ensemble**| 99.95%   | 98%       | 89%    | 0.8877  |

---

## 🏆 Comparative Analysis

- **Deep Learning Models** showed good recall (≥ 92%) but relatively lower AUC-ROC scores, indicating weaker discriminatory power.
- **ANN**, while achieving high recall (94%), suffered from low precision (52%) and AUC (0.4869).
- **LSTM** and **Bi-LSTM** both had excellent accuracy but again underperformed in terms of AUC-ROC, suggesting potential overfitting or poor model generalization in this binary classification task.
- Among ML models:
  - **LightGBM** emerged as the **best single model**, achieving:
    - Accuracy: **99.87%**
    - Precision: **80%**
    - Recall: **94%**
    - AUC-ROC: **0.9383**
  - **XGBoost** followed closely with nearly identical results.
- The **Ensemble Model** combining RF, XGBoost, and LightGBM:
  - Achieved the **highest accuracy (99.95%)** and **precision (98%)**, suggesting minimal false positives.
  - Slight drop in recall (89%) and AUC-ROC (0.8877), indicating a trade-off between detecting more frauds and reducing false alarms.

---

## ✅ Conclusion

- For **high-precision fraud detection**, the **Ensemble Model** is the top choice.
- For a balance between **recall and generalization**, **LightGBM** or **XGBoost** offer strong performance.
- Deep learning models may require further tuning or hybrid architectures to compete with advanced ML techniques in this task.

# Data Source: https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud
---


