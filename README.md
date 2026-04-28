# Heart Failure Detection with Machine Learning

End-to-end machine learning project for predicting heart failure using clinical and ECG data.

---

## Project Summary

This project applies machine learning techniques to a biomedical dataset in order to classify patients into:

- **0 → No Heart Failure**
- **1 → Heart Failure**

The focus was on building models that not only achieve high accuracy, but also **generalize well** and prioritize **patient safety (high recall)**.

---

## Key Results

- **Best Model:** Support Vector Machine (RBF Kernel, C=10)  
- **Test Accuracy:** 100%  
- **Cross-Validation Accuracy:** ~95.8%  
- **Recall (Heart Failure):** 100%  

> The model successfully identifies all heart failure cases, minimizing false negatives — a critical requirement in healthcare.

---

## Approach

### Data Preparation
- Converted multi-class labels into binary classification
- Stratified 80/20 train-test split
- Balanced dataset (50/50 classes)
- No missing values

---

### Models Implemented
- Random Forest
- XGBoost (with GridSearchCV tuning)
- Support Vector Machines (Linear & RBF)
- Voting Classifier (ensemble of SVM, RF, XGBoost)

---

### Model Optimization
- Hyperparameter tuning (GridSearchCV)
- 10-fold cross-validation
- Overfitting detection & mitigation
- Evaluation metrics:
  - Accuracy
  - Precision / Recall
  - F1-score
  - Cross-validation stability

---

### Feature Engineering
Tested interaction features:
- `EF / GLS`
- `QRS / GLS`

**Key Insight:**  
Simpler feature sets (EF + QRS) performed equally well → improved interpretability without loss of performance.

---

## 📊 Model Performance

| Model              | Test Accuracy | CV Accuracy | Notes |
|-------------------|--------------|------------|------|
| Random Forest      | 95.8%        | 96.7%      | Stable after tuning |
| XGBoost (tuned)    | 95.8%        | 96.7%      | Improved generalization |
| **SVM (RBF)**      | **100%**     | 95.8%      | Best overall model |

---

## Tech Stack

- Python
- Scikit-learn
- XGBoost
- Pandas, NumPy
- Matplotlib, Seaborn

---

## Project Structure


├── data/
├── notebooks/
├── src/
├── models/
├── README.md
└── requirements.txt


---

## Key Takeaways

- Simpler models can outperform complex ones when features are informative  
- Cross-validation is essential for reliable performance evaluation  
- In healthcare applications, **recall is more important than accuracy**  
- Ensemble methods improve robustness but may not always outperform the best single model  

---
  
## Disclaimer

This project is for educational and research purposes only and is not intended for clinical use.
