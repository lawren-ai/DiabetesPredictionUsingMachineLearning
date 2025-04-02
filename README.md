# Diabetes Prediction using Machine Learning

## 📖 Project Overview

Diabetes mellitus remains a global health issue, causing thousands of deaths each day. Early detection of diabetes can help prevent severe health complications such as cardiovascular diseases, kidney failure, and vision loss. This project aims to develop a predictive model to detect potential diabetes cases using medical and demographic data.

## 💾 Dataset Description

The dataset consists of diagnostic measurements related to diabetes, collected from a population of Pima Indian women. The dataset includes the following features:

| Feature                  | Type        | Description                                    |
| ------------------------ | ----------- | ---------------------------------------------- |
| Pregnancies              | Numerical   | Number of times the patient has been pregnant  |
| Glucose                  | Numerical   | Plasma glucose concentration (mg/dL)           |
| BloodPressure            | Numerical   | Diastolic blood pressure (mm Hg)               |
| SkinThickness            | Numerical   | Triceps skinfold thickness (mm)                |
| Insulin                  | Numerical   | 2-Hour serum insulin (mu U/ml)                 |
| BMI                      | Numerical   | Body mass index (weight in kg/(height in m)^2) |
| DiabetesPedigreeFunction | Numerical   | Likelihood of diabetes based on family history |
| Age                      | Numerical   | Age of the patient in years                    |
| Outcome                  | Categorical | Diabetes diagnosis (1 = Yes, 0 = No)           |

## 🧐 Exploratory Data Analysis (EDA)

### Data Overview

- The dataset was loaded and examined using `data.head()` and `data.info()`.
- The `Outcome` column was treated as a categorical variable.

### Visualizations

#### Glucose Levels by Diabetes Outcome

A boxplot was created to show the distribution of glucose levels among diabetic and non-diabetic individuals.
![Glucose Levels by Diabetes Outcome](https://github.com/lawren-ai/DiabetesPredictionUsingMachineLearning/blob/main/Glucose%20by%20Diabetes%20Outcome.png)


#### Age Distribution by Diabetes Outcome

A KDE (Kernel Density Estimation) plot was used to visualize the age distribution for each diabetes outcome.
![Age distribution by Diabetes Outcome](https://github.com/lawren-ai/DiabetesPredictionUsingMachineLearning/blob/main/Age%20Distribution%20by%20Diabetes%20Outcome.PNG)

## 🔍 Feature Importance Analysis

### Correlation Analysis

Feature correlation with the diabetes outcome was computed, and a bar plot was generated to highlight the most influential features.


### Random Forest Feature Importance

A RandomForestClassifier was trained to evaluate feature importance, providing insights into the most critical predictors of diabetes.

![Feature correlation and Importance](https://github.com/lawren-ai/DiabetesPredictionUsingMachineLearning/blob/main/Feature_correlation%20and%20Feature%20Importance.PNG)

## 📊 Interactive Visualizations

- **Glucose vs BMI:** A scatter plot was created to analyze the relationship between glucose levels, BMI, and diabetes outcome.
  ![Glucose vs BMI](https://github.com/lawren-ai/DiabetesPredictionUsingMachineLearning/blob/main/Glucose%20vs%20BMI.PNG)
- **Age vs Diabetes Pedigree Function:** Another scatter plot was generated to study how age and genetic predisposition influence diabetes diagnosis.
  ![Age vs Pedigree Function](https://github.com/lawren-ai/DiabetesPredictionUsingMachineLearning/blob/main/Age%20vs%20Diabetes%20Pedigree%20Function.PNG)

## 🔮 Risk Estimation for a Given Case

A function was implemented to estimate the risk of diabetes for an individual based on:

- Age: 54 years
- Height: 178 cm
- Weight: 96 kg
- Glucose Level: 125 mg/dL

The model predicts a **high risk of diabetes** for this individual.

## 🤖 Model Training and Evaluation

### Data Splitting and Scaling

- The dataset was split into training (80%) and testing (20%) sets.
- StandardScaler was applied to normalize the features.

### Model Selection and Performance

- **Algorithm:** RandomForestClassifier
- **Accuracy:** Computed using `accuracy_score()`
- **Classification Report:** Precision, Recall, and F1-score were generated to assess model performance.

## 🏆 Key Findings

- **Glucose, BMI, and Age** are the most significant predictors of diabetes.
- Higher **glucose levels** are strongly associated with a positive diabetes diagnosis.
- **BMI and age** contribute significantly to diabetes risk, highlighting the importance of weight management and aging factors.
- Individuals with a higher **Diabetes Pedigree Function** score (indicating genetic predisposition) are more likely to be diabetic.
- The **RandomForestClassifier** provides high accuracy and can be effectively used for diabetes prediction.
- Interactive visualizations aid in understanding the relationships between features and diabetes risk.

## 🏆 Results and Conclusion

- The model successfully predicts diabetes cases with high accuracy.
- Glucose level, BMI, and Age are among the most influential factors.
- Interactive visualizations provide deeper insights into diabetes risks.

## 🚀 Future Improvements

- Experimenting with other machine learning models (e.g., XGBoost, SVM) for better performance.
- Incorporating more demographic and lifestyle factors.
- Deploying the model as a web-based or mobile application for real-world use.

---
