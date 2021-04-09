# Credit Risk Analysis
Finished Deliverables:  
[Credit Risk Resampling](/credit_risk_resampling.ipynb)    
[Credit Risk Ensemble](/credit_risk_ensemble.ipynb)   
## Overview
Given a credit card dataset, use different techniques and algorithms to predict credit risk.  Then, evaluate the performance of each machine learning model.
## Results
Ensemble learners tended to give better all-around scores especially the Easy Ensemble AdaBoost Classifier.  

### Balanced Accuracy Scores

* The naive random oversampling method yielded a balanced accuracy score of 66%  
     - SMOTE oversampling and and undersampling were worse than this
     - Combination using SMOTEEN perfermed slighly better yielding a score of 68%  
* The balanced random forest classifer ensemble learner performed much better returning a balanced acuracy score of 79%  

  
### Precision and Recall Scores
* All oversampling and undersampling methods return a very low precision score  
* SMOTE oversampling and undersampling had recall scores below 70%, but combination sampling pushed it above 75%  
* The balanced random forest classifer ensemble learner returned a low precision score (3%)
     - The recall score is 70% for high-risk applicants 
  
![Resampling Class Report](/Images/resampling_class_report.png "Resampling Class Report")  
  
* The Easy Ensemble AdaBoost Classifier performed very well overall with a balanced accuracy score of 93% and a recall of 92%
     - Its precision is still low at 9%, but far higher than the next best for the other 5 models (3%)  
  
![Ensemble Class Report](/Images/ensemble_screenshot.png "Ensemble Class Report")  
    
## Summary
Sensitivity is most likely more important when analyzing credit risk because one would rather detect all of the bad credit risks even if it means a higher number of false positives.  It is important not to lend money to high-risk customers so the lender would rather deny some low-risk people if it means not losing a lot of money.  Therefore, since the Easy Ensemble provides a high accuracy and recall (sensitivity) score, and gives the highest precision score, it is a good candidate for this lender.  Generally, it is best to have a good balance between precision and recall so it is still advisable for the lender to proceed with caution.  Regardless, given this situation's extra importance on sensitivity, it makes sense for the lender to proceed with this method and continue to train the model to see if it improves.
