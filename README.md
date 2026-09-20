# Student Performance - Grade Prediction

## Project Overview

This project builds a complete Machine Learning pipeline to predict a student's final grade (`A`, `B`, `C`, `D`, or `F`) using academic performance, attendance, study habits, and demographic/background factors.

The notebook covers the workflow from raw data loading and exploratory analysis through preprocessing, feature engineering, model comparison, hyperparameter tuning, and final evaluation.

## Problem Statement

A university wants to identify students who may be at academic risk early by predicting their final grade from available student-related features.

## Dataset

- **Records:** 5,000 students
- **Input features:** 22
- **Target:** `Grade`
- **Target classes:** A, B, C, D, F
- **Dataset file expected by the notebook:** `Students_Performance_Dataset.csv`

> Note: The notebook describes the dataset as synthetic/illustrative. It should be validated on real institutional data before production use.

## Machine Learning Workflow

1. Import libraries
2. Load and understand the data
3. Exploratory Data Analysis (EDA)
4. Missing-value handling
5. Outlier detection
6. Categorical encoding
7. Feature engineering
8. Feature selection
9. Scaling and normalization
10. Stratified train-test split
11. Model training and comparison
12. Hyperparameter tuning
13. Final model evaluation
14. Business insights and recommendations

## Feature Engineering

The notebook creates features including:

- `Avg_Academic_Score`
- `Engagement_Score`
- `Sleep_Stress_Balance`
- `Study_Efficiency`
- `Is_High_Risk`

## Models Compared

The notebook evaluates:

- Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting
- Extra Trees
- Bagging
- AdaBoost
- K-Nearest Neighbors (KNN)
- Gaussian Naive Bayes
- Support Vector Machine (SVM)
- XGBoost (when available)

## Class Imbalance

The `A` grade is extremely rare in the dataset. The notebook uses `class_weight='balanced'` where supported and intentionally avoids SMOTE because of the very small minority class.

## Hyperparameter Tuning

RandomizedSearchCV with stratified 5-fold cross-validation is used to tune a Random Forest model using macro F1 as the scoring metric.

The notebook's recorded tuning result:

- **Best CV Macro F1:** 89.74%
- **Test Macro F1:** 89.79%
- **Test Accuracy:** 99.70%

The notebook also records a 100% test result for some initial models. Because `Total_Score` is directly related to the grading formula, these results should not be interpreted as production-ready early-prediction performance.

## Key Insights

According to the notebook:

- `Total_Score` is the dominant predictive feature.
- Attendance and engagement are strongly connected with grade outcomes.
- Study hours and study efficiency provide additional performance signals.
- Stress and sleep-related features provide wellbeing-related signals.
- Parent education and family income show milder influence.

## Important Caveat

The notebook itself notes that `Total_Score` is derived directly from the grading formula. For a true early-warning/early-prediction system, features such as `Total_Score` and `Final_Score` should be excluded if they are only known after or near the end of the academic period.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- imbalanced-learn

## Repository Files

```text
Student-Performance-Machine-Learning/
├── Student_Performance_ML_Project.ipynb
├── Students_Performance_Dataset.csv
├── requirements.txt
├── README.md
└── .gitignore
```

`Students_Performance_Dataset.csv` is not included in this package because only the notebook was provided. Upload the dataset to the repository if you have permission to share it.

## How to Run

1. Clone/download the repository.
2. Install the dependencies:

```bash
pip install -r requirements.txt
```

3. Place `Students_Performance_Dataset.csv` in the same folder as the notebook.
4. Open `Student_Performance_ML_Project.ipynb` in Jupyter Notebook, JupyterLab, or VS Code.
5. Run the notebook cells in order.

## Portfolio Skills Demonstrated

- Data preprocessing
- Exploratory Data Analysis
- Missing-value handling
- Outlier analysis
- Categorical encoding
- Feature engineering
- Feature selection
- Feature scaling
- Imbalanced classification
- Model comparison
- Hyperparameter tuning
- Cross-validation
- Classification metrics
- Confusion matrix
- Feature importance
- Business-oriented ML insights

## Author

**Jay Gajare**

Machine Learning / Data Analytics Portfolio Project
