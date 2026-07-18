# Titanic Dataset - My First EDA

This is my first Exploratory Data Analysis (EDA) assignment. I'm using the Titanic dataset from Kaggle to practice pandas and understand data better.

## Project Overview

I analyzed the Titanic passenger dataset to understand the data structure, find missing values, and identify which columns are numerical vs categorical. This is my first step in learning data science and machine learning.

## Dataset Information

- **Source:** Kaggle Titanic competition
- **Rows:** 891
- **Columns:** 12
- **Survival Rate:** 38.38% (342 survived, 549 did not)

### Columns in the Dataset

| Column Name | Type | Description |
|-------------|------|-------------|
| PassengerId | Numerical | Unique ID for each passenger |
| Survived | Categorical | 0 = Did not survive, 1 = Survived |
| Pclass | Categorical | Ticket class (1st, 2nd, 3rd) |
| Name | Categorical | Passenger's full name |
| Sex | Categorical | male or female |
| Age | Numerical | Age in years |
| SibSp | Numerical | Number of siblings/spouses aboard |
| Parch | Numerical | Number of parents/children aboard |
| Ticket | Categorical | Ticket number |
| Fare | Numerical | Fare paid |
| Cabin | Categorical | Cabin number |
| Embarked | Categorical | Port of embarkation (C, Q, S) |

## Key Findings

### Missing Values
- **Age:** 177 missing values - needs to be filled
- **Cabin:** 687 missing values - more than 75% missing, might need to drop
- **Embarked:** 2 missing values - easy to fill with the most common value

### Column Types
- **Numerical columns:** Age, Fare, SibSp, Parch
- **Categorical columns:** Name, Sex, Ticket, Cabin, Embarked
- **Note:** Survived is stored as a number but is actually categorical

## What I Learned

- Real data is never perfect - there are always missing values
- Not all numbers are numerical data - some represent categories
- Data cleaning is really important before machine learning
- Different columns need different approaches for handling missing values
- EDA helps understand data before building models

## Files in This Repository

| File | Description |
|------|-------------|
| `titanic_eda.ipynb` | My Jupyter notebook with all EDA code and outputs |
| `Titanic-Dataset.csv` | The Titanic dataset from Kaggle |
| `README.md` | This file |

## Tools Used

- Python 3
- pandas library
- Jupyter Notebook (in VS Code)
- Git and GitHub

## How to Run This Notebook

1. Clone this repository
2. Make sure you have Python and pandas installed
3. Open `titanic_eda.ipynb` in Jupyter Notebook or VS Code
4. Run each cell one by one

## Next Steps

I plan to learn:
1. How to handle missing values properly
2. Data visualization with matplotlib/seaborn
3. Building my first machine learning model

## Acknowledgements

- Kaggle for providing the Titanic dataset
- Neurofive ML Track for this learning opportunity

## Author

Samra Mohsin - Data Science Student

---

*This is my first EDA assignment. I'm still learning and will continue to improve my skills!*