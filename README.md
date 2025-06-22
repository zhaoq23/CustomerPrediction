# Smarter Retail, Smarter Customers
## A Data-Driven Approach to Customer Segmentation and Retention

<img src="https://github.com/user-attachments/assets/41768d7d-bd7b-4ca7-9687-36749f30002c" width="400"/>

# 📌 Overview
In today’s evolving brick-and-mortar retail landscape, AI and Augmented Reality are redefining customer engagement and in-store decision-making. This project presents a concrete machine learning use case—customer churn prediction—based on structured behavioral data. By embedding predictive models into interactive retail systems, we demonstrate how real-time churn risk identification can support personalized interventions and improve customer retention strategies directly at the point of sale.

# 📊 Data Preprocessing
**Data Overview**

<img src="https://github.com/user-attachments/assets/a0ddf270-0b37-4787-a76c-86f1037a750d" width="600"/>

👉 [Click here to access the Kaggle Dataset](https://www.kaggle.com/datasets/hassaneskikri/online-retail-customer-churn-dataset/code)

**Check and Transform Data Types** ✔

**Preprocessing: Deal With Missing Data**
- Due to structured nature of the dataset and minimal missingness, we handled missing data using the listwise deletion method, resulting in 7,032 records

**Preprocessing: EDA – Outlier Detection**

<img src="https://github.com/user-attachments/assets/6170baad-6489-4316-9d35-8522453e5708" width="500"/>

- To better capture customer spending behavior, we created a new feature

- 👉 AvgMonthlyCharge = TotalCharges / Tenure

<img src="https://github.com/user-attachments/assets/13fec6ac-cf39-4f7d-8630-3c663e8fbe6d" width="400"/>

- No outliers after feature engineering

<sub>

**Notes**: No outliers after feature engineering

</sub>

**Preprocessing: EDA – Outlier Detection (Isolation Forest)**

<img src="https://github.com/user-attachments/assets/61524b8d-c755-49e4-a38e-cc39e1ccf8ba" width="500"/>

👉 We need to deal with the anomalies

![image](https://github.com/user-attachments/assets/cf90bd06-b8a4-43b1-a2c5-c5512bf529d4)

**Preprocessing: EDA - Inter-Feature Correlation**

<img src="https://github.com/user-attachments/assets/9f8c3553-7ffc-4b01-823d-5a7b3b44b88e" width="500"/>

<img src="https://github.com/user-attachments/assets/cfd91d28-352c-4f2b-8ca6-980a8bf2f356" width="500"/>

**Preprocessing: EDA – DAG – Finding True Causality**

<img src="https://github.com/user-attachments/assets/f1593be5-48c2-456c-9271-454a0ddcc07b" width="400"/>

# 🧷 Feature Engineering

- Based on EDA, I created two new features: average monthly charges and tenure groups. The tenure was categorized into three bins: short-term (<1 year), medium-term (1-4 years), and long-term (>4 years). 
- Based on DAG analysis, I created interaction terms for these variable pairs: Contract * tenure and MonthlyCharges * tenure. Correlation analysis revealed that these interaction variables have meaningful explanatory power for predicting churn behavior.

# Modeling

## Preliminary Model: LASSO Logistic Regression
- I implemented logistic regression with L1 regularization (LASSO) to predict customer churn. Features were standardized and hyperparameters optimized via 5-fold cross-validation.

<img src="https://github.com/user-attachments/assets/776d01d6-adbe-4982-84cc-f57a7ee3aba4" width="300"/>

<img src="https://github.com/user-attachments/assets/f23dbacc-6c1a-4165-b07f-a2bff16565f9" width="400"/>

## Enhanced Models: Oversampled & Undersampled

<img src="https://github.com/user-attachments/assets/e3d4a18b-49fa-4ef2-af77-a2a6c93e7200" width="300"/>

## Enhanced Models: Decision Trees

<img src="https://github.com/user-attachments/assets/e9e90c45-2d87-48e1-9659-0b96b0d75d32" width="400"/>

<img src="https://github.com/user-attachments/assets/117b08fb-953c-4e0e-8464-d393ae89e66a" width="600"/>

## Enhanced Models: Random Forest

<img src="https://github.com/user-attachments/assets/e6289c1c-7aae-484a-afbf-b0738ee48d71" width="400"/>

<img src="https://github.com/user-attachments/assets/09c4de59-570f-4edc-8ebd-d7c761517c83" width="600"/>

## Enhanced Models: XGBoost

<img src="https://github.com/user-attachments/assets/9b4468f5-ae89-4963-8f6d-4488583ed803" width="400"/>

<img src="https://github.com/user-attachments/assets/df75dff2-ff9f-470f-9877-5e1c8fb53c0a" width="500"/>

# Prediction

![image](https://github.com/user-attachments/assets/335fa1db-db32-4860-8bb1-a5a173e4e4e8)

![1750618748271](https://github.com/user-attachments/assets/23292fa8-150c-4114-8518-0f1b1a59df4e)







