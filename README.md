# MIS 382N: Advanced Machine Learning - Assignment 5

**Course:** MIS 382N: Advanced Machine Learning  
**Student:** Zan Merrill (UT EID: ahm2452)  
**Due:** November 21st, 2025  
**Total Points:** 75

## Overview

This assignment covers two fundamental areas of machine learning: implementing linear models from scratch and comparing ensemble methods for classification. The work demonstrates both theoretical understanding and practical implementation of advanced ML techniques.

## Assignment Structure

### Question 1: Logistic Regression Implementation (30 pts)
Implements logistic regression from scratch using NumPy on a synthetic dataset generated from two isotropic Gaussians.

**Topics covered:**
- Sigmoid activation function
- Gradient descent optimization with L2 regularization
- Loss computation (binary cross-entropy)
- Decision boundary visualization
- Rejection region analysis
- Model interpretation and coefficient analysis

**Key implementations:**
- `sigmoid()`: Computes sigmoid activation
- `gradients()`: Calculates gradients for weights and bias
- `train_logreg()`: Full batch gradient descent training loop
- `predict_label()`: Classification with threshold
- `plot_boundary()`: Decision boundary visualization

**Key findings:**
- Learned parameters align with synthetic data generation process
- Weight coefficients correctly indicate positive relationship with Class 1
- Rejection region derived using inverse sigmoid (logit) function

### Question 2: Ensemble Methods for Classification (35 pts)
Compares various ensemble techniques on a real classification dataset using scikit-learn and XGBoost.

**Methods compared:**
1. **Decision Tree Classifier** - Single decision tree baseline
2. **Bagging** - Bootstrap aggregating with 10 decision tree estimators
3. **Random Forest** - Bagging with random feature subsets at each split
4. **AdaBoost** - Sequential boosting with adaptive weighting
5. **XGBoost** - Gradient boosting framework with regularization

**Hyperparameter tuning:**
- Decision Tree: `max_depth`, `min_samples_split`, `min_samples_leaf`
- Random Forest: `n_estimators`, `max_depth`, `min_samples_leaf`, `bootstrap`
- AdaBoost & XGBoost: `n_estimators`, `learning_rate`, `max_depth`

**Evaluation metrics:**
- Accuracy Score
- ROC-AUC Score (for probability-based evaluation)

**Key findings:**
- Ensemble methods generally outperform single decision trees
- XGBoost and AdaBoost achieve best performance
- Ensemble methods improve both accuracy and ROC-AUC

### Question 3: Ensemble Conceptual Questions (10 pts)
Theoretical analysis of ensemble methods.

**Topics:**
1. **Boosting sensitivity to outliers** - How sequential boosting can be distorted by outlier residuals
2. **Random Forest randomness sources** - Bootstrap sampling and random feature subsets

## Repository Structure

```
aml_hw5/
├── notebooks/
│   └── HW5.ipynb           # Main assignment notebook with all code and analysis
├── data/
│   └── hw5_data.csv        # Classification dataset used in Q2
└── README.md               # This file
```

## Key ML Techniques

### Logistic Regression
- Linear classification model with sigmoid activation
- Parametric model with interpretable weights
- Gradient descent optimization with L2 regularization

### Ensemble Methods
- **Bagging**: Reduces variance through averaging
- **Random Forest**: Decorrelates trees using feature randomness
- **AdaBoost**: Sequential boosting with sample weight adjustment
- **XGBoost**: Gradient boosting with regularization and pruning

## Files

- `notebooks/HW5.ipynb` - Complete Jupyter notebook with all implementations, visualizations, and analysis
- `data/hw5_data.csv` - Dataset for Q2 classification tasks
- `README.md` - This documentation

## Running the Code

1. Navigate to the notebooks directory
2. Open `HW5.ipynb` in Jupyter Notebook
3. The notebook contains all necessary code cells with clear sections for each question
4. Data is loaded from `../data/hw5_data.csv`

## Academic Integrity

ChatGPT was used in accordance with class policy (MIS 382N).

---

*Last updated: February 2026*
