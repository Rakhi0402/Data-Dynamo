
# Data-Dynamo
Retail Risk Prediction Model

This project predicts whether an e-commerce order will be returned by the customer.
Using machine learning models, the system analyzes order details such as price,
discount, product category, customer information, and region to provide a return
risk score.

Dataset:We took the dataset from kaggle,it consists of features : order_id,customer_id,product_id,category,price,discount	quantity,payment_method,order_date,delivery_time_days,region,returned(label),total_amount,shipping_cost,profit_margin	customer_age,customer_gender.The dataset contained 34500 rows and 15 columns the link for the dataset is : 

For pre-processing: As the dataset we chose has a problem of class imbalance we would use SMOTE to balance the classes as there is binary classification,and we would use encoding for different features that has alphabetical values. After the pre-processing we split the dataset into 2 parts: training and testing, the size of training dataset was 52156 and for testing it was 13038.The pre-processed data set is uploaded

For models: we would be using 4 models: logistic regression, XGboost,Neural Network,SVM. We would be using confusion matrix,precision,recall,f1-score and accuracy as your result metrices.
Neural Network: During the implementation of the neural network first we found out the correlation between the result and the different features and according to the values of correlation we used the weight according to the correlation values we gave the weight to the neural network.It builds a deep neural network with multiple Dense, BatchNormalization, and Dropout layers to prevent overfitting and improve training stability. The model is trained using the Adam optimizer with binary cross-entropy loss, while EarlyStopping and ReduceLROnPlateau automatically stop training when validation performance stops improving and reduce the learning rate when training slows down. After training, the model predicts probabilities for the test data, and instead of using the standard 0.5 threshold, the code finds the best classification threshold by computing precision-recall values and choosing the one that gives the highest F1 score. Finally, it converts probabilities to class labels and prints key performance metrics—accuracy, precision, recall, and F1 score—to evaluate how well the model predicts product returns. The result of the model is in the notebook file uploaded.
Out of all the models we ran XGBoost gave the best accuracy so we used that model for our UI as it was the best one.

For UI: Gradio is a Python library that lets us quickly create a simple web interface for our machine-learning model. In this project, we use Gradio to build an interactive UI where users can enter order features in a table and instantly get the predicted return probability from our trained XGBoost model. It helps connect our backend model to a clean, user-friendly frontend without writing any HTML or backend code.

The pynb file for each is uploaded on the github repository.

