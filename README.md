# telco-customer-churn-prediction
Customer Churn Prediction System developed using Machine Learning techniques to identify customers who are likely to discontinue a telecom service.
# Customer Churn Prediction (Telco Dataset)

## Overview
This project predicts customer churn for a telecommunications company using machine learning.  
The goal is to identify customers most at risk of leaving and provide actionable business recommendations to reduce churn.  

## Dataset
- **Source:** [Telco Customer Churn (Kaggle)](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)  
- **Size:** 7,043 customer records  
- **Target Variable:** `Churn` (`Yes`/`No`)  
- **Features:** Demographics, tenure, contract type, monthly charges, total charges, payment method, internet and support services  

## Methodology
1. **Exploratory Data Analysis (EDA)**  
   - Checked churn distribution  
   - Explored numerical feature relationships using correlation analysis  
   - Used boxplots to examine churn patterns across tenure, monthly charges, and total charges  
   - Identified important churn-related categorical features after encoding  

2. **Preprocessing**  
   - Cleaned missing and invalid values in `TotalCharges`  
   - Converted `Churn` from `Yes/No` to `1/0`  
   - Encoded categorical variables with one-hot encoding  
   - Train-test split using **80/20**  
   - Scaled features with `StandardScaler`  

3. **Modeling**  
   - Logistic Regression with `class_weight="balanced"`  
   - Custom classification threshold of **0.48** to improve churn detection  

4. **Evaluation**  
   - Metrics: Accuracy, Precision, Recall, F1-score, ROC-AUC  
   - Confusion matrix  
   - Classification report  

## Results
- **Accuracy:** `74.31%`  
- **ROC-AUC:** `0.8619`  
- **Churn Recall:** `0.85`  
- **Churn Precision:** `0.51`  

At the chosen threshold of **0.48**, the model detects most churners while keeping precision at a usable level for retention-focused decisions.  

## Business Insights
- **Contract Type:** Customers on longer-term contracts are less likely to churn.  
- **Tenure:** Customers with shorter tenure are at the highest risk of churn.  
- **Charges:** Higher monthly charges are associated with higher churn risk.  
- **Key Drivers:** Tenure, contract type, fiber optic internet service, electronic check payment method, and support-related services.  

### Recommendations
- Encourage customers to move from short-term to long-term contracts.  
- Target early-tenure customers with retention campaigns.  
- Monitor customers with high monthly charges more closely.  
- Offer value-added support services and incentives to high-risk customers.  

## Next Steps
- Incorporate customer satisfaction and feedback data into future datasets.
- Evaluate advanced machine learning algorithms such as XGBoost and LightGBM.
- Implement Explainable AI techniques such as SHAP for improved interpretability.
- Develop automated retention recommendation systems based on customer risk levels.
  

## How to Run This Project
1. Open [Google Colab](https://colab.research.google.com/).  
2. Upload the notebook `Telco-Customer_Churn_Prediction.ipynb` and the dataset CSV.  
3. Run all cells to reproduce the analysis, model training, and saved artifacts.  

---
