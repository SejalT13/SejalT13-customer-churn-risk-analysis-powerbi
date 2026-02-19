# Customer Churn Risk & Revenue Impact Analysis

##  Project Overview

This project builds an end-to-end Customer Churn Prediction system using Machine Learning and translates churn probability into business-focused revenue exposure insights using Power BI.

The objective is not just to predict churn, but to quantify financial risk and support targeted retention strategies.

---

##  Business Problem

Customer churn directly impacts recurring revenue in subscription-based businesses.

The goals of this project are to:

- Predict churn probability for each customer  
- Segment customers into risk categories  
- Estimate expected revenue exposure  
- Provide actionable insights for retention teams  

---

##  Tools & Technologies Used

- Python (Pandas, NumPy, Scikit-learn)
- Logistic Regression
- Random Forest
- Power BI
- DAX
- GitHub

---

##  Dataset

The Telco Customer Churn dataset includes:

- Customer demographics
- Service usage details
- Contract and billing information
- Churn status

---

##  Data Preparation

Key preprocessing steps:

- Converted `TotalCharges` to numeric and handled missing values
- Encoded categorical variables for model training
- Preserved original categorical columns for dashboard usability
- Split dataset into training and testing sets (80/20)

Two dataset versions were created:

1. Encoded dataset → for ML training  
2. Clean categorical dataset → for Power BI dashboard  

---

##  Machine Learning Approach

### Models Trained
- Logistic Regression  
- Random Forest  

### Model Performance

| Model | Accuracy | ROC-AUC |
|--------|----------|----------|
| Logistic Regression | ~78% | **0.83** |
| Random Forest | ~78% | 0.81 |

### Final Model Selected:
Logistic Regression

### Reason for Selection:
- Higher ROC-AUC score  
- Better probability calibration  
- More interpretable for business stakeholders  

---

##  Risk Segmentation Strategy

Churn probability was segmented into:

- High Risk (≥ 0.7)
- Medium Risk (0.4 – 0.7)
- Low Risk (< 0.4)

This enables targeted retention strategies.

---

##  Revenue Exposure Calculation

Revenue at Risk was calculated using:

MonthlyCharges × Churn Probability

This provides expected revenue exposure instead of only historical churn counts.

---

##  Key Insights

- Month-to-month customers show significantly higher churn rates.
- Electronic check users represent the highest revenue exposure.
- Approximately 6–7% of customers fall into the High Risk category.
- Overall churn rate is approximately 26%.

---

##  Power BI Dashboard Overview

The dashboard includes:

- Total Customers  
- Churn Rate %  
- High Risk Customers  
- Revenue at Risk  
- Churn Rate by Contract Type  
- Revenue Exposure by Payment Method  
- Customer Risk Segmentation  

---

##  Dashboard Preview

Example:
<img width="881" height="495" alt="image" src="https://github.com/user-attachments/assets/70f6e1ed-73df-4b27-aaf7-38baaf0f404a" />


---

##  Business Impact

This solution enables organizations to:

- Identify high-risk customers proactively  
- Prioritize retention campaigns  
- Optimize contract and payment strategies  
- Protect recurring revenue  

---

##  Repository Structure

customer-churn-risk-analysis-powerbi/
│
├── data/
│   └── churn_dashboard_dataset.csv
│
├── notebook/
│   └── churn_model.ipynb
│
├── dashboard/
│   └── Customer_Churn_Risk_Dashboard.pbix
│
├── images/
│   └── dashboard_preview.png
│
└── README.md

---

##  What This Project Demonstrates

- End-to-end ML workflow  
- Model evaluation and selection  
- Probability-based risk modeling  
- Revenue-focused analytics  
- Executive dashboard storytelling  

---
