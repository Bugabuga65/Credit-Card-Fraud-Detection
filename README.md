# Credit-Card-Fraud-Detection
PROJECT DESCRIPTION:

It is important that credit card companies are able to detect the fraudulent credit card transactions so that the customers will not get charged for items that they did not purchased.I have done this project by detecting the anomaly using ISOLATION FOREST algorithms and LOCAL OUTLIER FACTOR ALGORITHM for my proposed model for detecting frauds in credit card system using python.

DATASET: 

I have analysed the dataset which is taken from Kaggle. link: https://www.kaggle.com/mlg-ulb/creditcardfraud The datasetis in CSV format(creditcard.csv), it contains Credit card transactions which are made by customers during September 2013 in Europe containing 284,807 transactions. Looking upon the behaviour of the transactions Credit card transactions are characterized into two categories fraudulent and non-fraudulent.Original features and more background information are not provided in the dataset because of confidentiality issues. Only numerical input variables are provided which are the results of Principal Component Analysis (PCA) Transformation. 

ISOLATION FOREST METHOD: 

This method is highly useful and is fundamentally different from all existing methods. It introduces the use of isolation as a more effective and efficient means to detect anomalies than the commonly used basic distance and density measures. Moreover, this method is an algorithm with a low linear time complexity and a small memory requirement. It builds a good performing model with a small number of trees using small sub-samples of fixed size, regardless of the size of a data set.
            How Isolation Forests Work The Isolation Forest algorithm isolates observations by randomly selecting a feature and then randomly selecting a split value between the maximum and minimum values of the selected feature. The logic argument goes: isolating anomaly observations is easier because only a few conditions are needed to separate those cases from the normal observations. On the other hand, isolating normal observations require more conditions. Therefore, an anomaly score can be calculated as the number of conditions required to separate a given observation.The way that the algorithm constructs the separation is by first creating isolation trees, or random decision trees. Then, the score is calculated as the path length to isolate the observation.

LOCAL OUTLIER ALGORITHM:
              
The LOF algorithm is an unsupervised outlier detection method which computes the local density deviation of a given data point with respect to its neighbors. It considers as outlier samples that have a substantially lower density than their neighbors. The number of neighbors considered, (parameter n_neighbors) is typically chosen 1) greater than the minimum number of objects a cluster has to contain, so that other objects can be local outliers relative to this cluster, and 2) smaller than the maximum number of close by objects that can potentially be local outliers. In practice, such informations are generally not available, and taking n_neighbors=20 appears to work well in general.

METHODOLOGY:

In order to classify the transactions as fraud or non-fraud i used some other standards of correctness which are as: 
 Precision 
 Recall 
 F1-score 
 Support 
These all standard of correctness are depend upon the Actual and Predict class, so i draw a 2×2 confusion matrix .

RESULT: 
    
Isolation Forest: 73 Accuracy Score : 0.9974368877497279 Classification Report : precision recall f1-score support
Local Outlier Factor: 97 Accuracy Score : 0.9965942207085425 Classification Report : precision recall f1-score support

OBSERVATIONS:

Isolation Forest detected 73 errors versus Local Outlier Factor detecting 97 errors vs. SVM detecting 8516 errors
Isolation Forest has a 99.74% more accurate than LOF of 99.65%.
