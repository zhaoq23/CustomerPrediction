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
- To better capture customer spending behavior, we created a new feature:👉 AvgMonthlyCharge = TotalCharges / Tenure

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





