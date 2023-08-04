# Credit Card Fraud Detection
In this project we are tackling fraud within the payment card industry. This is based on a dataset containing credic card transactions made by cardholders in Europe in September 2013, available [here](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud). Our model is able to detect over X% of fraudulent transactions while flagging minimal valid transactions.

![Hacker stealing data](Images/fraudster.jpg)

## Business Understanding and Data Understanding
- Explain the project context, using at least one citation to demonstrate your domain understanding
- Consider including visualizations as well

It comes as no surprise that relative to valid transactions, fraudulent transactions are fairly rare. In fact, out of 284,315 transactions contained in our dataset, only 492 are fraudulent (just over 0.17%). Additionally, due to the sensitive nature of payment card transactions, the features contained within our dataset have been obfuscated with PCA to hide sensitive information behind new vague features while preserving most of the information from the dataset.

![Add visualization for class imbalance here]()

These factors create an interesting challenge. For more information about handling imbalanced datasets and the appropriate metrics to use for classification models we consulted a paper from University of Iaşi available [here](339986048_Methods_of_Handling_Unbalanced_Datasets_in_Credit_Card_Fraud_Detection).

## Modeling and Evaluation
- what kind of model(s) did you use?
- How well did your final model perform, compared to the baseline?

We began our modeling by loading in the dataset and doing some basic data exploration. From this we were able to identify the significant class imbalance within the data and note the distribution of various features. With our new understanding of the data set we were able to create a baseline model with a logistic regression. When examining the metrics generated when evaluating the model aggainst the test set and confusion matrix, it became immediately clear that accuracy would not be a useful measure of model performance due to the class imbalance. Therefore, we shifted our focus to interpretting model performance against more useful measures like precision, recall, and AUC ROC.

After establishing our baseline model performance we tested several potential ways to rebalance our dataset, these included undersampling, oversampling with SMOTE, and a combination of both. With our corrections to the class balances we moved on to more advanced models, these included...

We decided on random forrest as our final model. With our random forrest model, we were able to achieve... This was an improvement of around X% over our baseline...

## Conclusion
- How would you recommend that your model be used?

We would recommend that our model be integrated into a system where it can be used to flag and reject potentially fraudulent transactions in real time. Would help protect the financial interests of both the payment processor and the consumer. Even if some valid transacations may occasionally be flagged as fruad, we believe this would be far outweighed by the additional layer of protection against fraudulent transactions.

## Repository Navigation
- An explanation of the repsitory organization
- Links to the final notebook and presentation
- Reproduction instructions (or a link to them)