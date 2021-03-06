# UCB-Supervised-ML-Project
## Project Overview
In this project, I used Python to create and evaluate several machine learning models to predict credit risk. Here are the steps I followed
- oversample the data using the RandomOverSampler and SMOTE algorithms.
- Undersample the data using the ClusterCentroids algorithm.
- Use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm.
- Compare two machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier.

In thr report below, I evaluated the performance of these models and make a recommendation on whether they should be used to predict credit risk.

## Results - Balanced Accuracy Scores, Confusion Matrixes and Imbalanced Classification Reports

### RandomOverSampler model: 
The balanced accuracy score is ~ 65%.
The high_risk precision is about 1% only with 67% sensitivity making a F1 of 2% only.

<img width="322" alt="1" src="https://user-images.githubusercontent.com/69255270/125217337-38631280-e275-11eb-8e23-3d2f0b730c82.png">
<img width="484" alt="2" src="https://user-images.githubusercontent.com/69255270/125217340-3b5e0300-e275-11eb-8d7f-b987553670e5.png">


### SMOTE model
The results are similar to the previous model.
The balanced accuracy score is 64%.
The high_risk precision is about 1% only with 61% sensitivity which makes a F1 of 2% only.

<img width="275" alt="3" src="https://user-images.githubusercontent.com/69255270/125217433-75c7a000-e275-11eb-94f0-7ce17209dcef.png">

<img width="478" alt="4" src="https://user-images.githubusercontent.com/69255270/125217438-7829fa00-e275-11eb-9777-b51cbba5cefb.png">

### ClusterCentroids model
Here the balanced accuracy score is down to about 54%.
The high_risk precision is still 1% only with 66% sensitivity which makes a F1 of 1%.

<img width="399" alt="5" src="https://user-images.githubusercontent.com/69255270/125217493-a7d90200-e275-11eb-98c8-9ae6d31d0958.png">
<img width="480" alt="6" src="https://user-images.githubusercontent.com/69255270/125217502-ac9db600-e275-11eb-8bf9-922d8cfa789c.png">

### SMOTEENN model

The balanced accuracy score is about 64%.
The high_risk precision is still 1% only with 70% sensitivity which makes a F1 of only 2%.

<img width="285" alt="7" src="https://user-images.githubusercontent.com/69255270/125217554-d48d1980-e275-11eb-8af1-94a11a2d9cf4.png">
<img width="539" alt="8" src="https://user-images.githubusercontent.com/69255270/125217560-d951cd80-e275-11eb-9522-811e8cb91e8a.png">


### BalancedRandomForestClassifier model


The balanced accuracy score improved to about 74%.
The high_risk precision is still low at 3% only with 56% sensitivity which makes a F1 of only 6%.


### <img width="383" alt="9" src="https://user-images.githubusercontent.com/69255270/125217673-13bb6a80-e276-11eb-84e7-3a3cc0d928d9.png">
<img width="493" alt="10" src="https://user-images.githubusercontent.com/69255270/125217681-1c13a580-e276-11eb-8a4e-79d3f856b32f.png">


### EasyEnsembleClassifier model

Now, the balanced accuracy score is high to about 89%.
The high_risk precision is still low at 8% only with 82% sensitivity which makes a F1 of only 14%.


<img width="333" alt="11" src="https://user-images.githubusercontent.com/69255270/125217699-259d0d80-e276-11eb-84c9-c9805a3bd71a.png">
<img width="479" alt="12" src="https://user-images.githubusercontent.com/69255270/125217706-2897fe00-e276-11eb-980f-cd7e962b2cfa.png">


Summary
All the models used to perform the credit risk analysis show weak precision in determining if a credit risk is high.
Sensitivity being an important parameter for credit risk analysis, the Ensemble models brought a lot more improvment specially on the sensitivity of the high risk credits.
The EasyEnsembleClassifier model shows a recall of 82% so it detects high risk credit very well. But that will falsely detect even low risks as high risk where bank will loose business. So there is a scope to improve the model. 
