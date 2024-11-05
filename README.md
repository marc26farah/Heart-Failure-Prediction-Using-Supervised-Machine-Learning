# Heart Failure Prediction Using Supervised Machine Learning

## Project Overview

This project focuses on using machine learning models to predict heart failure based on clinical records. The study compares the performance of five models using various scaling techniques and feature sets to determine the best-performing model.

---

## Literature Review

Heart Failure (HF) is a significant global health concern affecting millions, with predictive models offering potential for early diagnosis. Prior studies demonstrated varied success using machine learning, with accuracy levels ranging from 54% to 89%, depending on model type and tuning.

---

## Dataset

The dataset consists of 299 records and 13 features, including:
- **Numerical Features**: age, creatinine phosphokinase, ejection fraction, platelets, serum creatinine, serum sodium, and time
- **Categorical Features**: anemia, diabetes, high blood pressure, sex, and smoking

The target variable, "Death Event," is binary.

### Preprocessing
- No missing values, duplicates, or outliers were found.
- Numerical and categorical features were analyzed for distribution and correlation.

---

## Methodology

The dataset was split into training (80%) and testing (20%) sets. Four dataset variations were created by scaling (Standard/MinMax) and feature selection. Each model was trained on these variations, and hyperparameters were optimized using grid search and 5-fold cross-validation.

### Models Analyzed
1. **K-Nearest Neighbors (KNN)**: Achieved an accuracy of 83.33% with an optimal parameter of 8 neighbors.
2. **Decision Tree (DT)**: Showed low performance with an accuracy around 72%.
3. **Random Forest (RF)**: Highest accuracy of 88%, best performance with MinMax scaling.
4. **Support Vector Machine (SVM)**: Accuracy peaked at 87% with Standard Scaling.
5. **Logistic Regression (LR)**: Accuracy around 85%, with no significant impact from scaling or feature removal.

---

## Results

| Model         | Accuracy | Recall | F1 Score |
|---------------|----------|--------|----------|
| KNN           | 0.83     | 0.72   | 0.72     |
| Decision Tree | 0.72     | 0.67   | 0.59     |
| Random Forest | 0.88     | 0.83   | 0.81     |
| SVM           | 0.87     | 0.72   | 0.76     |
| Logistic Reg. | 0.85     | 0.67   | 0.73     |

---

## Discussion

Random Forest showed the highest performance, particularly with MinMax scaling and full feature sets. Decision Tree performed the poorest, likely due to its simplicity. Feature scaling had minimal impact across models, with slight improvements when irrelevant features were removed.

---

## Conclusion

The Random Forest classifier is the most effective for heart failure prediction in this dataset, providing robust results across all performance metrics. Future work could explore ensemble methods or advanced neural networks for potentially better outcomes.
