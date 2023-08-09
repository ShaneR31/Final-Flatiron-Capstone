# Credit Card Fraud Detection
[elevator pitch] --> the problem you are solving, the data you are using to solve it, and how well your model soves the problem (just a couple sentances)

Credit card fraud impacts consumers, merchants and issuers alike. Its economic cost goes far beyond the cost of illegaly purchased
merchandise. 

![Hacker stealing data](Images/fraudster.jpg)

## Business Understanding and Data Understanding
- Explain the project context, using at least one citation to demonstrate your domain understanding
- This is a binary classification project with highly imbalanced dataset. We are looking for an AI driven strategy that will effectively identify patterns in fraud transactions
- Consider including visualizations as well
![image](https://github.com/ShaneR31/Final-Flatiron-Capstone/assets/124909566/d2d9e85c-edd7-4990-9b8d-820440489425)


## Modeling and Evaluation
- what kind of model(s) did you use?
- We used Artificial Neural Networkv (ANNs), Boosting ensemble (XGBoost) and Trees Ensemble(Random Forest & Decision Trees)
- We ignored the Accuracy Score due to the imbalance in the data, instead we focused on metrics such as Recall & Precision, Confusion Matrix
  to select our best model performer
  
- How well did your final model perform, compared to the baseline?
  In the test results of our best performer, we saw a recall & precision scores of 0.82 and 0.95 respectively. We are catching over 95% of fraud transactions.
  Plus, this model correctly identified 111 transactions as fraudulent; Missed 6 fraudulent transactions; At the cost of incorrectly flagging 25 legitimate transactions

## Conclusion
- How would you recommend that your model be used?
  We would recommend the XGBoost Classifier to be used with the Recall & Precision plus the Confusion matrix metrics, while ignoring the Accuracy score.
  This model is efficient on imbalance dataset but we are advising a change in the Loss function / Binary Crossencropy or Class Weight function to with its optimization.

## Repository Navigation
- An explanation of the repository organization
- Our repositoty has 6 branches, 4 branches allocated to the team members, a main branch that includes a final notebook, a final presentation, a Read Me file as well as a .gitignore file 
- Links to the final notebook and presentation
- Reproduction instructions (or a link to them)
