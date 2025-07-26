# -Titanic-Survival-Prediction
End-to-end machine learning solution for the Titanic dataset using data cleaning, feature engineering, model tuning, and final Kaggle submission with a public score of 0.76555.

# 🚢 Titanic Survival Prediction - Random Forest Based ML Pipeline

This is a complete end-to-end machine learning project built on the famous **Titanic: Machine Learning from Disaster** dataset on Kaggle. The goal is to predict passenger survival using classification models, with a focus on **data preprocessing**, **feature engineering**, and **model tuning**.

---

## 📌 Project Description

The Titanic dataset is a widely used beginner dataset for classification problems in machine learning. In this project, we went through all key stages of the ML pipeline:

- Exploratory Data Analysis
- Data Cleaning & Imputation
- Feature Engineering
- Model Selection and Hyperparameter Tuning
- Final Prediction and Kaggle Submission

---

## 🔍 Phases Breakdown

### ✅ Phase 1: Data Cleaning
- Dropped non-informative columns: `Name`, `Ticket`, `Cabin`
- Filled missing values in:
  - `Age`: with median grouped by `Pclass` and `Sex`
  - `Embarked`: with mode
  - `Fare` in test set: with median

### ✅ Phase 2: Feature Engineering
- Created `FamilySize` as `SibSp + Parch + 1`
- Extracted `Title` from the `Name` column before dropping it
- Mapped categorical columns (`Sex`, `Embarked`, `Title`) using **Label Encoding**

### ✅ Phase 3: Model Training & Tuning
- Tried baseline models including Logistic Regression and XGBoost
- Observed XGBoost underperformed (~0.60 accuracy)
- Final model: **Random Forest Classifier**
  - Tuned using `GridSearchCV`
  - Best parameters selected based on cross-validation
  - Trained on full training set and predicted on test set

### ✅ Phase 4: Final Submission
- Predictions were exported as `submission_final.csv`
- Submitted to Kaggle for evaluation


## 🏆 Kaggle Performance

- **Final Kaggle Score**: `0.76555`
- **Kaggle Rank**: ~11,000 (Top 30–35% range at time of submission)
- **Final Model**: Random Forest Classifier with GridSearchCV tuning


## 📁 Project Structure


├── data/
│   ├── train.csv
│   └── test.csv
├── titanic_model.ipynb       <- All model development in Jupyter
├── submission/
│   └── submission_final.csv
├── README.md
└── requirements.txt




## 🎓 What I Learned

- How to clean and preprocess real-world datasets with missing values
- Feature extraction using domain knowledge (like `Title`, `FamilySize`)
- Label encoding vs OneHotEncoding choices
- Why some models (e.g. XGBoost) may not always outperform others
- Hyperparameter tuning using `GridSearchCV`
- Submitting predictions on Kaggle and interpreting scores

---

## 💼 Future Improvements

- Try ensemble techniques (Voting, Stacking)
- Add feature importance plots for interpretability
- Experiment with other preprocessing pipelines

---


> Built as part of machine learning practice. Feel free to fork, reuse, or collaborate!
