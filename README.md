# Credit_Risk_Analysis

## Analysis Overview
In this project we are going to use different Machine Learning models to train and predict credit card risk. As credit risk is an unbalanced classifictaion problem, we will use models for unbalanced classes.

## Resources
Sci-kit learn library, Imbalanced_learn library, Pandas, Jupyter notebook, [LoanStats_2019Q1.csv.zip](/LoanStats_2019Q1.csv.zip)

## Results

### Oversampling
In random oversampling, instances of the minority class are randomly selected and added to the training set until the majority and minority classes are balanced.

The accuracy is of 67%.

The precision for low risk is 100% but only 1% for high risk.

The sensitivity for low risk is 61% and 73% for high risk.

![Screen Shot 2022-07-12 at 11 16 34 PM](https://user-images.githubusercontent.com/43548929/178649528-c8f99f89-ead8-4acb-8aa3-814642ccc569.png)

### SMOTE Oversampling
In this model the  size of the minority class has to increase too but the difference is that in SMOTE for an instance from the minority class, a number of its closest neighbors is chosen, based on the values of these neighbors, new values are created.

This model has an accuracy of 66%.

The precision for low risk is again 100% and again of 1% for high risk.

The sensitivity for low risk of  69% and of 62% for high risk.

![Screen Shot 2022-07-12 at 11 17 08 PM](https://user-images.githubusercontent.com/43548929/178649593-5f364592-d797-47c1-9f89-5aa42bdc2702.png)


### Undersampling
In this model to balance the classes the size of the majority class is decreased to the size of the minority class. It involves loss of data from the majority class. Cluster centroid undersampling creates clusters of the majority class, then generates synthetic data points, called centroids, that are representative of the clusters. 

This model has an accuracy of 52%, the lowest af all.

The precision is the same as the last 2, 100% for low risk and only 1% for high risk.

The sensitivity for low risk is 40% and for high risk 67%.

![Screen Shot 2022-07-12 at 11 17 47 PM](https://user-images.githubusercontent.com/43548929/178649659-90416257-f293-4fc9-be4d-9c01ff838343.png)

### Combination (Over and Under) Sampling
Here the minority class is oversampled; however, an undersampling step is added, removing some of each class's outliers from the dataset. The  two classes are more separated and can be identified easily.

This model has an accuracy of 65%.

A precision equalto the others of 1 for low risk and only 1% for highr risk.

The sensitivity for high risk is the highest for the resample models with 72% but for low risk only of 58%.

![Screen Shot 2022-07-12 at 11 18 20 PM](https://user-images.githubusercontent.com/43548929/178649708-0250d9b9-a601-4531-afba-67494a9fb7da.png)

### ENSEMBLE
### BalancedRandomForestClassifier
This model fits  a number of decision trees classifiers on various sub-samples of the dataset and use averages to improve the predictve accuracy and to control overfitting, however in cases like this one that is an unbalanced problem, we need to over-sample from the small class to balance the classes.

This model has an accuracy of  77%.

The precision for low risk is 100% again but only of 4% for high risk.

The sensitivity is of 91% for low risk and only 66% for high risk.

![Screen Shot 2022-07-12 at 11 04 21 PM](https://user-images.githubusercontent.com/43548929/178648298-dc1f8ceb-6845-4e52-b1ab-9426ea03b681.png)

### Easy Ensemble AdaBoost Classifier

This model combines multiple classifiers to increase the accuracy of classifiers. It works by set the weights of classifiers and training the data sample in each iteration to ensure the correct prediction of unusual observations.

The accuracy is of 91%.

The precision for low risk is 1 again and little higher for high risk but still very low, only 8% for high risk.

The sensitivity for low risk is 95% and for high risk of 87%,the highest until now.

![Screen Shot 2022-07-12 at 11 10 26 PM](https://user-images.githubusercontent.com/43548929/178648944-7f1ac081-8c39-497c-ad2e-a3d601966620.png)


## Summary

As we can see the resample models are not a good option for identifyng the credit risk, because they have a terrible precision with the True High risk and also the sensitivity is really low. The ensemble models made a better job, actually the only one that I would recommend to use is the Easy Ensemble AdaBoost Classifier because its accuracy is of 91% at properly classified the risk. It's precision for high risk was the highest one but it still letting go low risk cases classifying them as a high risk, but that is a better than the opposite. Also the sensitivity is really good for high risk, it means that he is avoiding most of the hight risk cases properly.
