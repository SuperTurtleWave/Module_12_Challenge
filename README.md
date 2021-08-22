# **Module_12_Challenge_Report**

---

## Overview of the Analysis

The purpose of this analysis is to compare two logistic regression models using two different versions of a dataset to see how imbalanced data plays a part in our models. Credit risk is usually known for classfication issues as the data is normally imbalanced. The financial information stored in our csv file is a collection of different loans with our loan status column being our dependent varaible for our predictions. In the loan status column, a '0' represents a healthy loan and a '1' represents a high-risk loan. 

We start my importing the necessary libraries and packages. We move onto reading the csv file into a dataframe so that we can seperate our data into labels (independent variables) and features (dependent varaibles). Once we isolate our loan status time series, using the value_counts function, we can take a sneak peek at the balance of our target values and observe any imbalances if any. We now split the data into training and testing data sets using a random_state parameter of 1 to ensure consistency when running model. Fit the model by passing in the training data, then pass in X_test into the fitted model to predict our features. 

To compare, we will create a different version of the dataset using the RandomOverSampler function and storing them into new variables. Using the resampled data, we can fit our new model and use that to predict our new labels. 

For the final part of comparisson, we will calculate the accuracy score, confusion matrix, and a classification report to evaluate both models. 


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Accuracy - This model has a 95% percent accuracy score
  * Precision - The model has 100% precision in predicting healthy loans when looking at healthy loans and 85% in correctly predicting high-risk loans when predicting high-risk loans.
  * Recall - The model will 99% of the time detect healthy loans and 91% of the time detect high-risk loans. 



* Machine Learning Model 2:
  * Accuracy - This model has a 99% percent accuracy score. 
  * Precision - This model has 100% precision when predicting healthy loans and 84% when predicting high-risk loans. 
  * Recall - The model will 100% of the time detect healthy & high-risk loans. 

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
The machine learning model 2 seems to perform much better at the sacrfice of 1% in precision when predicting high-risk loans, but we are gaining a 9% increase in the recall percentage. 

* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
Performance does depend on the problem we are trying to solve as it becomes a context situation. We would need to figure out our question and what we are trying to find. In a case where we want to precisely predict high-risk loans, we would want the first machine learning model. 

If you do not recommend any of the models, please justify your reasoning.
I would recommend model 2 as it does better overall. 