# 📊 Customer Churn Prediction

## 📌 Overview  
This project predicts employee churn (leave or stay) using machine learning. It covers data preprocessing, exploratory data analysis (EDA), feature engineering, model building, evaluation, and insights for actionable recommendations.  

## 📂 Dataset  

- **Records:** ~15,000 employees  
- **Satisfaction level**   | (int64) | The employee’s self-reported satisfaction level [0-1]
- **last evaluation**      | (int64) | Score of employee's last performance review [0–1] 
- **number of project**    | (int64) | Number of projects employee contributes to
- **average monthly hours**| (int64) | Average number of hours employee worked per month
- **time_spend_company**   | (int64) | How long the employee has been with the company (years)  
- **work_accident**        | (int64) | Whether or not the employee experienced an accident while at work 
- **left**                 | (int64) | Whether or not the employee left the company 
- **promotion_last_5years**| (int64) | Whether or not the employee was promoted in the last 5 years
- **Department**           | (str)   | The employee's department
- **salary**               | (str)   | The employee's salary (low, medium, or high)



## 🔎 Exploratory Data Analysis (EDA)  
In the EDA notebook, the following steps were performed:  

- **Data inspection**: Checked dataset shape, data types, missing values, and duplicates.  
- **Descriptive statistics**: Summarized distributions of numerical and categorical variables.  
- **Correlation analysis**: Generated a heatmap to examine feature relationships.  
- **Churn distribution**: Analyzed imbalance between employees who stayed vs. those who left.  
- **Feature relationships**:  
  - Churn vs. salary levels  
  - Churn vs. department  
  - Churn vs. workload (number of projects, average monthly hours)  
  - Churn vs. satisfaction level and evaluation score  
- **Encoding**: Converted `salary` to ordinal categories (low, medium, high) and one-hot encoded `department`.  

These steps provided key insights into employee churn patterns and guided feature engineering for model building.  


## 📊 Key Insights  
- **Workload impact**: Employees with many projects and long average monthly hours are more likely to leave.

- **Satisfaction level**: Employees with low satisfaction show a much higher churn rate.

- **Evaluation score**: Both very low and very high evaluation scores are linked with churn → suggesting overwork or disengagement.

- **Tenure effect**: Employees with around 4 years of service have a spike in attrition, indicating a critical retention point.

- **Salary**: Churn is higher among employees with low salary, but salary alone is not the strongest driver compared to satisfaction/workload.

- **Department**: Some departments (e.g., support, sales) have higher churn rates than others.

## 🛠️ Tools & Technologies  
- **Programming Language**: Python 

- **Data Manipulation & Analysis**: pandas, numpy

- **Data Visualization**: matplotlib, seaborn

- **Machine Learning**: scikit-learn (Logistic Regression, Random Forest), XGBoost

- **Environment**: Anaconda, Jupyter Notebook

## 📁 Project Structure  
Customer_Churn_Prediction/
│── data/             # Raw dataset
│── notebooks/        # Jupyter notebooks (EDA, Forecasting, etc.)
│── results/          # Exported plots & metrics
│── dashboard/        # Power BI or Streamlit dashboard
│── requirements.txt  # Python dependencies
└── README.md         # Project documentation


# How to Run
1. Clone this repository:
git clone https://github.com/your-username/Sales_EDA_Dashboard.git
cd Sales_EDA_Dashboard

2. Install dependencies
pip install -r requirements.txt

3. Open Jupyter Notebook
jupyter notebook

# Results

**Baseline Model – Logistic Regression**  
- **Accuracy:** 0.82  
- **Precision:** 0.44 (churn), 0.86 (stay)  
- **Recall:** 0.26 (churn), 0.93 (stay)  
- **F1-score:** 0.33 (churn), 0.90 (stay)  
- **ROC-AUC:** ~0.75  

**Confusion Matrix:**  

|                  | Predicted Stay | Predicted Leave |
|------------------|----------------|-----------------|
| **Actual Stay**  | 2165           | 156             |
| **Actual Leave** | 348            | 123             |

**Interpretation:** The model projects the “Stay” group very well, but still misses many employees who are likely to leave.

# Bussiness insight

# 📌 Business Insight

From the EDA and model results, several key insights emerged:

- **Overwork is a critical churn factor**: Employees handling too many projects or working excessive hours show higher churn rates.

- **Satisfaction is strongly tied to retention**: Low satisfaction scores are consistent among employees who left.

- **Tenure matters**: Employees with around four years at the company often report dissatisfaction and are more likely to leave.

- **Evaluation bias**: High performance evaluation alone does not guarantee retention if workload balance and recognition are lacking.

- **Salary level impact**: Lower-salary employees show a stronger tendency to leave compared to medium or high salary groups.

# 💼 Business Value

Reducing employee churn has significant business impact:

- **Lower Recruitment & Training Costs**: Retaining employees helps avoid the high costs of hiring and onboarding new staff.

- **Increased Productivity**: Experienced employees contribute more effectively to projects and require less supervision.

- **Improved Employee Morale**: A stable workforce fosters a healthier work culture and reduces the risk of burnout.

- **Better Strategic Planning**: Understanding churn patterns allows HR to design data-driven policies for promotions, workload management, and employee engagement.

- **Long-Term Growth**: Minimizing turnover strengthens institutional knowledge and supports sustainable company growth.

# Next Steps

- Model Improvement:
    - Train Random Forest and XGBoost models.**

    - Hyperparameter tuning for better performance.**

    - Address class imbalance with resampling or SMOTE.

- Feature Engineering:

    - Explore new features and test removing last_evaluation to avoid leakage.

- Business Application:

    - Build an HR dashboard to monitor churn risk.

    - Simulate intervention policies (promotion, workload capping, communication).
# Author
HaNguyenMinhTam - Data Scientist Enthusiast
- Email: hnmt@gmail.com
- Github: https://github.com/HaNguyenMinhTam

