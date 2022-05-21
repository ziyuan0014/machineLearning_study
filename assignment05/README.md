# assignment05

### dataset：Breast Cancer Wisconsin (Original) Data Set
http://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Original%29

### assignment：

1.	Create a boxplot or violin plot for each variable to visualize the distribution of the values between malignant and benign samples. Which of the four variables will be most accurate in predicting by itself? Explain why.
2.	Randomly remove 20% of our data and save it as test_set and the other 80% as training_set. Keep the proportion of Benign and Malignant the same in your test_set and training_set datasets.
3.  Using the training_set, create a logistic regression model using the glm() function described in our lecture to create a model for each variable separately. Calculate AUC using the test_set to determine which of the four variables is the most helpful predictor.
4.  Repeat step 3 but this time with all the variables together and calculate the AUC to compare the results. 
5.  Perform a decision tree classification using two different values for max_depth parameter. Draw the tree for both and compare AUC for both.

### package：

- numpy
- pandas
- sklearn
- matplotlib
