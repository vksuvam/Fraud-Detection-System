# Fraud-Detection-System


 * Problem Statement:
 The company aims to analyze and enhance its current fraud detection mechanisms using
 generative AI. The goal is to accurately identify and prevent fraudulent transactions in real-time,
 adapting quickly to emerging fraud patterns while minimizing false positives that could
 inconvenience legitimate users. Key areas of concern include:

   * Data Collection and Preprocessing: Evaluating the quality and diversity of transaction
 data used for training the fraud detection models. Identifying potential gaps or biases in
 the data that could affect the accuracy of fraud detection.
   * Anomaly Detection and Pattern Recognition: Enhancing the model’s ability to detect
 anomalies and recognize complex fraud patterns in real-time. Developing techniques to
 improve the sensitivity and specificity of fraud detection algorithms.
   * User Privacy and Data Security: Ensuring that the use of generative AI adheres to
 strict user privacy and data security standards. Balancing the need for fraud detection
 with user privacy concerns.

# Prerequisites

Below packages must be installed before moving forward with the project:

![Screenshot 2024-07-14 210717](https://github.com/user-attachments/assets/c0402f57-367f-4299-ab2d-884023984e42)


Use the below command in jupyter notebook to install all the dependencies mentioned in requirements.txt.

![Screenshot 2024-07-14 210348](https://github.com/user-attachments/assets/95f08b18-3509-4a7b-a0e5-b748ebe01641)

# System Architecture

![Data Loading   Encryption](https://github.com/user-attachments/assets/8676b0c0-14a3-4362-aa8f-a79611c98590)

# Overview

* Data Loading and Encryption:
  * Load the transaction data from a CSV file.
  * Encrypt personal identifiable information (PII) like transaction_id, user_id, transaction_time to ensure data privacy.

* Differential Privacy:
  * For numerical features (like transaction_amount), some "fuzziness" is added to enhance privacy (differential privacy).

* Data Preprocessing:
  * Encode categorical features into a format a machine can understand using one-hot encoding.
  * Standardize numerical features.
  * Perform feature engineering to extract additional features like transaction_hour and transaction_day.

* Data Splitting:
  *  Split the data into training and testing sets in the ratio of 80% and 20% respectively.

* Anomaly Detection:
  * Use Isolation Forest to detect anomalies in the transaction data.
  * Isolation forest algorithm is one of the newest anomaly detection technique. It is based on the fact that anomalies are data points that are few and different. As a result of these properties, anomalies are susceptible to mechanism called isolation. 

* Pattern Recognition:
  * Train a neural network using Keras to recognize fraud patterns in the data.
  * Dense and dropout layers within the Neural network are stacked sequentially & utilises Relu activation function.
  * Model uses the Adam optimizer, binary cross-entropy loss function (suitable for binary classification), and tracks accuracy as a performance metric.

* Model Evaluation:
  * Evaluate the model's performance on the test set and generate classification reports and confusion matrices.


