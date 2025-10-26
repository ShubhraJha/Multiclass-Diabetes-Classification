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


---

## 🧮 Results

- **Model:** Logistic Regression  
- **Accuracy:** *around 88-94% (varies by train-test split)*  
- **Best features (by coefficient magnitude):** `HbA1c`, `BMI`, `Chol`

---

## Key Learnings

- Importance of **feature scaling** in logistic regression  
- Checking **multicollinearity** using VIF  
- Evaluating multiclass models using **classification report & confusion matrix**

---
## Notes on Multicollinearity (VIF Analysis)
- High VIF (Variance Inflation Factor) values indicate multicollinearity — when features are highly correlated with each other.
- In this dataset, **AGE**, **BMI**, and **Chol** showed high VIF values, suggesting they share overlapping information with other variables.
 However, removing them caused a drop in model accuracy, meaning these features still contribute valuable predictive information.
 Therefore, each high-VIF feature was individually tested for its impact on accuracy.
- Features were retained or removed based on their actual contribution to model performance rather than VIF value alone.
**requirements.txt**
```
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

