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
![image](https://github.com/user-attachments/assets/6170baad-6489-4316-9d35-8522453e5708)
- To better capture customer spending behavior, we created a new feature:👉 AvgMonthlyCharge = TotalCharges / Tenure

![image](https://github.com/user-attachments/assets/13fec6ac-cf39-4f7d-8630-3c663e8fbe6d)
- No outliers after feature engineering

<sub>

**Notes**: No outliers after feature engineering

</sub>

