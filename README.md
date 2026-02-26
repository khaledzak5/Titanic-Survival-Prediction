# 🚢 Titanic Survival Prediction -- End-to-End Machine Learning Pipeline

## 📌 Overview

This project implements a complete machine learning workflow to predict
passenger survival on the Titanic dataset (Kaggle Competition).
The focus is on building a clean, reproducible, and leakage-free ML
pipeline from preprocessing to submission.

------------------------------------------------------------------------

## 🎯 Problem Statement

Predict whether a passenger survived the Titanic disaster using
structured passenger data.

Target variable: - Survived (1 = Survived, 0 = Did Not Survive)

------------------------------------------------------------------------

## 🧠 Workflow Summary

1.  Data inspection and exploration
2.  Missing value handling
3.  Feature engineering
4.  Encoding categorical variables
5.  Model training and evaluation
6.  Cross-validation
7.  Final model retraining
8.  Kaggle submission

------------------------------------------------------------------------

## 🧹 Data Preprocessing

### Dropped Columns

-   Cabin
-   Ticket
-   Name
-   PassengerId (stored separately for submission)

### Missing Values Handling

-   Age → Grouped median (by Pclass and Sex)
-   Embarked → Mode (from training data only)
-   Fare → Median (training statistics applied to test set)

All preprocessing statistics were derived strictly from the training
dataset to avoid data leakage.

------------------------------------------------------------------------

## ⚙️ Feature Engineering

-   FamilySize = SibSp + Parch + 1
-   IsAlone = 1 if FamilySize == 1 else 0
-   Log transformation applied to Fare

------------------------------------------------------------------------

## 🔢 Encoding

-   Sex → Binary encoding
-   Embarked → One-hot encoding (drop_first=True)

------------------------------------------------------------------------

## 🤖 Model

Model used: - RandomForestClassifier

Final Model Performance: - Train Accuracy ≈ 0.86
- Validation Accuracy ≈ 0.80
- 5-Fold Cross-Validation Mean AUC ≈ 0.868

------------------------------------------------------------------------

## 🏆 Kaggle Result

Public Leaderboard Score: 0.76794

------------------------------------------------------------------------

## 📁 Project Structure

-   Titanic Survival Classification.ipynb
-   train.csv
-   test.csv
-   submission.csv
-   README.md

------------------------------------------------------------------------

## 🔍 Key Learning Points

-   Preventing data leakage
-   Cross-validation vs single split
-   Overfitting detection and mitigation
-   Feature engineering importance
-   End-to-end ML workflow implementation

------------------------------------------------------------------------

## 🚀 Future Improvements

-   Title extraction from Name
-   Age binning
-   Interaction features
-   Gradient Boosting models
-   Hyperparameter tuning

------------------------------------------------------------------------

## 👨‍💻 Author

Khaled Zakaria
AI & Machine Learning Engineer
