# Credit Card Fraud Detection
[elevator pitch] --> the problem you are solving, the data you are using to solve it, and how well your model soves the problem (just a couple sentances)

Credit card fraud impacts consumers, merchants and issuers alike. Its economic cost goes far beyond the cost of illegaly purchased
merchandise. 

![Hacker stealing data](Images/fraudster.jpg)

## Business Understanding and Data Understanding
- Explain the project context, using at least one citation to demonstrate your domain understanding
  
- This is a binary classification project with highly imbalanced dataset. We are looking for an AI driven strategy that will effectively identify patterns in fraud transactions
- Consider including visualizations as well
![image](https://github.com/ShaneR31/Final-Flatiron-Capstone/assets/124909566/302682b5-ea2c-4fac-b022-25f9642bb89f)



## Modeling and Evaluation
- what kind of model(s) did you use?
  
- We applied a class weight or binary crossentropy function (loss function) to our Artificial Neural Networkv (ANNs), Boosting ensemble (XGBoost) and Trees Ensemble(Random Forest & Decision Trees) models.
- Even though we applied a weighted accuracy metric to our models, we chose to ignore its score to focus on metrics such as Recall & Precision, F1-score, Weighted Average and the Confusion Matrix to select our best model performer
  
- How well did your final model perform, compared to the baseline?
  
  In the test results of our best performer, we saw a recall & precision scores of 0.82 and 0.95 respectively. We are catching over 95% of fraud transactions.
  Plus, this model correctly identified 111 transactions as fraudulent; Missed 6 fraudulent transactions; At the cost of incorrectly flagging 25 legitimate transactions

## Conclusion
- How would you recommend that your model be used?
  
  We would recommend the XGBoost Classifier to be evaluated on its (Recall plus Precision) and its Confusion matrix test results, focusing on the fraudulent or minority class only. This model is effective on imbalance dataset. Our advice would be to apply a  class weights function: by making classes with higher data quantities less important in the model optimization process, it is possible to achieve optimization-level class balance without overfitting the data. 

## Repository Navigation
- An explanation of the repository organization
  
- Our repositoty has 5 branches, 4 branches allocated to the team members, a main branch that includes a final notebook, a final presentation, a Read Me file as well as a .gitignore file
  
- Links to the final notebook and presentation
- Reproduction instructions (or a link to them)
