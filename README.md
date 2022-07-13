# Credit_Risk_Analysis

## Analysis Overview
In this project we are going to use different Machine Learning models to train and predict credit card risk. As credit risk is an unbalanced classifictaion problem, we will use models for unbalanced classes.

## Resources
Sci-kit learn library, Imbalanced_learn library, Pandas, Jupyter notebook, [LoanStats_2019Q1.csv.zip](/LoanStats_2019Q1.csv.zip)

## Results

### BalancedRandomForestClassifier
This model fits  a number of decision trees classifiers on various sub-samples of the dataser and used averages to improve the predictve accuracy and control overfitting, however in cases like this one that are unbalanced problesm, we need to over-sample from the small class to balance the classes.


![Screen Shot 2022-07-12 at 11 04 21 PM](https://user-images.githubusercontent.com/43548929/178648298-dc1f8ceb-6845-4e52-b1ab-9426ea03b681.png)

### Easy Ensemble AdaBoost Classifier
![Screen Shot 2022-07-12 at 11 10 26 PM](https://user-images.githubusercontent.com/43548929/178648944-7f1ac081-8c39-497c-ad2e-a3d601966620.png)

### Oversampling
![Screen Shot 2022-07-12 at 11 16 34 PM](https://user-images.githubusercontent.com/43548929/178649528-c8f99f89-ead8-4acb-8aa3-814642ccc569.png)

### SMOTE Oversampling
![Screen Shot 2022-07-12 at 11 17 08 PM](https://user-images.githubusercontent.com/43548929/178649593-5f364592-d797-47c1-9f89-5aa42bdc2702.png)

### Undersampling
![Screen Shot 2022-07-12 at 11 17 47 PM](https://user-images.githubusercontent.com/43548929/178649659-90416257-f293-4fc9-be4d-9c01ff838343.png)

### Combination (Over and Under) Sampling
![Screen Shot 2022-07-12 at 11 18 20 PM](https://user-images.githubusercontent.com/43548929/178649708-0250d9b9-a601-4531-afba-67494a9fb7da.png)

