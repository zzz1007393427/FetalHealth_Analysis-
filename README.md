# Fetal Health Classification Using Machine Learning

## Project Overview

This project applies multiple machine learning models to classify fetal health conditions using cardiotocography (CTG) data. The main goal is to predict whether a fetal condition is classified as Normal, Suspect, or Pathological based on clinical monitoring measurements.

The project compares several machine learning approaches and evaluates their performance using multiple classification metrics.

---

## Dataset

The dataset used in this project is the **Fetal Health Classification Dataset** from Kaggle.

- Number of observations: 2,126
- Number of predictors: 21
- Outcome classes:
  - Normal
  - Suspect
  - Pathological

The predictors include fetal heart rate characteristics, variability measurements, accelerations, decelerations, uterine contractions, and histogram-based features.

Dataset source:  
https://www.kaggle.com/datasets/andrewmvd/fetal-health-classification

---

## Methods

The following machine learning models were implemented and compared:

- K-Nearest Neighbors (KNN)
- Multinomial Logistic Regression
- Random Forest
- Gradient Boosting Machine (GBM)
- Neural Network

To improve classification performance for minority classes, SMOTE (Synthetic Minority Over-sampling Technique) was applied to the training data.

Model performance was evaluated using:

- Accuracy
- Macro F1-score
- Multiclass AUC
- Cross-Validated F1-score

---

## Main Findings

Among all models, Gradient Boosting and Random Forest achieved the strongest overall performance.

Key findings include:

- Tree-based ensemble methods outperformed linear models
- Gradient Boosting achieved the best overall Macro F1-score
- Random Forest achieved the highest AUC
- Pathological fetal cases were classified with high accuracy

Feature importance analysis showed that fetal heart rate variability and prolonged decelerations were among the most important predictors.

---

## Repository Structure

```text
├── data/
│   └── fetal_health.csv
│
├── code/
│   └── ml_report_revised.Rmd
│
├── figures/
│   ├── confusion_matrix/
│   ├── feature_importance/
│   └── model_performance/
│
│
└── README.md
