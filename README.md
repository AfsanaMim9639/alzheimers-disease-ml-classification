# Alzheimer's Disease Classification using Novel ML Algorithm

An independent research project implementing and comparing multiple 
machine learning models for early Alzheimer's disease diagnosis.

## Overview

This project applies supervised machine learning algorithms to a 
clinical dataset of 2,149 patients to predict Alzheimer's disease 
diagnosis. A novel feature-weighted KNN model is proposed and 
benchmarked against standard ML methods.

## Dataset

- **Source:** [Kaggle — Alzheimer's Disease Dataset](https://www.kaggle.com/datasets/rabieelkharoua/alzheimers-disease-dataset)
- **Patients:** 2,149
- **Features:** 35 clinical features
- **Target:** Alzheimer's diagnosis (0 = No, 1 = Yes)

## Models Implemented

| Model | Accuracy (%) |
|---|---|
| Random Forest | 92.82 |
| Decision Tree | 88.76 |
| Support Vector Machine (SVM) | 85.77 |
| Logistic Regression | 84.77 |
| Naive Bayes | 83.04 |
| **Proposed Weighted KNN** | **74.93** |
| KNN (standard) | 74.80 |

## Methodology

- 10-Fold Cross Validation
- Feature Engineering (Age × BMI, Cognitive Score)
- StandardScaler Normalization (mean=0, std=1)
- Hyperparameter Tuning (GridSearchCV)

## Proposed Model

A modified KNN using a feature-weighted distance function:

d(x, x') = √[ Σ(xᵢ − x'ᵢ)² · kᵢ ] / √[ Σkᵢ² ]

Features are weighted by their variance, giving more importance 
to clinically significant variables.

## Tools & Libraries

- Python, Jupyter Notebook (Google Colab)
- scikit-learn, pandas, numpy
- matplotlib, seaborn, scipy

## Author

**Afsana Mim**  
Independent Researcher | AI & ML  
Dhaka, Bangladesh  
[GitHub](https://github.com/AfsanaMim9639) | afsanamim9639@gmail.com
