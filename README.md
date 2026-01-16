# Employee Salary Prediction Using Machine Learning

## Project Overview
- Built a regression-based machine learning system to predict annual employee salary
- Objective: analyze salary trends and identify key factors influencing employee pay
- Uses historical hiring and salary data for exploratory analysis and prediction

## Dataset
- **train_salary.csv**
- Contains employee details including:
  - Name
  - JobTitle
  - Agency
  - AgencyID
  - HireDate
  - AnnualSalary
  - GrossPay

## Data Preprocessing & Feature Engineering
- Removed unnecessary columns such as `GrossPay`
- Cleaned column names by stripping extra spaces
- Removed rows with missing hire dates
- Converted salary from string to numeric format
- Extracted Month, Day, and Year from HireDate
- Removed extreme salary outliers (AnnualSalary > 140000)
- Dropped non-informative columns such as employee name

## Exploratory Data Analysis
- Analyzed most common job titles and hiring agencies
- Visualized salary distribution and outliers
- Identified top 10 hiring jobs and highest paying roles
- Examined hiring trends across months and years
- Performed correlation analysis using heatmaps and pair plots

## Categorical Encoding
- Applied mean encoding to categorical variables:
  - JobTitle
  - Agency
  - AgencyID
- Replaced categorical values with their corresponding average salary

## Model Building & Evaluation
- Train-test split: 80% training, 20% testing
- Scaled features using StandardScaler
- Models used:
  - Linear Regression
  - Decision Tree Regressor
  - Random Forest Regressor
  - XGBoost Regressor
- Evaluation metric: R² score
- Ensemble models showed better predictive performance

## How to Run the Repository
1. Clone the repository

        git clone https://github.com/Gem793/Salary_Prediction_Model
        cd Employee_Salary_Predictor
2. Install required dependencies

        pip install pandas numpy matplotlib seaborn scikit-learn xgboost
3. Ensure `train_salary.csv` is present in the project directory
4. Launch Jupyter Notebook
        jupyter notebook
5. Run the notebook cells

## Technologies Used
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- XGBoost

## Conclusion
- Salary prediction can be effectively modeled using regression techniques
- Job title, agency, and hiring year are strong salary predictors
- Demonstrates an end-to-end machine learning workflow from EDA to modeling
