# Healthcare Insurance Premium Prediction

This project predicts healthcare insurance premiums using machine learning.  
The goal is to estimate insurance costs based on demographic, lifestyle, and medical risk factors.

The project follows an **end-to-end machine learning workflow**, including exploratory data analysis, feature engineering, model training, error analysis, and deployment.

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Machine Learning](https://img.shields.io/badge/Model-XGBoost-orange)
![Deployment](https://img.shields.io/badge/Deployment-Streamlit-green)

## Live Demo
https://ml-project-healthcare-insurance-prediction.streamlit.app/

## App Preview
<img width="1081" height="747" alt="App Preview" src="https://github.com/user-attachments/assets/7f06b133-3b54-4f16-85b7-80320a9fae17" />

---

# Problem Statement

Insurance companies estimate premiums using multiple risk factors such as age, medical history, lifestyle habits, and income.  
This project builds a machine learning model to estimate healthcare insurance premiums based on these attributes.

---

# Project Workflow

## 1. Exploratory Data Analysis (EDA)
- Performed univariate and bivariate analysis
- Identified outliers using boxplots
- Analyzed relationships between features and insurance premiums

## 2. Data Cleaning
- Removed duplicate records
- Handled missing values
- Corrected invalid entries such as negative dependants

## 3. Feature Engineering
- Created a **risk score feature**
- Encoded categorical variables
- Selected relevant predictive features

## 4. Multicollinearity Analysis
- Used **Variance Inflation Factor (VIF)** to detect multicollinearity
- Removed highly correlated variables

## 5. Model Training
Multiple regression models were trained and compared:

- Linear Regression
- Ridge Regression
- XGBoost Regression

## 6. Error Analysis
Model evaluation revealed higher prediction errors for individuals under the age of 25.

## 7. Data Segmentation
To address this issue, the dataset was segmented:

- Age ≤ 25 → Young population model
- Age > 25 → General population model

Separate models were trained for each segment to improve prediction accuracy.

## 8. Model Deployment
The trained models and scalers were exported using **Joblib** and deployed as an interactive web application using **Streamlit**.

---

# Features Used

- Age
- BMI Category
- Smoking Status
- Employment Status
- Medical History
- Income
- Number of Dependants
- Genetical Risk
- Insurance Plan
- Gender
- Marital Status
- Region

---

# Tech Stack

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- Streamlit
- Joblib

---

# Project Structure

ml-project-healthcare-premium-prediction
│
├── main.py
├── prediction_helper.py
├── requirements.txt
├── artifacts
│   ├── model_young.joblib
│   ├── model_rest.joblib
│   ├── scaler_young.joblib
│   └── scaler_rest.joblib
│
├── notebooks
│   ├── data_segmentation.ipynb
│   ├── ml_healthcare_premium_prediction.ipynb
│   ├── ml_premium_prediction_young_with_gr.ipynb
│   └── ml_premium_prediction_rest_with_gr.ipynb
│
└── README.md

The repository also includes Jupyter notebooks containing the full experimentation process:

- Exploratory Data Analysis
- Feature engineering
- Model training and comparison
- Error analysis
- Data segmentation for young vs rest population


---

# Deployment

The project is deployed using **Streamlit Cloud** and allows users to input features and receive real-time insurance premium predictions.


# How to Run the Project Locally
Follow these steps to run the application on your local machine.

### 1. Clone the repository
git clone https://github.com/YOUR_USERNAME/ml-project-healthcare-premium-prediction.git
cd ml-project-healthcare-premium-prediction

### 2. Create a virtual environment
python -m venv venv

### 3. Activate the environment
Windows:
venv\Scripts\activate
Mac/Linux:
source venv/bin/activate

### 4. Install dependencies
pip install -r requirements.txt

### 5. Run the Streamlit app
streamlit run main.py

⭐ If you found this project useful, consider giving it a star!
