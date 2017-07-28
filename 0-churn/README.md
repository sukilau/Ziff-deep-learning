# Customer Churn Prediction using Random Forest (AUC=0.904)

Customer churn prediction (positive or negative) using scikit-learn in Python 3.6.0. 


## What is in this repo

*churn-prediction.ipynb*  

* An implementation of RandomForestClassifier trained against 3333 observations with 17 features using 10-fold cross validation.

* Missing values are imputed by using median (numeric data) or mode (categorical data). Feature vectors are standardized before fitting into the model.

* Grid search is used to find the best parameter set of the RandomForestClassifier: {'max_depth': 10, 'n_estimators': 100}.

* Evaluation on area under ROC curve is made using 10-fold cross validation.  Best AUC score = 0.904 (+/-0.090) for the parameter set {'max_depth': 10, 'n_estimators': 100}.


*model-comparison.ipynb*  

* The dataset is also tested against other classifiers, i.e. KNeighborsClassifier, SVC, LinearSVC, SGDClassifier. Grid search is implemented to find the best parameter set of the classifiers on 10-fold CV.

* RandomForestClassifier achieves the best AUC score compared with the above classifiers.


*churn.csv*  
*churn-clean.csv*  

* Original and cleaned churn dataset of 3333 observations with 17 columns of selected features and the final clolumn of churn labels. 


## Model Evaluation
 
| Classifiers                |  AUC   |
| -------------------------- |-------:|
| RandomForestClassifier     |  90.4% |
| KNeighborsClassifier       |  87.7% |
| SVC                        |  89.2% |
| LinearSVC                  |  80.7% |
| SGDClassifier              |  77.1% |





