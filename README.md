# yuva-intern
# Week 1 — Data Acquisition, Cleaning and Preprocessing

## 📌 Project Overview

This project was completed as part of the Week 1 technical internship task on Data Acquisition, Cleaning, and Preprocessing.

The project demonstrates a complete data preprocessing workflow using the Titanic passenger dataset. The workflow includes dataset acquisition, exploratory data analysis, missing-value analysis, duplicate detection, invalid-value checking, outlier analysis, data cleaning, feature engineering, categorical encoding, and numerical scaling.

## 🎯 Objectives

* Acquire a publicly available dataset
* Understand the structure and quality of the dataset
* Identify missing values
* Detect duplicate records
* Identify inconsistent or invalid values
* Detect and investigate outliers
* Perform appropriate data cleaning
* Apply preprocessing techniques
* Compare the dataset before and after preprocessing
* Document the reasoning behind preprocessing decisions

## 📊 Dataset

**Dataset:** Titanic — Machine Learning from Disaster

**Source:** Kaggle

The dataset contains passenger information such as:

* Passenger class
* Sex
* Age
* Number of siblings/spouses
* Number of parents/children
* Ticket
* Fare
* Cabin
* Port of embarkation
* Survival status

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Google Colab
* GitHub

## 🔍 Data Cleaning Process

The following data-quality issues were investigated:

1. Missing values
2. Duplicate records
3. Invalid numerical values
4. Categorical inconsistencies
5. Numerical outliers
6. High-missingness columns

### Missing Values

Missing values were analyzed using both counts and percentages.

Numerical missing values such as `Age` were handled using median imputation, while categorical missing values such as `Embarked` were handled using the mode.

The `Cabin` column contained substantial missing information. Instead of removing all records with missing cabin information, a `CabinKnown` feature was created to preserve useful information about cabin availability.

### Outlier Analysis

The Interquartile Range (IQR) method was used to identify potential numerical outliers.

Outliers were investigated rather than automatically deleted because an extreme value may represent a legitimate real-world observation.

## ⚙️ Feature Engineering

The following features were created:

* `CabinKnown`
* `FamilySize`
* `IsAlone`

These features provide additional information that can be useful for subsequent analysis.

## 🔄 Preprocessing

Categorical variables were encoded using one-hot encoding.

Numerical variables were standardized using `StandardScaler`.

A separate model-ready dataset was created after preprocessing.

## 📁 Project Structure

```text
week1-data-cleaning-preprocessing/
│
├── README.md
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   └── Week1_Titanic_Data_Cleaning_Colab.ipynb
│
├── outputs/
│   ├── titanic_cleaned.csv
│   ├── titanic_preprocessed.csv
│   └── final_quality_summary.csv
│
├── figures/
│   ├── missing_values_before.png
│   ├── outliers_before.png
│   └── before_after_quality.png
│
└── reports/
    └── Week_1_Data_Cleaning_Report.docx
```

## 📈 Results

The project produces a cleaned dataset and a preprocessing-ready dataset.

The notebook also generates visualizations showing:

* Missing values
* Potential numerical outliers
* Before-and-after data quality

The exact numerical results are documented in the final project report.

## 💡 Key Learning

This project demonstrates that data preprocessing should not consist of blindly deleting missing values or outliers. Each data-quality issue needs to be investigated and treated according to its context and potential impact on subsequent analysis.

## 📄 Report

The complete detailed analysis is available in:

`reports/Week_1_Data_Cleaning_Report.docx`

## 👩‍💻 Author

**Swathi V.**

B.Tech Artificial Intelligence and Data Science

## 📚 References

* Kaggle — Titanic: Machine Learning from Disaster
* Python Documentation
* Pandas Documentation
* Scikit-learn Documentation
