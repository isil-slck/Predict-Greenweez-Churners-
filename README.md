# Predict-Greenweez-Churners-

This project focuses on predicting customer churn for Greenweez, a French e-commerce company, by identifying which customers are likely to make a second purchase within 3 months of their first order.

📊 Problem Statement
Customer retention is key to e-commerce growth. Using historical sales data from 2019 to 2021, our goal is to build a predictive model that identifies potential repeat customers to support marketing and CRM strategies.

🗃️ Dataset
The dataset contains 381,398 rows and 12 columns with customer order data. It includes information like:

avg_basket: average spending per order

total_purchase_cost: total spending

nb_days_since_last_order: recency metric

re_purchase: our target (1 = repurchase within 3 months, 0 = not)

🧹 Note: Some preprocessing was done in advance — the dataset includes ready-to-use features and target.

🔍 Steps
1. 🧼 Data Exploration & Cleaning
Removed non-informative columns: orders_id, date_date

Set customers_id as index

Verified scale differences → Applied StandardScaler normalization

2. 🔢 Modeling
Split data: train_test_split (80/20)

Baseline model: predicted always “1” → Accuracy: 48%

Logistic Regression Model:

Accuracy: 73%

Precision: 75%

Recall: 65%

No signs of overfitting

3. 📊 Evaluation
Confusion Matrix and metrics showed solid results

Identified:

Customers likely to churn (≤20% probability of repurchase)

Customers at risk (20–50% probability)

📈 Business Impact
The model can be integrated into Greenweez's CRM system via ELT pipelines. Based on predictions:

CRM team targets likely churners with:

Discounts

Coupons

Personalized campaigns

This helps reduce churn and improve Customer Lifetime Value (CLV).

🛠️ Tools & Libraries
Python (pandas, sklearn, numpy)

Google BigQuery (data source)

Logistic Regression

StandardScaler (for normalization)

Matplotlib / seaborn (optional for visualization)

