TITANIC SURVIVAL ANALYSIS
Exploratory Data Analysis & Data Visualization

================================================================================

TABLE OF CONTENTS
================================================================================

1. Project Overview
2. Dataset Description
3. Project Structure
4. Notebooks
5. Key Findings
6. Technologies Used
7. Installation & Setup
8. Results
9. Next Steps
10. Connect

================================================================================

PROJECT OVERVIEW
================================================================================

This project presents a comprehensive exploratory data analysis (EDA) of the 
famous Titanic dataset. The goal is to understand the data, handle missing 
values, detect outliers, and create visualizations to uncover patterns before 
building predictive models.

Key Objectives:
- Perform initial data exploration to understand dataset structure
- Handle missing values with appropriate strategies
- Detect and analyze outliers in numerical features
- Create visualizations to identify survival patterns
- Determine which features most strongly influence survival

================================================================================

DATASET DESCRIPTION
================================================================================

The dataset contains information about passengers aboard the RMS Titanic, which 
sank on April 15, 1912. It includes demographic and travel information for 891 
passengers.

Features:
- Survived: Survival indicator (0 = No, 1 = Yes)
- Pclass: Passenger class (1st, 2nd, 3rd)
- Name: Passenger name
- Sex: Gender
- Age: Age in years
- SibSp: Number of siblings/spouses aboard
- Parch: Number of parents/children aboard
- Ticket: Ticket number
- Fare: Passenger fare
- Cabin: Cabin number
- Embarked: Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)

================================================================================

PROJECT STRUCTURE
================================================================================

neurofive-ml-track/
│
├── data/
│   ├── train.csv                   # Training dataset (891 records)
│   ├── test.csv                    # Test dataset (418 records)
│   └── gender_submission.csv       # Sample submission format
│
├── notebooks/
│   ├── titanic_eda.ipynb           # Phase 1: Initial exploration
│   └── titanic_cleaning_visualization.ipynb  # Phase 2: Cleaning & visuals
│
├── .gitignore
├── README.md
└── requirements.txt                # Project dependencies

================================================================================

NOTEBOOKS
================================================================================

1. titanic_eda.ipynb - Initial Exploration
   Status: Complete

   Description:
   First-phase analysis focusing on understanding the dataset's structure, 
   identifying data types, and detecting missing values.

   Key Steps:
   - pd.read_csv(): Load dataset
   - .head(): Preview first 5 rows
   - .info(): Check data types & missing values
   - .describe(): Statistical summary
   - .isnull().sum(): Count missing values
   - .select_dtypes(): Identify numeric vs categorical

   Output:
   - Dataset shape: (891, 12)
   - 177 missing values in Age column
   - 687 missing values in Cabin column
   - 2 missing values in Embarked column

-------------------------------------------------------------------------------

2. titanic_cleaning_visualization.ipynb - Data Cleaning & Visualization
   Status: Complete

   Description:
   Second-phase analysis focused on cleaning messy data and creating 
   visualizations to uncover patterns.

   Data Cleaning Strategy:
   - Cabin (77.1% missing): Dropped column - Too many missing values
   - Age (19.9% missing): Filled with median - Median is robust to outliers
   - Embarked (0.2% missing): Filled with mode - Only 2 missing values

   Visualizations Created:
   1. Histogram: Age distribution - Most passengers aged 20-40 years
   2. Boxplot: Age by Passenger Class - 1st class passengers older on average
   3. Bar Chart: Survival by Gender - 74% female survival vs 19% male
   4. Heatmap: Feature correlations - Pclass and Fare strongly correlated

================================================================================

KEY FINDINGS
================================================================================

1. Feature Importance

   Gender is the strongest predictor of survival

   - Female survival rate: 74.2%
   - Male survival rate: 18.9%
   - Difference: 55.3 percentage points

   Supporting Evidence:
   - "Women and children first" policy clearly reflected in data
   - 55 percentage point gap indicates systematic bias
   - Consistent with historical records

-------------------------------------------------------------------------------

2. Secondary Factors

   - Passenger Class: Moderate impact - 1st class had highest survival
   - Fare: Moderate impact - Higher fare = higher survival
   - Age: Weak impact - Younger passengers slightly better outcomes

-------------------------------------------------------------------------------

3. Data Quality Observations

   Issues Identified:
   - Cabin column has 77% missing data: Dropped
   - Age has 20% missing data: Imputed with median
   - Fare contains outliers up to 512: Normalize for modeling

   Recommendations:
   - Consider feature engineering from Name (title extraction)
   - Create family size feature from SibSp + Parch
   - Scale Fare to reduce outlier impact

================================================================================

TECHNOLOGIES USED
================================================================================

- Language: Python 3.8+
- Data Processing: pandas, numpy
- Visualization: matplotlib, seaborn
- Development: Jupyter Notebook, VS Code
- Version Control: Git, GitHub

================================================================================

INSTALLATION & SETUP
================================================================================

Prerequisites:
- Python 3.8 or higher
- Git (for cloning)
- VS Code or Jupyter Notebook

Step 1: Clone Repository
git clone https://github.com/SamraMohsin/neurofive-ml-track.git
cd neurofive-ml-track

Step 2: Create Virtual Environment
python -m venv venv

For Windows:
venv\Scripts\activate

For Mac/Linux:
source venv/bin/activate

Step 3: Install Dependencies
pip install pandas numpy matplotlib seaborn jupyter

Step 4: Launch Notebooks

In VS Code:
code .

Or in Jupyter:
jupyter notebook notebooks/

================================================================================

RESULTS
================================================================================

Statistical Summary:

- Total Passengers: 891
- Overall Survival Rate: 38.4%
- Female Survival Rate: 74.2%
- Male Survival Rate: 18.9%
- Average Age: 29.7 years
- Average Fare: 32.20

Correlation with Survival:

- Pclass: -0.34 (negative = higher class = better survival)
- Fare: 0.26 (higher fare = better survival)
- Age: -0.06 (younger = slightly better survival)
- SibSp: -0.04
- Parch: 0.08

================================================================================

NEXT STEPS
================================================================================

Planned Improvements:
- Build predictive models (Logistic Regression, Random Forest)
- Engineer new features from existing data
- Perform hyperparameter tuning
- Create predictions for test.csv
- Submit to Kaggle competition

Feature Engineering Ideas:
- Extract titles from Name (Mr, Mrs, Miss, Master)
- Calculate family size from SibSp + Parch
- Create age groups/bins
- Scale and normalize Fare

================================================================================

CONNECT
================================================================================

- GitHub: https://github.com/SamraMohsin
- Project: https://github.com/SamraMohsin/neurofive-ml-track

================================================================================

ACKNOWLEDGMENTS
================================================================================

- Neurofive Solutions - For providing the learning opportunity
- Kaggle - For the Titanic dataset
- Python Community - For excellent open-source libraries

================================================================================



"Data is the new oil. But like oil, it needs to be refined before it's useful."

================================================================================