# Titanic Survival Analysis - Machine Learning Project

**Author:** Samra Mohsin  
**Role:** Machine Learning Intern  
**Organization:** Neurofive Solutions  

---

## Project Overview

This project is part of my Machine Learning Internship at Neurofive Solutions. I analyzed the famous Titanic dataset to understand survival patterns, clean messy data, and create meaningful visualizations. This is the foundation for building predictive models.

The project is divided into two main tasks:

| Task | Topic | Status |
|------|-------|--------|
| Task 1 | Exploratory Data Analysis (EDA) | ✅ Complete |
| Task 2 | Data Cleaning and Visualization | ✅ Complete |

---

## Task 1: Exploratory Data Analysis (EDA)

### Objective
To understand the Titanic dataset structure, identify data quality issues, and discover initial patterns.

### Steps Performed

1. **Data Loading**
   - Used pandas to load the Titanic dataset
   - Examined the first 5 rows using `df.head()`

2. **Data Exploration**
   - Checked data types with `df.info()`
   - Generated statistical summary with `df.describe()`
   - Found dataset shape: 891 rows, 12 columns

3. **Missing Values Analysis**
   - **Age:** 177 missing values (19.9% of data)
   - **Cabin:** 687 missing values (77.1% of data)
   - **Embarked:** 2 missing values (0.2% of data)

4. **Feature Identification**
   - **Numerical columns:** PassengerId, Survived, Pclass, Age, SibSp, Parch, Fare
   - **Categorical columns:** Name, Sex, Ticket, Cabin, Embarked

### Key Findings
- **Survival Rate:** 38.38% (342 survived, 549 did not)
- Most passengers were between 20-40 years old
- Gender and ticket class appear to be important survival factors

### Notebook
`titanic_eda.ipynb`

---

## Task 2: Data Cleaning and Visualization

### Objective
To clean the data properly and tell its story through visualizations before building machine learning models.

### 1. Handling Missing Values

**My Approach:**

| Column | Missing Values | Method Used | Justification |
|--------|---------------|-------------|---------------|
| Cabin | 687 (77%) | Dropped | Too many missing values to fill reliably |
| Age | 177 (19.9%) | Filled with median | Median is robust against outliers |
| Embarked | 2 (0.2%) | Filled with mode | Only 2 missing, use most common value |

**Code Implementation:**
```python
# Drop Cabin column
df_clean = df.drop('Cabin', axis=1)

# Fill Age with median
df_clean['Age'] = df_clean['Age'].fillna(df_clean['Age'].median())

# Fill Embarked with mode
df_clean['Embarked'] = df_clean['Embarked'].fillna(df_clean['Embarked'].mode()[0])