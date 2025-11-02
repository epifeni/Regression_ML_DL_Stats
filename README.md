# Machine Learning/Deep Learning Model Notes  

Machine Learning Cheat-Sheet  
<img width="714" height="408" alt="image" src="https://github.com/user-attachments/assets/1fb278f1-de5d-449f-b482-2466a349e44b" />   

## <u>Supervised Learning</u>  

Machine learing process for supervised learining  
<img width="951" height="302" alt="image" src="https://github.com/user-attachments/assets/04cd0896-5b56-42eb-9fec-0f3f77bc13eb" />

### Classification Error Performance Evaluation
* Model tires to predict categorical values (i.e. dog/cat, spam/not-spam)
* **Accuracy** in classification porblems is the **number of correct predictions** made by the model divided by the **total number of predictions**. How many prediction did you get right as a percentage?
  * Accuracy is a good indicator of model performance on balanced data only
* **Recall** is the ability of a model to find all the relevant cases within a dataset
  * Expresses the ability of finding all the relevant instances in a dataset
  * = Number of true positives / (number of true positives {correct positive predictions} + number of false negatives {incorrect positive predictions})
* **Precision** of a classification model is to identify only the relevant data points
  * Expresses the propotion of the datasets our model says was relevant that actually were relevant
  * = Number of true positives / (number of true positives + number of false positives {incorrectly classifed as positive})
* **F1 Score** finds the optimal blend of precision and recall
* * The harmonic mean of precision and recall
  * = 2 X [(precision * recall) / (precision + recall)]
   * Harmonic mean punishes extreme differences between precision and recall

#### Confusion Matrix - Compares the predicted values to the true values
<img width="851" height="400" alt="image" src="https://github.com/user-attachments/assets/4176ae46-8a37-45d7-ab33-c6eeb49f5f27" />  

#### Correct Predictions
* *True positive* - the person having the disease and the model correctly predicting that they have the disease
* *True negative* - the person not having the disease and the model correctly predicting that they do not have the disease
#### Incorrent Predictions
* *False positive* (Type 1 Error) - the person does not have the disease by the model inaccurately predicts taht they do have the disease. The model is falsely saying the person is positive for the disease
* *False negative* (Type 2 Error) - the person does have the disease but the model inaccuraetly predicts that they do not have the disease.

#### Calculations
<img width="815" height="432" alt="image" src="https://github.com/user-attachments/assets/4d6b1f79-2a40-4da2-a2fa-dcd2e461e457" />  

### Regression Error Performance Evaluation  
* Model tries to predict continuous values
* Error: true value - predicted value
* **Mean Absolute Error** - Compare predictions to the true y-label
  * This is the mean of the sum of the absolute value of errors
  * Issue - will NOT punish large errors
* **Mean Squared Error** - The mean of the squared errors
  * Squaring the error punished larger outliers more than the Mean Absolute Erros
  * The model punishes outliers
  * Issue - Squaring the error also squares the units as well which is difficult to interpret (i.e. $ squared)
* **Root Mean Squared Error** - Takes the square-root to fix the issue with Mean Squared Error
  * Compare the Root Mean Squared Error to the mean values to get an idea of significance

## <u>Unsupervised Learning</u>  
Machine learning process for unsupervised learning
<img width="926" height="134" alt="image" src="https://github.com/user-attachments/assets/3919cd9e-2131-4259-b56c-3dc2ab515521" />

* There is no Test/Train split
  * So, train ad fit the model on all the data and afterwards, perform some sort of transformation on the data set such as Dimentionality Reduction
* No historical labels
* Raw data  with no lables
* **Clustering** - Group together **unlable** datapoints into categories or clusters
  * Data points are assigned to a cluster based on the similarity to other points within that cluster
* **Anomaly Detectection** - Attempts to detect outliers in a dataset (i.e. fraudulent transactions on a credit card)
* **Dimentionality Reduction** - Reduce the number of features in a dataset

# Artificail Neural Networks



