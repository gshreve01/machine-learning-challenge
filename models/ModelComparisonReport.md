Model Comparison Analysis

I created three classifier models as well as a simple regression anda deep learning model.  The linear regression model performed the worst while the deep learning model performed the best The cleanup of the data was limited to Removing any rows with na values, and I considered removing some of the Other category type rows but decided that would corrupt some of the classification learning that would need to occur.  I included all columns within the dataset after initially testing the linear regression excludingthe ‘err’ columns, but discovered it performed better (only slightly) with the values included.

Linear Regression Model:
The prediction with the test data was 0.663 which was the worst of all models, and falls short of what I believe would be acceptable.  I used the StandardScalar for scaling the data since the MinMaxScaler performed worse.  The hyperparameter tuning did not perform any better than the defaults used.

Logistic Regression Model:
The prediction with the test data was 0.876 which while better than the Linear regression did not quite reach the 0.9 that I believe would be acceptable.  I used the MinMaxScaler for scaling the data to match what was dictated in the homework assignment.  The hyperparameter tuning did perform better than the defaults used.

SVC Model:
The prediction with the test data was 0.886 which was only slightly better than the Logistic regression and still fell short of the 0.9 to meet my minimum standards.  I used the MinMaxScaler for scaling the data.  The hyperparameter tunding did perfrom better than the defaults used.

Random Forest Classifier Model:
The prediction with the test data rounds to 0.907 which I will declare as acceptable (I am taking the values prior to hypertuning).  I used the MinMaxScaler for scaling the data.  The hyperparameter tuning did NOT perform better than the defaults used, and amazingly the defaults resulted in a perfect score using the training data.

Deep Learning Model:
The prediction with the test data rounds to 0.900 which again meets my minimum requirements.  I used the MinMaxScalar for scaling the data, but hypertuning did not apply.  It was the most difficult model to setup as the parameters were hard to set without throwing exceptions, and I had to do some google searching to set the appropriate parameters.  The model failed to save like the other models, and I can only assume its structure is radically different.  I did some initial research on how to save the model, but determined it was not worth the effort given this was an extra model.

Summary:
Of the two models that met the minimum requirements, I would choose the Random Forest Classifier.  It had the best score, the model could be saved, and without hypertuning it scored perfectly on the training data.  I think what I would focus on to make the models better is tuning which features or inputs provide the best results.  I used all columns provided, but in all likelihood some models may have performed better focusing with fewer.  If I had more time, I would have tested the models without the 'err' values or with just a few.  A goal would maybe reduce the inputs to 20 or 25.