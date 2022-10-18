# Credit_Risk_Analysis
## Overview of the analysis:
Credit risk is very tough to predict. In this project we want to take a look at how all the factors in our loan_stats csv help predict whether someone is low or high risk status. In this project we are using imbalanced-learn and scikit-learn libraries to build models and evalute them using a resampling method. In the first couple of models I oversampled the data using randomoversampler and smote algorithms and undersample the data with the clustercentroid algorithm. In the remaining models I used a combination approach to over and undersample the data using smoteenn. Finally, I compared two machine learning models that minimize bias, balancedrandomforestclassifier and easyensembleclassifier.

## Results:
Naive Random Oversampling results: Our balanced accuracy test it 65%, the precision for the high_risk has a very low positivity at 1% and the recall is 72%

![Screen Shot 2022-04-22 at 4 31 59 PM](https://user-images.githubusercontent.com/96554223/164789700-0261f9ab-92b6-4ee1-9772-087cde47cd6c.png)


SMOTE oversampling results: the accuracy score is 66.2%, the precision for the high_risk loans has a low positvity again at 1% and recall is 69% overall
smote

![Screen Shot 2022-04-22 at 4 33 58 PM](https://user-images.githubusercontent.com/96554223/164789760-a5c34fb5-863f-4820-8c1b-5938c1c5beaa.png)

Undersampling results: balanced accuracy score is 66.2% overall, the precision is at 99% and the recall is 40%
undersampling

![Screen Shot 2022-04-22 at 4 34 44 PM](https://user-images.githubusercontent.com/96554223/164789851-d49fcd83-82f2-4d0c-a6a6-21d97d75d2c3.png)


Combination(over and undersampling) results: balanced accuracy score is 54.4% the precision is 99% and the recall is 57% overall
combination

![Screen Shot 2022-04-22 at 4 35 21 PM](https://user-images.githubusercontent.com/96554223/164789914-83001331-8562-4eca-a3d5-97b6badec06d.png)


Balanced Random Forest Classifier results: the accuracy score is 78.7% the precision is 99% and the recall is 88%
random forest

![Screen Shot 2022-04-22 at 4 37 41 PM](https://user-images.githubusercontent.com/96554223/164790182-234ea274-0bfc-4cef-8271-5b941aade2ae.png)


Easy Ensemble AdaBoost Classifier results: the accuracy score is 91.7% the precision is 99% and the recall is 94%
ensemble

![Screen Shot 2022-04-22 at 4 38 07 PM](https://user-images.githubusercontent.com/96554223/164790219-7bef6885-fb5e-4c19-bcbe-e9c40b58220e.png)


## Summary:
In the first four models we undersampled, oversampled and did a combination of both to try and determine which model is best at predicting which loans are the highest risk. The next two models we resampled the data using ensemble classifiers to try and predict which which loans are high or low risk. In our first four models our accuracy score is not as high as the ensemble classifiers and the recall in the oversampling/undersampling/mixed models is low as well. Typically in your models you want a good balance of recall and precision which is why I recommend the ensemble classifiers over the first four models. It appears that the Easy Ensemble had the best balance of all the models because of it's high accuracy score and good balance of precision and recall scores.
