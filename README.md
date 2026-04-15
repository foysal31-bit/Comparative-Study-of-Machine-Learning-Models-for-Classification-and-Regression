# Comparative Study of Machine Learning Models for Classification and Regression

## Overview
This project presents a comparative analysis of machine learning models applied to both classification and regression problems. The goal is to evaluate model performance, understand data characteristics, and analyze the trade-offs between model complexity, generalization, and interpretability.

Two datasets are used:
- NASA Shuttle dataset (multi-class classification)
- Fish toxicity dataset (regression)

---

## Objectives
- Build and compare multiple machine learning models
- Evaluate performance relative to baseline metrics
- Analyze linear vs nonlinear decision boundaries
- Identify overfitting and generalization behavior
- Interpret model effectiveness across different problem types

---

## Dataset 1: Shuttle Data (Classification)

### Problem
Predict the class label (7 categories) based on numerical features related to system performance.

### Key Steps
- Data preprocessing and train-test split (60–40, stratified)
- Baseline evaluation using No Information Rate (NIR ≈ 79%)
- Exploratory Data Analysis (scatterplots, class means)

### Models Used
- Logistic Regression
- Linear Discriminant Analysis (LDA)
- Support Vector Machine (SVM)
- Multilayer Perceptron (MLP)
- Decision Tree
- Random Forest

### Results Summary
- Logistic Regression: ~97% accuracy  
- LDA: ~94% accuracy  
- SVM: ~99.7% accuracy  
- Decision Tree: ~99.9% accuracy  
- Random Forest: ~99.97% accuracy  

### Key Insights
- Data shows strong class separability
- Nonlinear models significantly outperform linear models
- Random Forest provides the best balance of accuracy and generalization

---

## Dataset 2: Fish Toxicity (Regression)

### Problem
Predict LC50 (toxicity level) using molecular descriptors.

### Key Steps
- Correlation analysis and statistical significance testing
- Train-test split (75–25)
- Model comparison across multiple regression techniques

### Models Used
- Linear Regression
- Polynomial Regression (degree 2 and 3)
- RANSAC (robust regression)
- Ridge Regression (with cross-validation)
- Lasso Regression

### Results Summary
- Linear Regression: R² ≈ 0.49 (test)
- Polynomial models: higher training accuracy but overfitting
- RANSAC: similar performance to linear regression
- Ridge: no significant improvement
- Lasso: underfitting due to strong regularization

### Key Insights
- Moderate predictive power across all models
- Increasing complexity leads to overfitting without improving generalization
- Linear regression remains the most stable and interpretable model

---

## Tools and Libraries
- Python
- NumPy, Pandas
- Matplotlib, Seaborn
- Scikit-learn
- Statsmodels
- SciPy

---

## Key Takeaways
- Model selection depends heavily on data structure and problem type
- Flexible models (SVM, Random Forest) excel in complex classification tasks
- Simpler models can outperform complex ones in regression when data relationships are weak
- Overfitting is a critical issue when increasing model complexity

---

## How to Run
```bash
git clone <your-repo-url>
cd <repo-name>
pip install -r requirements.txt
jupyter notebook
