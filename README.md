## Module 17 Challenge: Credit Risk Resampling

The purpose of this challenge is to train and evaluate different machine learning models to solve an unbalanced classification problem which is inherent to the credit risk analysis due to a small fraction of bad loans in comparison to the number of good loans.
--
4 different techniques are evaluated here:
* Oversampling with RandomOverSampler
* Oversampling with SMOTE algorithms
* Undersampling using the cluster centroids algorithm
* Combination approach with the SMOTEENN algorithm

*1. Oversampling with RandomOverSampler*
* The precision score is the measure of how reliable a classification is.  The precision for the bad loan (high risk = 0) here is 0.01, which indicates that a large number of false high risk status were predicted.
* The recall score is the ability of the classifier to find all the positive samples.  Here it is 0.62 for high risk and 0.61 for low risk.
* The balance accuracy score measures how often the classifier is correct with the model.  Here it is 0.62.
* Due to extremely low precision score, oversampling with RandomOverSampler performs poorly on predicting the loan status.

*2. SMOTE Oversampling*
* The precision scores for both bad loans and good loans are 0.68.
* The recall scores also are higher at 0.68 and 0.69 for bad loans and good loans each.
* The accuracy score is also higher at 0.68.
* This model predicts the risk status better than oversampling with RandomOverSampler.

*3. Undersampling*
* The precision score for the bad loans are 0.69 while it is 0.65 for the good loans.
* The recall score is strong at 0.73 for the good loans while it is weak at 0.6 for the high risk applications.
* The accuracy score is 0.67, similar to the SMOTE Oversampling model.

*4. Combination Sampling*
* The precision score for both bad loans and good loans are 0.67.
* The recall score is strong at 0.74 for the bad loans while it is weak at 0.59 for the good loans.
* The accuracy score is 0.67, similar to both SMOTE Oversampling and Undersampling.

Based on this analysis, *the Combination Sampling* seems to perform best to predict the high risk loan status out of all 4 techniques as it has the best recall score to predict the high risk loan status while the precision score and accuracy scores are good enough to perform reasonably well.
