# Credit Card Fraud Detection

## Problem:

Credit card fraud can cost consumers and the financial company billions of dollars anually, and fraudsters continuously try to find new rules and tacticts to commit illegal actions. Therefore, fraud detection systems have become essential for financial institutions in order to minimize losses and improve customer experience.

## Goals:

Our goal is to leverage our data to identify fradulent transactions based on 28 variables. 

## Methodlogy:

Here, we used the Isolation Forest Algorithm and Local Outlier Factor for anomaly detections and predict outliers.
Isolation Forest is a machine learning algorithm for anomaly detection that identified anomaly by isolating outliers in the data (a.k.a. fradulent transactions in our case). The Local Outlier Factor is an unsurpervised outlier detection method which calculates the anomaly score of each outlier. 

* Advantages of Isolation Forest

It has the ability to detect anomalies pureply based on the concept of isolation without employing any distance or density measure — fundamentally different from all existing methods. It also has the ability to exploit subsampling to achieve a low linear time-complexity and a small memory-requirement, and to deal with the effects of swamping and masking effectively, which allows us to improve detection rates.

* Disadvantages of Isolation Forest

While Isolation Forest contains many advantages, it has a disadvantage in detecting local anomaly point, which affects the accuracy of the algorithm. The final anomaly score depends on the contamination parameter, provided while training the model. This implies that we should have an idea of what percentage of the data is anomalous beforehand to get a better prediction. Also, the model suffers from a bias due to the way the branching takes place. 

* Advantages of LOF

A point will be considered as an outlier if it is at a small distance to the extremely dense cluster. The global approach may not consider that point as an outlier. But the LOF can effectively identify the local outliers.

* Disadvantages of LOF
 
Since LOF is a ratio, it is tough to interpret. There is no specific threshold value above which a point is defined as an outlier. The identification of an outlier is dependent on the problem and the user.

Local outlier factor (LOF) values identify an outlier based on the local neighborhood. It gives better results than the global approach to find outliers. Since there is no threshold value of LOF, the selection of a point as an outlier is user-dependent.

## Results:

The results were 99.75% accuracy using Isolation Forest and 99.66% accuracy using Local Outlier Factor. However, F1 scores were low with an F1 score of 0.64 using Isolation Forest and 0.51 using Local Outlier Factor. Other methods must be explored to improve the results of this project.
