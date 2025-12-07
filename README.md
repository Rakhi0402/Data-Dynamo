# Data-Dynamo
Retail Risk Prediction Model
# Data-Dynamo
Retail Risk Prediction Model

This project predicts whether an e-commerce order will be returned by the customer.
Using machine learning models, the system analyzes order details such as price,
discount, product category, customer information, and region to provide a return
risk score.

Dataset:We took the dataset from kaggle,it consists of features : order_id,customer_id,product_id,category,price,discount	quantity,payment_method,order_date,delivery_time_days,region,returned(label),total_amount,shipping_cost,profit_margin	customer_age,customer_gender.

For pre-processing: As the dataset we chose has a problem of class imbalance we would use SMOTE to balance the classes as there is binary classification,and we would use encoding for different features that has alphabetical values.

For models: we would be using 4 models: logistic regression, XGboost,Neural Network,SVM. We would be using confusion matrix,precision,recall,f1-score and accuracy as your result metrices

