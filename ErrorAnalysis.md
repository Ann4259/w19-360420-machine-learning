# Error Analysis
## Intro to Programming Section 1
## Zi Xiang Huang, An Qi Xu

## After 1000 runs, the mean accuracy is 98.168% and the standard variation is 2.14*10^(-24)

## Analysis of different error types

•	the amount of confidence we can put in our model
    Each time we want to split our training set and test set, our Dataset methods will shuffle through the whole dataset, meaning that give all data points a completely random order, then we take the number of data points we want, starting from the first one. Therefore, each time we run this program, we have a different training set and a test set. For a certain test point, the nearest neighbors method may give different answers according to different data available in the training set. This randomness of training & test dataset contributes to the variance in accuracy.
    After 1000 runs, the mean accuracy is 98.168% and the standard variation is 2.14*10^(-24). 
    In a complete random test set, the percentage frequency of label benign is 65.2% and the percentage frequency of label malignant is 34.8%. In this case, if we choose the label “benign” to predict all data points, the baseline performance should be 65.2%.


•	Type of errors
  False positive: when something is not happening, but being said that it’s happening (ex. You didn’t catch a fever, but your doctor said you’re having a fever)
  False negative: when something is happening, but being said that it’s not the case (ex. You caught a severe fever, but your doctor said that you were totally fine)
  Precision: when you say a set of data belongs to the same category, the part that is actually this category (number of your right prediction) divided by the total number of predictions is precision
  Recall: when you make predictions about a category of data, the part that you say it’s belong to this category(number of your right predictions) divided by the total number of predictions is recall
These two measurement differ in this case because the number of benign cancers and the number of malignant cancers are not exactly the same, or else the precision and recall would be the same value.
When precision is 100%, the baseline recall would be 65.2%; when recall is 100%, the baseline precision is 100%.
  By increasing the number of K in the code, the mean accuracy drops, so does the standard deviation. 


