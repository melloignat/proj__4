## **Project description:**

A prototype of a machine learning model for company X. The company develops solutions for the efficient operation of industrial enterprises. The model must predict the gold recovery rate from gold-bearing ore. You have data on mining and refining parameters. The model will help optimize production allowing not to launch unprofitable business.

## **Project timeline:**

* Initial data analysis performed to check features and data consistency. Some missing features in the test dataset found.
* Checked that the enrichment efficiency is calculated correctly in the original data. Calculated it on the training set for the "rougher.output.recovery" feature. Found the MAE between our calculations and the feature value.
* For the features not available in the test dataset correlation was checked to see if we can create a good model without them.
* Data was analysed and preprocessed. Checked how the concentration of metals (Au, Ag, Pb) changes at different stages: in the feedstock, in the rough concentrate, in the concentrate after the first cleaning, and in the final concentrate.
* Compared the distributions of the grain sizes of the feedstock on the training and test sets. If the distributions differ greatly from each other, the model estimate will be incorrect.
* Studied the total concentration of metals at different stages: in the feedstock, in the rough concentrate, in the concentrate after the first cleaning, and in the final concentrate.
* Custome sMAPE metric was initialised to check models prediction quality and select the best one.
* 2 models (RandomForest and DecisionTree) were created and trained.
* Both models was checked on test data, compared with constant model and sMAPE was used to select the most suitable one.

## **Project result:**

As the result, based on custom metric that we created we selected "RandomForest" model for prediction. Also we compared it with constant model to check that the quality of the selected model is better than the dummy one. Resulting model will allow the customer to fulfill his goal.

