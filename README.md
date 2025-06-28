# 🧠 Alzheimer’s Disease Prediction Using Machine Learning
## 📌 Introduction
Alzheimer’s Disease (AD) is a progressive neurodegenerative condition affecting memory, behavior, and cognitive functions. Early detection is critical for timely intervention, and machine learning offers powerful tools for predictive modeling in healthcare.

This project applies supervised machine learning to predict Alzheimer’s Disease diagnosis using structured patient data, including demographic, clinical, lifestyle, and cognitive assessment variables.

## 📊 Dataset Overview
Source: (Kaggle)[https://www.kaggle.com/datasets/rabieelkharoua/alzheimers-disease-dataset/data]

Size: 2,419 patient records

Features:

Demographics: Age, Gender, Ethnicity, Education

Lifestyle: BMI, smoking, alcohol, sleep, diet

Medical History: Diabetes, depression, head injury, hypertension, family history

Clinical Measurements: Blood pressure, cholesterol

Cognitive Assessments: MMSE, ADL, Functional Assessment, Memory & Behavior indicators

Symptoms: Confusion, disorientation, forgetfulness

## 📈 Exploratory Data Analysis (EDA)

Analyzed class balance between AD vs non-AD.

Identified outliers using IQR rules.

Visualized feature separation across diagnosis classes.

Revealed 5 top predictive features:

Functional Assessment
ADL (Activities of Daily Living)
MMSE (Mini-Mental State Exam)
Memory Complaints
Behavioral Problems

## 🛠️ Feature Selection & Modeling : Random Forest and Lasso Regression both pointed to the same top 5 features.

Algorithms Used:

**Logistic Regression (L1 & L2)**

**Gaussian Naïve Bayes**

**k-Nearest Neighbors (k=3, 5, 7)**

**Random Forest (varied trees & depths)**

**SVM (linear & RBF, C={0.1, 1, 10})**


## Models tuned using GridSearchCV with 5-fold stratified cross-validation.
## ⚖️ Handling Class Imbalance

Used **Balanced Random** Forest with 100 trees

Training with 70/30 stratified split

Achieved 95% accuracy on test set

## 🔍 Model Interpretation with SHAP
Used **SHAP** to explain why the model predicted AD:

Top global SHAP values:

Functional Assessment (0.184)

ADL (0.172)

Memory Complaints (0.117)

MMSE (0.093)

Behavioral Problems (0.083)

These insights confirm:

Functional and behavioral data are key to diagnosis

Age, vitals, and demographics were less informative

## ✅ Key Findings
**Random Forest and SVM** outperformed linear models.

Feature importance and SHAP consistently highlighted the same 5 features.

Behavioral and cognitive self-assessment data are most predictive.

Clinically interpretable models can support early, explainable detection of Alzheimer’s.
