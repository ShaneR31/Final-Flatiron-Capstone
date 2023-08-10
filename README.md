# Credit Card Fraud Detection
Credit card fraud impacts consumers, merchants and issuers alike. Its economic cost goes far beyond the cost of illegaly purchased
merchandise. We are here to tackle fraud within the financial industry by focusing on only supervised learning processes.

![Hacker stealing data](Images/fraudster.jpg)

## Business Understanding and Data Understanding
- This is a binary classification project with highly imbalanced dataset. We are looking for an AI driven strategy that will effectively identify patterns in fraud transactions
-  [here](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud).

These factors create an interesting challenge. For more information about handling imbalanced datasets and the appropriate metrics to use for classification models we consulted a paper from University of Iaşi available [here](339986048_Methods_of_Handling_Unbalanced_Datasets_in_Credit_Card_Fraud_Detection).

## Modeling and Evaluation
  
  In the test results of our best performer, we saw a recall & precision scores of 0.82 and 0.95 respectively. We are catching over 95% of the fraud transactions.
  Plus, this model correctly identified 111 transactions as fraudulent; Missed 6 fraudulent transactions; At the cost of incorrectly flagging 25 legitimate transactions

We began our modeling by loading in the dataset and doing some basic data exploration. From this we were able to identify the significant class imbalance within the data, note the distribution of various features, and see which features are significant when relating to fraud. With our new understanding of the data set we were able to create a baseline model with a logistic regression. When examining the metrics generated when evaluating the model against the test set and confusion matrix, it became immediately clear that accuracy would not be a useful measure of model performance due to the class imbalance. Therefore, we shifted our focus to interpretting model performance against more useful measures like precision, recall, and AUC ROC.

After establishing our baseline model performance we tested several potential ways to rebalance our dataset, these included undersampling, oversampling with SMOTE, and a combination of both. With our corrections to the class balances we moved on to more advanced models, these included...


We applied a class weight or binary crossentropy function (loss function) to our Artificial Neural Networkv (ANNs), Boosting ensemble (XGBoost) and Trees Ensemble(Random Forest & Decision Trees) models.
  Even though we applied a weighted accuracy metric to our models, we chose to ignore its score to focus on metrics such as Recall & Precision, F1-score, Weighted Average and the Confusion Matrix to select our best model performer.

## Conclusion
  We would recommend the XGBoost Classifier to be evaluated on its (Recall plus Precision) and its Confusion matrix test results, focusing on the fraudulent or minority class only. This model is effective on imbalance dataset. Our advice would be to apply a  class weights function: by making classes with higher data quantities less important in the model optimization process, it is possible to achieve optimization-level class balance without overfitting the data. 

## Repository Navigation
  Our repositoty has 5 branches, 4 branches allocated to the team members for their individual contributions, a main branch that includes a final notebook, a final presentation, a Read Me file as well as a .gitignore file
  
[Final Notebook](339986048_Methods_of_Handling_Unbalanced_Datasets_in_Credit_Card_Fraud_Detection)
[Presentation](339986048_Methods_of_Handling_Unbalanced_Datasets_in_Credit_Card_Fraud_Detection)

Reproduction instructions:
Clone repository, Download required data from [here](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) and store CSV in repo Data folder. Run notebooks normally, some required packages may need to be installed.
