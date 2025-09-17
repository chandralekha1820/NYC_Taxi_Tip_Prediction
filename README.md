
**🚕 NYC Taxi Tip Prediction**

End-to-end machine learning pipeline to predict whether a NYC taxi passenger will leave a high tip based on trip details.

The project covers data cleaning, exploratory data analysis (EDA), feature engineering, modeling, and evaluation using Python, pandas, scikit-learn, and XGBoost.

**📑 Table of Contents**

-Overview

-Dataset

-Workflow

-Tools & Libraries

-Results

-Future Work

-Repository Structure

**📌 Overview**

This project predicts whether a passenger will leave a **high tip** for a NYC taxi trip based on trip features such as **fare amount, trip distance, and payment type**.

It demonstrates the **full data science lifecycle**:

Data ingestion & cleaning

Exploratory Data Analysis (EDA)

Feature engineering

Machine learning modeling & evaluation

**📚 Course Project**: MIS550E – Introduction to Data Science (Fall 2024) at Washington University of Virginia


**🗂 Dataset**

-**Source**: NYC Taxi trip dataset (NYC Open Data Portal)

-**Rows**: ~170,000 taxi rides (2013)

-**Features**: pickup time, drop-off time, trip distance, fare amount, tip amount, vendor ID, payment type, trip duration, etc.

-**Target**: Whether a tip was given (binary classification)


**🔑 Workflow**

**0. Setup**
Imported core libraries: 
pandas, numpy, matplotlib, seaborn, missingno, scikit-learn, xgboost

**1. Data Ingestion**

Loaded raw CSV files

Merged datasets on time-related keys

Resolved ~300 duplicate/misaligned rows

**2. Exploratory Data Analysis (EDA)**

-.head(), .describe(), .info() for inspection

-Distribution plots & histograms

-Correlation analysis & scatter matrix plots

-Missing values visualization (missingno.matrix())

-Categorical analysis: Vendor ID, Payment type, Weekend trips

**3. Data Cleaning & Transformation**

Handled duplicates & missing values (mean/median imputation)

Standardized categorical values (case, spelling)

Feature engineering:

Extracted day of week and rush hour from pickup time

Created binary features (weekend / rush hour)

One-hot encoding for categorical variables

**4. Feature Selection**

Correlation heatmap used to drop redundant features

Removed IDs & unused fields

**5. Modeling**

**Baseline**: Logistic Regression

**Advanced Models**: Random Forest, XGBoost

Hyperparameter tuning with **GridSearchCV** & cross-validation

**6. Evaluation**

**Metrics**: Accuracy, Precision, Recall, F1-score, ROC-AUC

Random Forest achieved ~98% accuracy, high precision & recall


**🛠 Tools & Libraries**

-Python 3.x

-pandas, numpy

-matplotlib, seaborn, missingno

-scikit-learn

-xgboost

 -Jupyter Notebook

**📊 Results**

**Best Model**: Random Forest (after tuning)

**Accuracy**: 98.3%

**Precision**: 96.9%

**Recall**: 99.8%

**F1-Score**: 98.3%

**ROC-AUC**: 98.5%

**Key Insights:**

Higher fares and longer trips → higher tips

Payment type strongly affects tipping behavior

Weekend and rush-hour patterns influence tipping

**🔮 Future Work**

Add driver ratings & passenger demographics for richer features

Explore real-time tip prediction systems for taxi apps

Try advanced models (Gradient Boosting, Neural Nets)

**📂 Repository Structure**
NYC_Taxi_Tip_Prediction/

│── DS_Final_Project_Fall_2024__testing.ipynb     # Jupyter Notebook (main pipeline)

│── Data Science Final Project Presentation.pptx    # Final presentation slides

│── README.md                                     # Project documentation

│── requirements.txt    
