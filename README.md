# **CREDIT RISK ANALYSIS**

## **Overview of The analysis**

This project employs six different machine learning models and provide analysis on its balance accuracy, precision and sensitivity scores as a means of evaluating the model performance or ability to predict credit risk. The six machine learning algorithms used are Random Oversampling, SMOTE Oversampling, Cluster Centroids Undersampling, Combination Sampling(SMOTEENN), Balanced Random Forest Classifer and Easy Ensemble AdaBoost Classifier. 

## **Results**

The scores analyzed are  the balance accuracy score, precision and sensitivity scores of the data sample. Below is a brief description of what they test for. 
- Balance Accuracy Score measures the accuracy of a model in predicting a positive classification when an imbalance technique is used to correct the data representation. 
- Precision score measures how likely a target can occur or how reliable a positive classification is.  
- Sensitivity Score (Recall) measures how well a model can predict a positive classification.

### **Naive Random Oversampling Results**

This technique increases the minority class in an attempt to balance the dataset by randomly selecting instances in the minority class and adding it to the training set. From the image below, the balanced accuracy score for the dataset was 0.6403. Its precision score for high risk was 0.01 and 1.0 for low risk. This shows the model is more reliable in predicting low risk instances than high risk. The recall score is 0.66 for high risk and 0.62 for low risk.

![Random Oversampling](/Images/oversampling.png)

### **SMOTE Oversampling Results**
This oversampling technique is used to deal with unbalanced datasets by increasing the size of the minority class in the dataset by interpolating the data points. From the model analysis, the balance accuracy score is 0.6515 which is a better score than the random oversampling. Precision scores for high and low risk were 0.01 and 1.00 respectively, same as oversampling approach. In contrast, the recall score for the SMOTE approach yielded a lower score (0.61) in predicting a positive classification of high risk application than random sampling.

![SMOTE Oversampling](/Images/SMOTE_oversampling.png)

### **Undersampling Results**

This model reduces the size of the majority class by removing instances from the majority class within the dataset. The undersampling technique used in this analysis is the cluster centroid undersampling, which creates synthetic points of the majority class and reduce it to the size of the minority class. From the results, precision remained the same, high risk recall is 0.61, and the model balance accuracy is 0.6512. It appears that the undersampling and SMOTE oversampling yielded similar results.

![Cluster Centroid Undersampling](/Images/undersampling.png)

### **Combination Sampling Results (SMOTEENN)**

As the name suggest, this model combines oversampling and undersampling approaches. The model oversample the minority class using the SMOTE approach and then clean the sample data by dropping nearest neighbors of a data point that belongs to both majority and minority classes. From the image displayed below, this model yielded the best score for all the sampling techniques. it shows a slightly higher balanced accuracy of 0.6551, and a higher recall of 0.75 for high risk. 

![Combination Sampling](/Images/combination_sampling.png)

### **Balanced Random Forest Classifier**

This model samples the data and creates smaller and simpler decision trees. From the image below, balance accuracy is 0.7885, precision is 0.03 for high risk and 1 for low risk, and recall of 0.70 for high risk and 0.87 for low risk.

![Random Forest Classifier](/Images/BRFC.png)

### **Easy Esembler AdaBoost Classifier**
In this model, subsequent models are trained after previous models are evaluated and errors from the previous model are weighted to minimize them in the subsequent models.From the image below, this model generated a high balanced accuracy score of 0.9317, and recall for high and low risk of 0.92 and 0.94 respectively. The precision score was higher for low risk instances.

![Easy Essembler AdaBoost Classifier](/Images/EEAC.png)

## **Summary**

In all the sampling models, the precision score remained the same for both high risk and low risk at 0.01 and 1 respectively. The balance accuracy and sensitivity score however, differs. The classifiers on the other hand yeilded same precision score for low risk but different for high risk. Also, The analysis showed that the classifiers has a higher balance and recall score than sampling models. The Easy Essemble AdaBoost yielded the best scores in predicting a positive classification, the reliabilty of a positive classification and also accuracy of the model. 
Even though the Easy Ensemble AdaBoost yielded the best scores, it is still insufficient to accept the model for prediciting credit risk. This is because the precision score, which is how likely a target can occur, is very low for predicting high risk applications. The model is good for predicting low risk applications but appears unreliable for high risk applications due to the high false positives. 
