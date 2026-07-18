# Titanic Dataset - Exploratory Data Analysis

**Author:** Samra Mohsin  
**Role:** Machine Learning Intern  
**Project:** First EDA Assignment for Neurofive ML Track

---

## Project Overview

This project is my first Exploratory Data Analysis (EDA) assignment as a Machine Learning Intern. I analyzed the Titanic passenger dataset using Python and pandas to understand data structure, identify missing values, and distinguish between numerical and categorical features. This foundational work is essential before building any machine learning model.

---

## Dataset Information

- **Source:** Kaggle Titanic Competition
- **Samples:** 891 passenger records
- **Features:** 12 columns
- **Target Variable:** Survived (0 = Did not survive, 1 = Survived)
- **Survival Rate:** 38.38%

### Features Description

| Feature | Type | Description |
|---------|------|-------------|
| PassengerId | int64 | Unique passenger identifier |
| Survived | int64 | Target variable (0/1) |
| Pclass | int64 | Ticket class (1st, 2nd, 3rd) |
| Name | string | Passenger name |
| Sex | string | Gender |
| Age | float64 | Age in years |
| SibSp | int64 | Siblings/Spouses aboard |
| Parch | int64 | Parents/Children aboard |
| Ticket | string | Ticket number |
| Fare | float64 | Fare paid |
| Cabin | string | Cabin number |
| Embarked | string | Port of embarkation (C= Cherbourg, Q= Queenstown, S= Southampton) |

---

## Key Findings

### Missing Values Analysis
- **Age:** 177 missing values (19.9%) - Requires imputation
- **Cabin:** 687 missing values (77.1%) - Consider dropping or feature engineering
- **Embarked:** 2 missing values (0.2%) - Easy to impute with mode

### Feature Types
- **Numerical Features:** Age, Fare, SibSp, Parch, PassengerId, Pclass
- **Categorical Features:** Name, Sex, Ticket, Cabin, Embarked
- **Note:** Survived is numerical but serves as a categorical target variable

---

## Technical Implementation

### Tools & Technologies
- Python 3.x
- pandas for data manipulation
- Jupyter Notebook (VS Code)
- Git & GitHub for version control

### Key Code Snippets

```python
import pandas as pd

# Load dataset
df = pd.read_csv('Titanic-Dataset.csv')

# Explore data
df.head()
df.info()
df.describe()

# Check missing values
df.isnull().sum()

# Identify feature types
numerical_cols = df.select_dtypes(include=['int64', 'float64']).columns.tolist()
categorical_cols = df.select_dtypes(include=['object', 'string']).columns.tolist()