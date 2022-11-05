# Credit-card-default-prediction
## Business Problem
Credit cards are one of the key business areas within the banking industry, and have gained huge success in the past few years. Banks often issue credit cards to ineligible customers without sufficient background checks in an effort to increase their market share. Additionally, many customers overused their credit cards, resulting in high debt accumulation. One of the biggest challenges banks face is identifying risks and non-risks among customers. So, the problem we are trying to analyze is how to identify the risky and non-risky customers, helping the bank to decide if a customer has the potential to repay the used credit of the bank.
## 2. Approach
● Null values Treatment

Thankfully our dataset contains no missing values and duplicate values. so there was no need to remove or impute them.

● Encoding of categorical columns

We used One Hot Encoding to produce binary integers of 0 and 1 to encode our categorical features because categorical features that are in string format cannot be understood by the machine and needs to be converted to numerical format.

● Exploratory Data Analysis

After loading the dataset we performed this method by comparing our target variable that is “default.payment.next.month” with other independent variables. This process helped us figuring out various aspects and relationships among the target and the independent variables. It gave us a better idea of which feature behaves in which manner compared to the target variable.

● Feature Selection

In these steps we used algorithms like ExtraTree classifier to check the results of each feature i.e which feature is more important compared to our model and which is of less importance. Next we used ANOVA to select the best feature which we will be using further in our model.

● Treating class imbalance (SMOTE)

To compensate for the rare classes in the imbalance dataset, we use SMOTE(Synthetic Minority Over-Sampling Technique) method to over sample the minority class and ensure the sampling is not biased. What this technique does under the hood is simply duplicating examples from the minority class in the training dataset prior to fitting a mode. After SMOTE sampling, the dataset has almost equal size of 0s and 1s.

● Fitting different models

For modelling we tried various classification algorithms like:

Logistic Regression
Decision Tree Classifier
Random Forest Classifier
KNN Classifier
## 3. Conclusions
● As the company can not afford the False Negative so main metric to comapre all algorithm is Recall metric.

● Logistic Regression had an imbalance in the recall score of about 82% for class 0 and 56% for class 1.

● Performance on Decision Tree is comparatively better. Decision Trees have recall scores of 78%(class 0) , 48%(class 1).

● Imbalanced data was balanced using SMOTE sampling technique.

● Data categorical variables had minority classes which were added to their closest majority class

● There were not huge gap but female clients tended to default the most.

● Random forest have the highest test accuracy with 77%.
