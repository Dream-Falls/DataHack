# Predicting Probabilities of XYZ and Seasonal Vaccination Uptake

This project focuses on predicting the probabilities of individuals receiving xyz and seasonal influenza vaccinations using machine learning techniques.
BaggingClassifier with XGBoostClassifier as the base estimator
## Key Points
* Tackled the feature columns' missing values.
* Addressed the taget variables' class imbalance. 
* Two separate models are instantiated using BaggingClassifier with XGBoostClassifier as the base estimator for each target variable.
* Implemented hyperparameter tuning using Stratified RandomSearchCV.
* The best hyperparameters are directly used in the [code](https://github.com/Dream-Falls/AnalyticaX/blob/main/source_code.ipynb).
* Utilizes ROC AUC for evaluation within each model. Additionally, we calculated an overall ROC AUC by combining both models' predictions, providing a comprehensive assessment of performance.
## Results
The mean ROC AUC scores for each target variable and the overall score are summarized below:
   * XYZ vaccine: Mean ROC AUC score = 0.8415
   * Seasonal vaccine: Mean ROC AUC score = 0.8588
   * Overall ROC AUC score = 0.8502

The predicted probabilities for the two target variables of the 'test_set_features' dataset are stored [here](https://github.com/Dream-Falls/DataHack/blob/main/Submission_.csv).
