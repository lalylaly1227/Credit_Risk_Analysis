# Credit_Risk_Analysis
## Overview

In this challenge we were given a file, LoanStats_2019Q1, which we used to determine credit risks. To complete this analysis, we use different Machine Learning techniques to train and evaluate the data with unbalanced classification which presented a problem due to the number of good loans outweighing the amount of risky loans.

Various libraries and algorithms were used to build and evaluate models using resampling including:

* imbalanced-learn
* scikit-learn
* RandomOverSampler
* SMOTE (Synthetic Minority Oversampling Technique) algorithms
* ClusterCentroids algorithm
* SMOTEENN algorithm
* BalancedRandomForestClassifier (Bias Reduction Model)
* EasyEnsembleClassifier (Bias Reduction Model)

## Deliverable 1: Use Resampling Models to Predict Credit Risk

First, we split the data into training and testing data.  Then we took the steps with Naive Random Oversampling, SMOTE Oversampling, and Undersampling to see which method produced the highest accuracy.

### Results
The original dataset contained 115,675 loan applications in Q1 of 2019. We then used the "loan status" to determine whether the application was considered "low" or "high" risk. Applications that had "current" as the "loan status" were classified as "low risk" and the remaining as "high risk". This reduced the dataset to a total of 68,817 applications with 68470 classified as "low risk" and only 347 classified as “high risk”. Then we split the data into test and train 75/25.

<img width="295" alt="Screen Shot 2022-09-25 at 5 34 27 PM" src="https://user-images.githubusercontent.com/105124485/192166693-9e75c179-d2bf-4195-a089-41552a2e571d.png">

Naive Random Oversampling produced equal amounts of low and high risk data with a balance accuracy score of 63% (0.6314677834584286).

<img width="435" alt="Screen Shot 2022-09-25 at 5 34 46 PM" src="https://user-images.githubusercontent.com/105124485/192166760-6b41286d-869d-4ea7-af73-b47ceda86957.png">

<img width="490" alt="Screen Shot 2022-09-25 at 5 34 56 PM" src="https://user-images.githubusercontent.com/105124485/192166768-11642ecd-e41b-4d71-8498-90240d322f14.png">

<img width="365" alt="Screen Shot 2022-09-25 at 5 35 07 PM" src="https://user-images.githubusercontent.com/105124485/192166771-00923dc7-53ce-479a-8473-225859e1faad.png">

<img width="720" alt="Screen Shot 2022-09-25 at 5 35 15 PM" src="https://user-images.githubusercontent.com/105124485/192166777-0b01e16e-559f-400f-a7d0-056fa7b6dde7.png">

Next, I used SMOTE Oversampling which produced a balance accuracy score of 63% (0.6268316069795457).

<img width="391" alt="Screen Shot 2022-09-25 at 5 42 07 PM" src="https://user-images.githubusercontent.com/105124485/192166838-fdfbea06-2062-417c-afe6-5fedf4ecb1e3.png">

<img width="365" alt="Screen Shot 2022-09-25 at 5 42 38 PM" src="https://user-images.githubusercontent.com/105124485/192166857-08cc9c0b-9250-495b-9547-82c1bab0bbb1.png">

<img width="710" alt="Screen Shot 2022-09-25 at 5 42 59 PM" src="https://user-images.githubusercontent.com/105124485/192166866-52a850ff-6e5f-44a4-9ee6-3a9fe3167764.png">

Lastly, I used Undersampling which produced a balance accuracy score of 51% (0.5106522273388368).

<img width="370" alt="Screen Shot 2022-09-25 at 5 43 46 PM" src="https://user-images.githubusercontent.com/105124485/192166886-51b51bb5-0211-41ac-a369-5d2fc8247650.png">

<img width="357" alt="Screen Shot 2022-09-25 at 5 44 04 PM" src="https://user-images.githubusercontent.com/105124485/192166903-03e44d95-d4d2-4fdc-ae89-a5b12e712363.png">

<img width="707" alt="Screen Shot 2022-09-25 at 5 44 18 PM" src="https://user-images.githubusercontent.com/105124485/192166907-2b81e4ec-71eb-4a84-bad0-2fae945e7a79.png">

## Deliverable 2: Use the SMOTEENN algorithm to Predict Credit Risk

### Results
SMOTE and Edited Nearest Neighbors was used in this deliverable to see if it could predict credit risk.

I used a Combination (Over and Under) Sampling which produced a balance accuracy score of 62% (0.6235551607301852).

<img width="365" alt="Screen Shot 2022-09-25 at 5 45 18 PM" src="https://user-images.githubusercontent.com/105124485/192166943-38850261-cf3d-4c25-be84-8dd8a3a88cad.png">

<img width="362" alt="Screen Shot 2022-09-25 at 5 45 32 PM" src="https://user-images.githubusercontent.com/105124485/192166953-eda2db6d-b0eb-47e5-8eb7-d216db12469f.png">

<img width="713" alt="Screen Shot 2022-09-25 at 5 45 49 PM" src="https://user-images.githubusercontent.com/105124485/192166966-74f79a97-46ee-4ed9-acb5-b6e0724b6a01.png">

## Deliverable 3: Use Ensemble Classifiers to Predict Credit Risk

### Results
I compare two ensemble algorithms to determine which algorithm results in the best performance. I will train a Balanced Random Forest Classifier and an Easy Ensemble AdaBoost classifier.

Balanced Random Forest Classifier produced a balance accuracy score of 79% (0.7885466545953005).

<img width="455" alt="Screen Shot 2022-09-25 at 5 46 56 PM" src="https://user-images.githubusercontent.com/105124485/192167010-4962f69b-ad34-4da8-aec1-7e624f2defc2.png">

<img width="703" alt="Screen Shot 2022-09-25 at 5 47 20 PM" src="https://user-images.githubusercontent.com/105124485/192167028-ccdde1a9-0f69-46c3-827d-628701061bb6.png">

Finally, I used Easy Ensemble AdaBoost Classifier which produced a balance accuracy score of 93% (0.9316600714093861).

<img width="368" alt="Screen Shot 2022-09-25 at 5 47 45 PM" src="https://user-images.githubusercontent.com/105124485/192167040-4e1b6575-574c-41f4-ba5c-d1a5217ab766.png">

<img width="700" alt="Screen Shot 2022-09-25 at 5 48 06 PM" src="https://user-images.githubusercontent.com/105124485/192167052-c21d4571-7c13-4438-a88b-f4230a7a77bd.png">

## Summary
In conclusion, credit-risk is a challenging thing to predict, even for advanced Machine Learning algorithms with almost 100 columns of data to process. While the Easy Ensemble AdaBoost Classifier model produced the highest overall accuracy, this was largely due to the dataset being so thoroughly unbalanced. Even when it’s balanced accuracy and average F-score were above 90%, it's F-score for high-risk prediction was only 0.16. In the end, I would advise against using any of these algorithms, since it would put creditors at risk of being unable to accurately predict who the high-risk clients or debtors are.

![ml-techniques](https://user-images.githubusercontent.com/105124485/192167160-0de57d8d-96ec-4e5d-a49a-39c11938d00c.jpg)

