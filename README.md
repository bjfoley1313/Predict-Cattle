# Predict-Cattle

This binary classification project's goal was to predict whether the settlement in Live Cattle futures price would be higher or lower than the previous days.  The data was called using the Python API in Quandl.  

The feature's used to predict cattle settlement were previous day open interes, previous day volume, previous day lean hogs settle and previous day corn settle.  

For the training data, 9 years (April, 2007 - March, 2016) of continous front month data was used.  The test set (April, 2016 - March, 2017) is the years worth of data directly following the training period.  Since this data is a continuous time series there was no cross validation used.  

All numerical data was standardized and Nan values were removed.  The target class values were similar in count so there was no need to balance.  

Five ML classification models were fit to the training data: Naive Bayes, Logistic Regression, KNN, SVM and Random Forest.  In addition, a Grid Search was used to tune the hyperparameters of all models except the Naive Bayes.  

The Logistic Regression and Linear SVM models ended up generalizing the data the best.  The SVM model was run with a high C and gamma so there is risk of overfitting the training set that possibly needs to be examined further. 
