# Data Science Documentation for Machine and Deep Learning

# Probability Distributions
## Continuous Probability Distributions - Probability Density Functions
### **Normal Distirbution** - Most relevant to business decissions
 * *If a population approximate a standard normal distribution, then we can make some powerful inferences about it once we know its Mean and Standard Deviation - Using a Z-table*
 * Population Standard Deviation describes what you already know - How wodely individual values stray from the population mean
    * Bell Curve or Gaussian Dristibution
    * All Normal curves:
     * Is symmetrical about the mean
     * 99.73% of values fall under 3 Standard Deviaitons
     * Mean does not have to equal 0 and Standard Deviation does not have to equal 1
    * Normal distributions are symmetrical
    * Not-Normal distributions display an asymmetrical skew
    * Probablity of any specific outcome is zero
    * Probabilites can only be calculated over a range of outcomes
    * In a normal distribution - mean, median and mode are all equal to the same value
     * **Standard Normal Distribution** - is a special case where the mean = zero and it's Standard Deviation = 1
      * 68.27% of all values fall under +or- 1 Standard Deviatoin
      * 96.45% of all the values fall under +or- 2 Standard Deviations
      * 99.73% of all the values fall under +or- 3 Standard Deviations

## Less popular distributions
### Exponential Distribution
### Beta Distribution

## Discrete Probability Distributions - Probability Mass Functions (Binomial Distribution)

# Statistics
* Population - every member of a group we want to study
* Sample - small set of random members of the population
*    * Approximately 30 or greater random sample will almost always reflect the populaiton
     * Bias in sampling
         * **Selection Bias** - favours members of a population that are more inclined or able to answer polls (more willing to respond the the sampling technique)
            * Undercoverage Bias - making too few observations or omitting entire segments of a population
            * Self-selection Bias - people who volunteer may differ significantly from those in the population who don't
            * Healthy-user Bias - sample may come from a helthier segment of the population
         * **Survivorship Bias** - If a population moves over time, it may be due to lessor members leaving the population due to death, expulsion, erlocation etc.
* Parameter - charisteristic of a population
* Statistic - is a characteristic of a sample

*From a **Population** of voters, we can gather a **Sample**. We calculate a **Statistic** from the sample that lets us estimate a **Parameter** of the population.*

* Apply **Statistical Inference** to the **Sample** in an attempt to describe the population
* Variable - a charisteristic that describes a member of the sample
     * Discrete - gender, birthplace
     * Continuous - age, salary
## Types of Sampling
* Random - every member of a population has an equal chance of being selected
   * Since samples are smaller than populations, there is a chance that entire demographics might be missed
* Stratified Random - ensures that groups within a population are adiquately represented
*    * Divide the pupulation into segments based on some charisteristics
     * Take random samples from each group
     * Size of each sample is based on the size of th group realtive to the population
* Cluster - break the population down into groups and sample a random selecton of groups, or *clusters*

## Central Limit Theorem
* 95% of all sample means shold fall within 2 Standard Deviations of the population mean even if the population itself is not normally distributed
<img width="927" height="420" alt="image" src="https://github.com/user-attachments/assets/d22afed3-27c1-44a7-8e13-6ddf5f15b562" />

# Standard Error  
Describes how far a **sample mean** stray from the **population mean**  
Takes both the sample and population into consideration
* N = # of population members
* n = # of sample members
* P = population parameter
* p-hat = sample statistic
* Sigma = population standard deviation
* SE_sub_p-hat = standard error of the sample

We can say that with a 95% **confidence level** that the **populaiton parameter** lies within a **confidence interval** of plus-or-minus 2 **Standard Errors** of the **sample statistic**
* Standard Error describes how a sample statistic varies from the population parameter. It **does not** describe how individual values deviate within the statistic (this would just be the standard deviation of the sample)
* We can say that the sample statistic (p-hat) is a **point estimator** of the population parameter P
<img width="757" height="429" alt="image" src="https://github.com/user-attachments/assets/8787fa23-0b98-4612-8e21-ef8958225be2" />

# Hypothesis Testing  
**We never "PROVE" a hypothesis. We only can **reject** OR **fail to reject** the null hypothesis  
The application of statistical methods to real-world questions  
* We start with a null hypothesis (the **an ssumption**). Then we run an expriment to test his null hypothesis
* Based on the results of the experiment, we either **reject** or **fail to reject** the null hypothesis
* If the null hypothesis is rejected, then we say that the data supports another, mutually exclusive **alternative hypothesis**

## Framing the Hypothesis
* At the start of the experiment, the null hypothesis is assumed to be true. It is upto the experiment to to **reject** or **fail to reject** the null hypothesis
* If the data fails to support the null hypothesis, only then can we look at an alternative hypothesis
* **null hypothesis should contain some kind of equality (=, <=, >=)**
* **alternative hypothesis should **not* have an equality (not = to, <, >)**

## Testing the Hypothesis
* Assuming out null hypothesis is valid, if the probability of observing these results of the null hypothiesis (after recording the results) is very small (inside of 0.05 - **The Level of Significance [alpha]**), then we reject the null hypothesis\
  * i.e. Given an assumption, the probability of a particular observed event is exceptionally small, then you can conclude that the assumption is probaby not correct\
* If alpha = 0.05 and the alternative hypothesis has an alpha that is **less than* the null hypothesis, then the **left-tail** of the probability curve has an area of 0.05\
<img width="343" height="221" alt="image" src="https://github.com/user-attachments/assets/b0cb61a3-b6cd-4d2f-bab7-b52c539e1a2f" />
* If alpha = 0.05 and the alternative hypothesis has an alpha that is **more than* the null hypothesis, then the **right-tail** of the probability curve has an area of 0.05\
<img width="290" height="228" alt="image" src="https://github.com/user-attachments/assets/d0c84b0f-8a6f-43d6-89af-7bed40201a8a" />
* If alpha = 0.05 and the alternative hypothesis has an alpha that is **not equal to* the null hypothesis, then the two tales of the probability curve **share** an area of 0.05 (H1 not= null)\  
<img width="539" height="60" alt="image" src="https://github.com/user-attachments/assets/00e6180e-2831-410a-8718-2526905cdb7a" /> 
* These areas establish the **critical values** or Z-scores\  
<img width="575" height="235" alt="image" src="https://github.com/user-attachments/assets/d8976ee0-c177-4563-b597-41a0d9967ecf" />  

## 2 Types of Tests - Test of Means and Test of Propotions
* Each has it's own test statistic to calculate
* **Tests of Mean** - Looking to find an **average**, or specific value in a population
* **Test of Propotion** - Looking at a percentage of the population does 'X'. Trying to extablish an hypothesis when dealing with a propotion of the population

### Calculating Test Statistics
* When working with mean\
<img width="624" height="134" alt="image" src="https://github.com/user-attachments/assets/151ab9c9-7959-4ba9-b8d8-54852c87a1f9" />
* When working with populations\
<img width="509" height="161" alt="image" src="https://github.com/user-attachments/assets/5eb77b53-157f-4094-b084-0ae4cab403fb" />

## 2 Ways of Performing Hypothesis Tests  
### Traditional Test
1. Take the level of significance (alpha)  
2. Use it to determine the critical value  
3. Compare the test statistic to the critical value

### Traditional Test Setup
1. State the null hypothesis
2. State the alternative hypothesis
3. Set a level of significance (alpha)
4. Determine the test type (left tail,  right tail or two tail based on the null an alternative hypothesis)\
<img width="550" height="134" alt="image" src="https://github.com/user-attachments/assets/62461180-91c7-4e11-8cec-ea0e343b8e7c" />
5. Calculate the test statistic (using the Z formula)\
<img width="171" height="105" alt="image" src="https://github.com/user-attachments/assets/1046c2b4-346d-49b0-80de-5dd6e27eae4d" />
6. Calculate Critical Value
   * Do a z-table lookup of the alpha value to get the z value
7. Check if the value Rejects or Fail to Reject the null hypothesis

### P-value Test
1. Take the test statistic (Z-value)
2. Use it to determine the P-value
3. Compare the P-value to the level of significance (alpha)

### Traditional Test Setup
1. State the null hypothesis
2. State the alternative hypothesis
3. Set a level of significance (alpha)
4. Determine the test type (left tail,  right tail or two tail based on the null an alternative hypothesis)\
<img width="550" height="134" alt="image" src="https://github.com/user-attachments/assets/62461180-91c7-4e11-8cec-ea0e343b8e7c" />
5. Calculate the test statistic (using the Z formula)\
<img width="171" height="105" alt="image" src="https://github.com/user-attachments/assets/1046c2b4-346d-49b0-80de-5dd6e27eae4d" />
6. P-Value
   * z-table lookup to get the p value
7. Check if the value Rejects or Fail to Reject the null hypothesis

**"If the P-value is low, the null must go!"* --> Reject null hypothesis
**"If the P-value is high, the null must fly!"* --> Fail to reject null hypothesis  

# Type 1 and Type 2 Errors
Used when you already know the truth that you are testing for wher you already know if the null hypothesis is TRUE or FALSE\
* Type 1 Error (Fasle Positive) - **Rejecting** a null hypothesis that should have been supported
    * Null hypothesis was that there was no fire. There was actually no fire but you pulled the fire alarm anyway
* Type 2 Error (False Negative) - **Failing to Reject** reject a null hypothesis that should have been rejected
    * Null hypothesis was that there was no fire. So you fail to pull the fire alarm when there was actually a fire 

## Student's T-Distribuiton
Uses when the population Standard Deviation is not known
* Determines if there is a significant difference between two sets of data
* When due to variance and outliers, it's not enough just compare mean values
* T-test also considers sample variances

### Types of Student's T-Test
* One-sample t-test - Tests the null hypothesis that the populatin mean is equal to a specified value $\mu$ based on a sample mean $\bar{x}$
*    * Check if the sample mean equals populaiton mean without knowing the Standard Deviation of the population
t-statistic\
<img width="473" height="304" alt="image" src="https://github.com/user-attachments/assets/74ca8d02-bb4f-4e38-b072-dc691bb38314" />

* Independent two-sample t-test - Tests the null hypothesis that two sample means $\bar{x1}$ and $\bar{x2}$ are equal
     * Check if the mean test scores of two seperate samples of students have a statistically significant difference
<img width="892" height="298" alt="image" src="https://github.com/user-attachments/assets/b141a927-e928-49be-9b46-ae9f5348fa27" />

t-statistic depends on 3 scenarios\
* Equal  sample size, equal variance
* Unequal sample size, equal variance
* Equal orunequal sample sizes, unequal variance (**Most Common - AKA Welch-Satterthwaite Formula**)
<img width="659" height="224" alt="image" src="https://github.com/user-attachments/assets/2c341383-8ee0-46ef-9360-8a9355ddd95b" />
   * General formula when variences of the samples are close enough to being equal
<img width="317" height="52" alt="image" src="https://github.com/user-attachments/assets/833a7b61-4acd-4fd3-b4a1-a2fb72e7adbd" />

* Dependent, paired-sample t-test - Used when samples are dependent
     * One sample has been tested twice (repeated measurements)
     * two sampels have been matched or paired
     * Check if the same group of students have improved results on the test scores  before prep couse and after prep course

t Vs z distribuiton\
t distribution approaches the z distribution as the degrees of freedom increase - i.e. if the sample size is big enough, use the normal distribution (n = 30 is a standard cut-off point to switch over to a normal distribution)
<img width="876" height="278" alt="image" src="https://github.com/user-attachments/assets/5af5b91f-6f45-4e09-b847-561fd854d828" />


# Machine Learning/Deep Learning Model Notes  

[Machine Learning Cheat-Sheet](https://scikit-learn.org/stable/machine_learning_map.html)

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

# Deep Learning

## Perceptron Model
<img width="929" height="296" alt="image" src="https://github.com/user-attachments/assets/1fcfa38d-deaf-408a-9066-881d7c1dd5d9" />
1. if f(X) is a sum then, y = x1 + x2\

2. There is no way that this model can work, so we can add in adjustable weights to multiply against the inputs of x\
<img width="935" height="250" alt="image" src="https://github.com/user-attachments/assets/5427b94b-69d5-4854-8ce8-0cb7116f72c6" />
Now y = x1w1 + x2w2\
weight can be updated to affect the output y\

3. In the case that the impt values are zero, we can add a bias term b to the input
    * The way to think about the bias is that the multiplication of (x1 * w1) i.e. the input times its weights has to overcome the bias value in order to have an affect on the output of y
<img width="946" height="278" alt="image" src="https://github.com/user-attachments/assets/cf78e8c9-81da-4e1a-8822-44f2084c1047" />
Now y = (x1w1 + b) + (x2w2 + b)\

4. Inputs can be expanded out all the way to n number of inputs\
<img width="924" height="308" alt="image" src="https://github.com/user-attachments/assets/61c26984-e0f2-4781-a154-c5f26208f342" />

5. This model can be expanded to have X be a **tensor** of information, where a tensor is an n-dimentional matrix\
<img width="528" height="211" alt="image" src="https://github.com/user-attachments/assets/1c44b112-be48-40ae-b6b1-835bd21ddad1" />

6. This equation can be simplified by adding up all the biases into one bias labeled B\
<img width="907" height="307" alt="image" src="https://github.com/user-attachments/assets/6356480c-6ab5-429f-a97e-3f95cb8fdb3e" />

 











