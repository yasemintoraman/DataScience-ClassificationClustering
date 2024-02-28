# DataScience-ClassificationClustering

#### First of all, I found the "mole2_dataset" to use in this project. This dataset about moles contains features which will help us identify whether the mole is velus, melanoma, seborrheic keratosis or basal cell carcinoma.(Last column is response variable). Then I followed the steps below in the required order: <br> 
1. Split your data into train (80%) and test (20%) datasets using caret’s createDataPartition function.<br> 
2. Use the skim_to_wide function in skimr package, and provide descriptive stats for each column. <br>
3. Predict and impute the missing values with k-Nearest Neighbors using preProcess function in caret. <br>
4. After you impute missing values, use variable transformations. Convert all the numeric variables to range between 0 and 1, by setting method=range in preProcess function. <br>
5. Use caret’s featurePlot() function to visually examine how the predictors influence the predictor variable. <br>
6. <br>
   a. Use train() function to build the machine learning model. Choose knn algorithm. <br> b. Make predictions for test data using the predict() function. <br> c. Construct the confusion matrix to compare the predictions (data) vs the actuals (reference). <br> 
7. <br>  a. Use train() function to build the machine learning model. Choose random forest algorithm. <br>  b. Make predictions for test data using the predict() function. <br> c. Construct the confusion matrix to compare the predictions (data) vs the actuals (reference). <br>
8. <br> a. Use train() function to build the machine learning model. Choose naïve bayes classification algorithm. <br> b. Make predictions for test data using the predict() function. <br> c. Construct the confusion matrix to compare the predictions (data) vs the actuals (reference).  

## The Project Result

#### I compared the final results I found in steps “6-8” and came to the following conclusions about them: <br>
Random Forest, KNN and Naive Bayes also seem to have the ability to correctly recognize and distinguish negative classes in all 3 models, as their specificity values are high. Positive prediction values are high in Random Forest, which shows us that the model is capable of correctly recognizing and distinguishing positive classes. In addition to Random Forest, KNN and Naive Bayes have a weaker ability to recognize and distinguish positive classes because their positive prediction values are low. <br><br> The inter-class sensitivity values of the model we trained with KNN are low. While the sensitivity values between classes of the model we trained with random forest are more balanced and higher, the model we trained with naive Bayes is similar to random forest, but the sensitivity values between classes are different.<br><br>  Random forest has higher accuracy and kappa values than the other two models. This model seems to better balance cross-class sensitivity. <br> KNN seems to be a model with low inter-class precision. The success of this model is quite low, especially in the "basal cell carcinoma" class. <br><br> Naive Bayes has an average performance compared to the other two models in terms of accuracy and kappa values. However, sensitivity values between classes appear to be more unstable than other models. Inter-class sensitivity values show us the rate of correct classification of each class. For example, we observe that since the inter-class sensitivity of the model we trained with knn is low, the success of correctly predicting the class in this model is poor. <br><br>  According to the data we obtained, we can say that the Random Forest model has a better performance in general.



