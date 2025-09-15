# 🩺 Diabetes Risk Predictor (Week 1 Project)

A machine learning pipeline for predicting diabetes outcomes using the **PIMA Indians Diabetes dataset**.  
This project demonstrates best practices in **data preprocessing, hyperparameter tuning, and model evaluation** — serving as a foundation for clinical AI applications.

---

## 🚀 Project Overview
- **Goal**: Predict whether a patient is at risk of diabetes.  
- **Techniques**: End-to-end scikit-learn pipeline with preprocessing, model training, and evaluation.  
- **Dataset**: [PIMA Indians Diabetes Dataset (Kaggle)](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database)  

---

## 🔧 Methods
1. **Preprocessing**
   - Convert invalid zeros → `NaN`
   - Winsorize outliers (Insulin, SkinThickness)
   - Median imputation
   - Robust scaling

2. **Modeling**
   - Logistic Regression
   - Hyperparameter tuning with `GridSearchCV`
   - Stratified 5-fold cross-validation

3. **Evaluation**
   - Confusion Matrix
   - ROC Curve & AUC
   - Precision–Recall analysis
   - Feature importance visualization

---

## 📊 Results
- **Best Model**: Logistic Regression (`C=10`, `penalty=l1`, `solver=liblinear`, `class_weight=balanced`)  
- **Performance**:  
  - Cross-validation F1-score: ~0.69  
  - ROC-AUC: (see plots below)  

*Glucose, BMI, and Age were the most important predictors.*

---

## 📂 Repository Structure
Week_1_Diabetes_Risk_Predictor/
│── diabetes_pipeline.ipynb # main notebook
│── requirements.txt # dependencies
│── README.md # this file
│── .gitignore
│── LICENSE

---

## ⚡ How to Run
Clone the repo and install requirements:

```bash
git clone https://github.com/yourusername/Week_1_Diabetes_Risk_Predictor.git
cd Week_1_Diabetes_Risk_Predictor
pip install -r requirements.txt


Run the notebook or Python script:

jupyter notebook diabetes_pipeline.ipynb


🔮 Future Work

Try advanced models (XGBoost, LightGBM, Neural Networks)

Use SHAP/LIME for explainability

Build a Flask app for real-time predictions

Integrate with EHR systems for clinical deployment
