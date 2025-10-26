# 🩺 Multiclass Diabetes Classification using Logistic Regression

This project builds a **multiclass classification model** using **Logistic Regression** to predict the type or severity of diabetes based on various clinical parameters.

---

## 📊 Dataset

**File:** `Multiclass_Diabetes_dataset.csv`  
The dataset contains 264 samples with 12 columns including gender, age, cholesterol levels, BMI, and others.

| Column | Description |
|--------|--------------|
| Gender | 0 = Female, 1 = Male |
| AGE | Age of the patient |
| Urea | Urea level |
| Cr | Creatinine level |
| HbA1c | Glycated hemoglobin |
| Chol | Cholesterol |
| TG | Triglycerides |
| HDL | High-density lipoprotein |
| LDL | Low-density lipoprotein |
| VLDL | Very low-density lipoprotein |
| BMI | Body Mass Index |
| Class | Diabetes class (target variable) |

---
## Objective

To build a simple yet effective logistic regression model for predicting diabetes categories while understanding the role of correlated medical parameters and their impact on predictive performance.


## Project Description
This project applies Logistic Regression to predict different classes (types) of diabetes based on key clinical and biochemical features such as HbA1c, BMI, Cholesterol, and Age.
The goal is to demonstrate a complete machine learning workflow, starting from data preprocessing and exploratory data analysis (EDA) to multicollinearity detection (VIF), model training, and performance evaluation.

The dataset used represents a multiclass classification problem — where patients are categorized into different diabetes levels

 ## The project helps understand:

- How logistic regression works for multiclass problems

- The importance of feature scaling

- The impact of multicollinearity on model performance
- How to interpret model coefficients and feature influence
-I t also includes clear data visualizations, correlation heatmaps, confusion matrix, and classification metrics to evaluate model performance.
## ⚙️ Project Workflow
1. **Data Loading and Cleaning**
   - Checked for missing values and duplicates.
2. **Exploratory Data Analysis (EDA)**
   - Correlation heatmap to analyze feature relationships.
3. **Feature Scaling**
   - Standardized numerical features using `StandardScaler`.
4. **Multicollinearity Check**
   - Calculated VIF (Variance Inflation Factor).
5. **Model Training**
   - Used `LogisticRegression()` from Scikit-learn.
6. **Evaluation**
   - Confusion Matrix and Classification Report to assess performance.

##  How VIF Was Used for Feature Selection
- High VIF (Variance Inflation Factor) values indicate multicollinearity — when features are highly correlated with each other.
- In this dataset, **AGE**, **BMI**, and **Chol** showed high VIF values, suggesting they share overlapping information with other variables.
 However, removing them caused a drop in model accuracy, meaning these features still contribute valuable predictive information.
 Therefore, each high-VIF feature was individually tested for its impact on accuracy.
- Features were retained or removed based on their actual contribution to model performance rather than VIF value alone.

---
## 🧮 Results

- **Model:** Logistic Regression  
- **Accuracy:** *around 94%*  
- **Best features (by coefficient magnitude):** `HbA1c`, `BMI`, `Chol`

---

## Key Learnings

- Importance of **feature scaling** in logistic regression  
- Checking **multicollinearity** using VIF  
- Evaluating multiclass models using **classification report & confusion matrix**

```
## requirements
pandas
numpy
matplotlib
seaborn
scikit-learn
statsmodels
```

## 🚀 Future Improvements
- Try advanced models like **RandomForest**, **XGBoost**
- Add **ROC-AUC** visualization for multiclass classification

---

## 📜 License
This project is released under the MIT License — feel free to use, modify, and share.

---

## ✨ Author
**Shubhra Jha**  
⭐ *If you found this useful, consider giving a star to the repo!*

