# Credit Card Fraud Detection
In this project we are tackling fraud within the payment card industry. This is based on a dataset containing credic card transactions made by cardholders in Europe in September 2013, available [here](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud). Our model is able to detect over X% of fraudulent transactions while flagging minimal valid transactions.

Credit card fraud impacts consumers, merchants and issuers alike. Its economic cost goes far beyond the cost of illegaly purchased
merchandise. 

![Hacker stealing data](Images/fraudster.jpg)

## Business Understanding and Data Understanding
- Explain the project context, using at least one citation to demonstrate your domain understanding
  
  This is a binary classification project with highly imbalanced dataset. We are looking for an AI driven strategy that will effectively identify patterns in fraud transactions
- Consider including visualizations as well
![image](https://github.com/ShaneR31/Final-Flatiron-Capstone/assets/124909566/302682b5-ea2c-4fac-b022-25f9642bb89f)
![image](https://github.com/ShaneR31/Final-Flatiron-Capstone/assets/124909566/98653ee7-f737-4f62-88ad-b5007bff5ab1)
![image](https://github.com/ShaneR31/Final-Flatiron-Capstone/assets/124909566/a723e844-c1cf-4b8f-b259-9c1276fb19cb)
![image](https://github.com/ShaneR31/Final-Flatiron-Capstone/assets/124909566/c9d60b11-31a1-4433-8d4b-013d997b80ae)






It comes as no surprise that relative to valid transactions, fraudulent transactions are fairly rare. In fact, out of 284,315 transactions contained in our dataset, only 492 are fraudulent (just over 0.17%). Additionally, due to the sensitive nature of payment card transactions, the features contained within our dataset have been obfuscated with PCA to hide sensitive information behind new vague features while preserving most of the information from the dataset.

![Add visualization for class imbalance here]()

These factors create an interesting challenge. For more information about handling imbalanced datasets and the appropriate metrics to use for classification models we consulted a paper from University of Iaşi available [here](339986048_Methods_of_Handling_Unbalanced_Datasets_in_Credit_Card_Fraud_Detection).

## Modeling and Evaluation
- what kind of model(s) did you use?
  
  We applied a class weight or binary crossentropy function (loss function) to our Artificial Neural Networkv (ANNs), Boosting ensemble (XGBoost) and Trees Ensemble(Random Forest & Decision Trees) models.
  Even though we applied a weighted accuracy metric to our models, we chose to ignore its score to focus on metrics such as Recall & Precision, F1-score, Weighted Average and the Confusion Matrix to select our best model performer
  
- How well did your final model perform, compared to the baseline?
  
  In the test results of our best performer, we saw a recall & precision scores of 0.82 and 0.95 respectively. We are catching over 95% of fraud transactions.
  Plus, this model correctly identified 111 transactions as fraudulent; Missed 6 fraudulent transactions; At the cost of incorrectly flagging 25 legitimate transactions

We began our modeling by loading in the dataset and doing some basic data exploration. From this we were able to identify the significant class imbalance within the data, note the distribution of various features, and see which features are significant when relating to fraud. With our new understanding of the data set we were able to create a baseline model with a logistic regression. When examining the metrics generated when evaluating the model against the test set and confusion matrix, it became immediately clear that accuracy would not be a useful measure of model performance due to the class imbalance. Therefore, we shifted our focus to interpretting model performance against more useful measures like precision, recall, and AUC ROC.

After establishing our baseline model performance we tested several potential ways to rebalance our dataset, these included undersampling, oversampling with SMOTE, and a combination of both. With our corrections to the class balances we moved on to more advanced models, these included...

We decided on random forrest as our final model. With our random forrest model, we were able to achieve... This was an improvement of around X% over our baseline...

## Conclusion
- How would you recommend that your model be used?
  
  We would recommend the XGBoost Classifier to be evaluated on its (Recall plus Precision) and its Confusion matrix test results, focusing on the fraudulent or minority class only. This model is effective on imbalance dataset. Our advice would be to apply a  class weights function: by making classes with higher data quantities less important in the model optimization process, it is possible to achieve optimization-level class balance without overfitting the data. 

We would recommend that our model be integrated into a system where it can be used to flag and reject potentially fraudulent transactions in real time. Would help protect the financial interests of both the payment processor and the consumer. Even if some valid transacations may occasionally be flagged as fruad, we believe this would be far outweighed by the additional layer of protection against fraudulent transactions.

## Repository Navigation
- An explanation of the repository organization
  
  Our repositoty has 5 branches, 4 branches allocated to the team members for their individual contributions, a main branch that includes a final notebook, a final presentation, a Read Me file as well as a .gitignore file
  
- Links to the final notebook and presentation
- Reproduction instructions (or a link to them)
