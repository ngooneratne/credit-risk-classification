-----------------------------------------------------------------------------------------------------------------------------------------------------------------
# ANALYSIS

## Overview of Project
This project involved performing an analysis on a data set titled "lending_data" that consisted of various loans and information regarding those loans such as loan size, interest rate, derogatory marks, loan status, etc. To analyze this data, supervised machine learning models were utilized in order to evaluate loan risk. The loan status was predicted by the model, using various other variables to predict loan status. 
The steps taken to implement machine learning models on the data included separating the data into x and y variables, splitting the data into testing and training categories, fitting and predicting models, resampling the data with the RandomOverSampler tool and making a new model based off of that, and evaluating models for accuracy and error.

## Results
* Machine Learning Model 1:
  * This machine learning model was a simple logistic regression model created by separating the data into x and y variables. The y variable consisted of the response variable: loan status, and the x variable consisted of the explanatory variables - every other variable in the dataset except for loan status.
  * the x and y variables were split into training and testing subcategories and the model was created using the x and y training data. Then the model was used to predict values for x test data and it was evaluated.
  * The balanced accuracy score for the simple logistic regression model was just over 95% accurate. This accuracy score is high and we can be confident that the model is usable and accurate when it comes to predicting loan status.
  * The confusion matrix shows that the model is really accurate with predicting healthy loans and less accurate with predicting high-risk loans but the rate of error is still rather small for both categories. It is just smaller for healthy loans likely because healthy loans had a larger data representation leading to more accurate results and less error in predictions.
  * Overall this model is accurate and reliable and I would consider this model to have useful application should it be implemented.

* Machine Learning Model 2:
  * This machine learning model was a more complex logistic regression model created similarly to the previous logistic regression model. The only difference with this model was that the data was resampled prior to being used to train the logistic regression model. The data was resampled using the RandomOverSampler so that each type of loan status (0 or 1) had an equal number of data points for more accurate results.
  * Once the data was resampled it was fed into the model in the same way as with the previous model. Results were obtained and the model was evaluated for accuracy and usability.
  * The balanced accuracy score for the resampled logistic regression model was over 99%. This is an even higher accuracy score than the previous model which was at 95% so we can be confident that this model is even more reliable in predicting loan status.

## Conclusion
I would recommend using the second model, the resampled logistic regression model, as a tool for predicting the loan status simply because it has a higher accuracy score than the simple logistic regression. This model is highly accurate at 99% accuracy and can be used to predict loan status with great confidence. Performance depends on the problem we are trying to solve. In the case of credit risk, it is more important to correctly predict the high risk cases (loan status = 1) than it is to predict the low risk cases (loan status = 0) because those are the cases in which capital is lost and preventing that is extremely important. This is why the resampled data model is better because it has an equal amount of data for both the loan status = 1 and loan status = 0 categories whereas the simple logistic regression model had much more data for loan status = 0 just because that was more often the case. This is another reason why the resampled logistic regression model is a better option.
