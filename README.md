#  Power System Load Type Classification

##  Objective

The objective of this project is to develop a machine learning model that predicts the **Load Type** of a power system using historical energy consumption data. The classification categories are:

-  Light_Load  
-  Medium_Load  
-  Maximum_Load  

This project demonstrates the complete ML pipeline: from data preprocessing and feature engineering to model selection and evaluation.

---

##  Dataset Description

The dataset includes the following features:

| Feature                            | Description                                           |
|------------------------------------|-------------------------------------------------------|
| `Date`                             | Continuous-time data recorded monthly                 |
| `Usage_kWh`                        | Industrial energy consumption (in kilowatt-hours)     |
| `Lagging_Current_Reactive_Power`   | Lagging reactive power (kVarh)                        |
| `Leading_Current_Reactive_Power`   | Leading reactive power (kVarh)                        |
| `CO2`                              | CO2 emissions (ppm)                                   |
| `NSM`                              | Number of seconds from midnight                       |
| `Load_Type`                        | Target variable: Light_Load, Medium_Load, Maximum_Load|

---

##  Project Pipeline

The project includes the following steps:

1. **Data Loading & Cleaning**
   - Handling missing values
   - Formatting date columns
2. **Exploratory Data Analysis (EDA)**
   - Visualizing feature distributions
   - Identifying correlations
3. **Feature Engineering**
   - Extracting datetime features
   - Normalization/Scaling
4. **Modeling**
   - Tried multiple models: Logistic Regression, Random Forest, XGBoost
   - Hyperparameter tuning using GridSearchCV
5. **Evaluation**
   - Used metrics: Accuracy, Precision, Recall, F1-Score
   - Validated using the last month of data as the test set

---

##  Evaluation Metrics

| Metric      | Description                         |
|-------------|-------------------------------------|
| Accuracy    | Overall correctness of predictions  |
| Precision   | Exactness of positive predictions   |
| Recall      | Completeness of positive predictions|
| F1-Score    | Harmonic mean of precision & recall |

---

##  Results

- **Best Model**: Random Forest Classifier  
-  **Test Accuracy**: 94.5%  
-  Model shows balanced performance across all classes

---

##  How to Run

### 1. Clone the repository
```bash
git clone https://github.com/your-username/power-load-classification.git
cd power-load-classification
