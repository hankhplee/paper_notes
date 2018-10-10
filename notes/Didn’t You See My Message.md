# Didn’t You See My Message? Predicting Attentiveness to Mobile Instant Messages
Predict attentiveness using simple phone sensor. Seven easily computed features can predict attentiveness with an accuracy of 70%.

### Data Set
1. 24 participants, 6423 msg notifications

## Model
### Features
1. the notification is considered "attented" if
    1. the notification drawer is opened
    2. a app was opened, and all its unread msg were attended
2. the median delay between receiving and attending to a message is 6.15 minutes. As a threshold for
    1. "High" attentiveness
    2. "Low" attentiveness 

3. 
![](https://i.imgur.com/FLoY7CB.png)

## Classifier
1. nauve Bayes
2. logistic regression
3. SVM
4. random decision tree
5. **random forest (10 decision trees)** with accuracy of 68.7%

## Asymmetric Error Penalization
higher penalty cost (1.5 times) when the low class is misclassified as high than when the high class is misclassified as low. 

## Feature ranking and selection
Starting from the strongest feature (Time since lat screen on), and adding other features into the model. Remained if the accuracy and precision improve, otherwise discarded.
![](https://i.imgur.com/i95lJIE.png)
