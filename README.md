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

## 🔧 Tasks Involved
1️⃣ **Data Preprocessing**
- Load the dataset
- Handle missing values and data cleaning
- Convert `Outcome` to categorical for visualization

2️⃣ **Feature Importance Analysis**
- Train a **Random Forest Classifier** on all available features
- Extract and rank feature importance scores
- **Top Features Identified**: `Glucose`, `BMI`, `Age`

3️⃣ **Data Visualization**
- Boxplot of `Glucose` levels by diabetes outcome
- KDE plot of `Age` distribution by diabetes outcome
- Feature importance visualization
- Interactive plots for better insights

4️⃣ **Model Training with Selected Features**
- Train a **Random Forest Classifier** using only the top 3 features
- Split data into **80% training, 20% testing**
- Evaluate model performance using **accuracy, precision, recall, and F1-score**

5️⃣ **Diabetes Risk Prediction**
- Input test case: **Age = 54, Height = 178 cm, Weight = 96 kg, Glucose = 125 mg/dL**
- Calculate BMI from height & weight
- Predict diabetes risk using trained model
- **Prediction Output**: `87% probability of diabetes (High Risk)`

## 📊 Results
- **Feature Importance Scores:**
  ```plaintext
  Glucose                     0.257226
  BMI                         0.168345
  Age                         0.132573
  DiabetesPedigreeFunction    0.126038
  BloodPressure               0.092014
  Pregnancies                 0.084424
  Insulin                     0.072200
  SkinThickness               0.067179
  ```
- **Model Accuracy:** `73.38%`

- **Predicted Diabetes Risk Example:**
  - **Input:** `Age = 54, Height = 178 cm, Weight = 96 kg, Glucose = 125 mg/dL`
  - **Predicted Status:** `High Risk of Diabetes`
  - **Diabetes Probability:** `87%`

## 📈 Visualizations
- **Boxplot of Glucose Levels by Outcome** 

![Glucose Boxplot](https://github.com/lawren-ai/DiabetesPredictionUsingMachineLearning/blob/main/Glucose%20by%20diabetes%20outcome.PNG)
- **Age Distribution by Diabetes Outcome** 

![Age KDE Plot](https://github.com/lawren-ai/DiabetesPredictionUsingMachineLearning/blob/main/Age%20Distribution%20by%20Diabetes%20Outcome.PNG)
- **Feature Importance Chart** 

![Feature Importance](https://github.com/lawren-ai/DiabetesPredictionUsingMachineLearning/blob/main/Feature_importance.PNG)
- **Interactive Plots Showing relationship between the top four factors determining Diabetes. Go through the notebook ![Notebook](https://github.com/lawren-ai/DiabetesPredictionUsingMachineLearning/blob/main/DiabetesMellitus%20(1).ipynb) to interact with the visualizations:**


- Histogram Showing relationship between diabetes and glucose level
![Histogram](https://github.com/lawren-ai/DiabetesPredictionUsingMachineLearning/blob/main/Diabetes%20by%20glucose%20level.PNG)
- Scatter Plot showing relationship between patient's Age and BMI 
![Scatter Plot](https://github.com/lawren-ai/DiabetesPredictionUsingMachineLearning/blob/main/Age%20vs%20BMI.PNG)
-  Violin Plot Showing relationship between diabetes status and the diabetes pedigree function
![Violin Plot](https://github.com/lawren-ai/DiabetesPredictionUsingMachineLearning/blob/main/Diabetes%20Pedigree%20function%20by%20Diabetes%20status.PNG)
- Box Plot Showing relationship between diabetes and blood pressure
![Box Plot](https://github.com/lawren-ai/DiabetesPredictionUsingMachineLearning/blob/main/Diabetes%20by%20blood%20pressure.PNG)

## 🏆 Key Findings

- **Glucose, BMI, and Age** are the most significant predictors of diabetes.
- Higher **glucose levels** are strongly associated with a positive diabetes diagnosis.
- **BMI and age** contribute significantly to diabetes risk, highlighting the importance of weight management and aging factors.
- Individuals with a higher **Diabetes Pedigree Function** score (indicating genetic predisposition) are more likely to be diabetic.
- The **RandomForestClassifier** provides high accuracy and can be effectively used for diabetes prediction.
- Interactive visualizations aid in understanding the relationships between features and diabetes risk.


## 🚀 Future Improvements

- Experimenting with other machine learning models (e.g., XGBoost, SVM) for better performance.
- Incorporating more demographic and lifestyle factors.
- Deploying the model as a web-based or mobile application for real-world use.

---
## 🔗 References
- [Scikit-Learn Documentation](https://scikit-learn.org/)
- [DataCamp](#) *(datacamp.com/datalab)*

---
**Author:** *Ayotunde Akinboade*  
📧 Contact: *akinboadelawrenceayo@gmail.com*
