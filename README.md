# Predicting Probabilities of XYZ and Seasonal Vaccination Uptake

This project focuses on predicting the probabilities of individuals receiving xyz and seasonal influenza vaccinations using machine learning techniques.
## Model Used
BaggingClassifier with XGBoostClassifier as the base estimator
## Key Points

* Tackled the feature columns' missing values using Iterative Imputer and Simple Imputer.
* Applied One-Hot Encoding to convert categorical features into numerical features.
* Applied Standard Scaler to normalize the values.
* Addressed the target variables' class imbalance using scale_pos_weight.
* Instantiated two separate models using BaggingClassifier with XGBClassifier as the base estimator for each target variable.
* Implemented hyperparameter tuning using RandomizedSearchCV.
* The best hyperparameters are directly used in the [code](https://github.com/Dream-Falls/Tushar-Punjabi_Datahack/blob/main/Source_Code.ipynb).
* Utilized ROC AUC for evaluation within each model. Additionally, calculated an overall ROC AUC by combining both models' predictions,  providing a comprehensive assessment of performance.
* Trained the models on the complete training data and made predictions on 'test_set_features'.
## Results
The mean ROC AUC scores for each target variable and the overall score are summarized below:
   * XYZ vaccine: Mean ROC AUC score = 0.8415
   * Seasonal vaccine: Mean ROC AUC score = 0.8588
   * Overall ROC AUC score = 0.8502

The predicted probabilities for the two target variables of the 'test_set_features' dataset are stored [here](https://github.com/Dream-Falls/DataHack/blob/main/Submission_.csv).
