# Chronic Kidney Disease (CKD) Stage Prediction

## Project Overview

This project focuses on predicting Chronic Kidney Disease (CKD) stages using clinical and demographic features through a multi-class classification approach.

The project compares different machine learning algorithms and investigates the impact of including or excluding two important kidney-related markers: **Serum Creatinine** and **eGFR**.

## Project Objectives

- Predict CKD stages using clinical and demographic data.
- Compare the performance of multiple machine learning models.
- Investigate the impact of Serum Creatinine and eGFR on classification performance.
- Evaluate models using Accuracy, Macro Recall, and Macro F1-score.

## Dataset

**Source:** [Chronic Kidney Disease (CKD) Clinical Dataset – Kaggle](https://www.kaggle.com/datasets/priyankabarik/chronic-kidney-disease-ckd-clinical-dataset)

The dataset contains clinical measurements and patient-related features.

The target variable contains five classes:

- Healthy Kidney
- Mild CKD (Stage 1–2)
- Moderate CKD (Stage 3)
- Severe CKD (Stage 4)
- Kidney Failure (Stage 5)

## Experiments

Two feature configurations were evaluated:

**Experiment 1: Without Kidney Markers**
- Excluded Serum_Creatinine.
- Excluded eGFR.
- Used the remaining features.

**Experiment 2: With All Features**
- Included all available features, including Serum_Creatinine and eGFR.

Both experiments used the same stratified training and validation split to ensure a fair comparison.

## Machine Learning Models

The following algorithms were evaluated:

- Decision Tree
- Random Forest
- Support Vector Machine (SVM)
- K-Nearest Neighbors (KNN)

## Data Preprocessing

- Separated input features from the target variable.
- Encoded binary categorical features.
- Applied feature scaling using StandardScaler for SVM and KNN.
- Used stratified splitting to preserve class proportions.
- Used balanced class weights for Decision Tree, Random Forest, and SVM.

## Validation Results

| Experiment | Model | Accuracy | Macro Recall | Macro F1 |
|---|---|---:|---:|---:|
| Without kidney markers | Decision Tree | 1.000 | 1.000 | 1.000 |
| Without kidney markers | Random Forest | 1.000 | 1.000 | 1.000 |
| Without kidney markers | SVM | 1.000 | 1.000 | 1.000 |
| Without kidney markers | KNN | 0.996 | 0.994 | 0.996 |
| With all features | Decision Tree | 1.000 | 1.000 | 1.000 |
| With all features | Random Forest | 1.000 | 1.000 | 1.000 |
| With all features | SVM | 1.000 | 1.000 | 1.000 |
| With all features | KNN | 0.999 | 0.998 | 0.999 |

*Note: These are the observed validation results. The unusually high scores require further investigation for potential data leakage, feature-target relationships, and dataset overlap before drawing conclusions about generalization.*

## Repository Contents

- `CKD Notebook.ipynb`: Data analysis, preprocessing, model training, and evaluation.
- `training ckd dataset.csv`: Training dataset.
- `testing ckd dataset.csv`: Testing dataset.

## Technologies Used

- Python
- Pandas
- Scikit-learn
- StandardScaler
- Decision Tree
- Random Forest
- Support Vector Machine
- K-Nearest Neighbors

## Important Disclaimer

This project is developed for educational and machine learning practice purposes only. It is not intended to provide medical diagnoses or replace professional medical evaluation.

## Author

**Farah Hewedy**

[GitHub Profile](https://github.com/FarahHewedy)
