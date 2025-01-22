# module-9
Model Selection and Regularization

## Course Notes:

### Cross Validation
- Holdout Cross Validation : As part of this method, you randomly divide your data into two sets: the training set and the test/validation set (i.e., the holdout set). This technique has the advantage of performing well on unseen datasets.  This type of cross validation is the simplest from and is also known as "Simple Cross Validation".  As a disadvantage, if you dataset is small then this might not be the best choice being that part of your dataset is reserved for testing.
- K-Fold Cross Validation : uses unseen data to estimate the performance of a model. Using this technique, hyperparameters (k-values) can be tuned to the optimal level to train the model. In addition, this approach has the advantage of using each example only once for training and validation (as part of a test fold).  Here the disadvantage is that the process of selecting your trainging and validation data is process intensive.

### Regularization 
Regularization involves techniques that are used to optimize machine learning models by minimizing the adjusted loss function and preventing overfitting or underfitting. Ridge regression (L2 regularization) and LASSO regression (L1 regularization) are the two main types of regularization.
- Ridge regression (L2 regularization) is a regularized version of linear regression. Having a regularization term when added to the cost function forces the learning algorithm to fit the data and keep the model weights as small as possible. Ridge regression uses the L₂ norm of the vector w, which is the vector of the feature weights.  Basically this uses the "sum of the squares of the features * alpha" as the penalty term.
- LASSO regression (L1 regularization) is another regularized version of linear regression that adds a regularization term to the cost function but uses the L₁ norm of the weight vector w.  So for each feature, instead of the sum of the squares as the penalty term like L2 regulariztion it uses the sum of the absolute values multiplied by alpha.  This also provides a way for performing feature selection on datasets with a large number of features.  This type of regression is slower and less stable (i.e. convergence warning due to rounding errors and the like) but it provides a way to determine what features to use from a dataset with a lot of features.

#### Things to note about Lasso and Ridge Regression:
- these types of regression are used to prevent overfitting by adding a penalty to the regression coefficients.
- with Ridge regularization when a larger alpha is introduced it reduces the complexity of the model by shrinking the coefficients toward zero.  In the case of Lasso regularization it can reduce the value to 0 which is an indicator that the feature should not be used in the final model.

### Approaches to scaling data used in Regularization (L1 and L2)
- Standarization : 
  - creates a Z score for each feacher in a column by applying the following formula: (x − mean) / standard deviation.
  - This process is applied to each column of the dataset independently which, in turn converts the mean and variance of each column to 0 and 1 respectively.
  - Scikit-Learn StandardScaler():  This API also comes with an inverse transform that undoes the scaling that was done.
    USAGE: it solves the problem of the penalty term penalizing small features heavily in Lasso and Ridge regression. This, in turn ensures that all features contribute equally to the penalty term by scaling features to have zero mean and unit variance. 
  - Scikit-Learn GridSearchCV(): allows you to test various combinations of hyperparameters used to fine-tune a model.

## Live Session Notes:

### Office Hour with Savio Saldanha:
- Review TransformedTargetRegressor

### For further study
- Look at what quantile transformation is when you require a normalized distribution after the transformation has been applied.
- Review Scikit-Learn's "Permutation feature importance API" for determining when features have a high impact when creating a modeling using a specific dataset.
- For an understanding of how Lasso Reguarization works, do a Google search using the text string "normball".

### Notes
- Pipe.get_params() gets the params used in a model defined in a pipe.

- Use Pandas help function: help(GridSearchCV) to get documentation along with GridSearchCV.cv_results_ and GridSearchCV.best_score_ for getting the results produced by the model being tested.

- Example using TransformedTargetRegressor and GridSearchCV can be found in [colab_activity9_1-Sequential_Feature_Selection.ipynb](module-9/edit/main/colab_activity9_1-Sequential_Feature_Selection.ipynb)

- Example using Sequential Feature Selection, Rige regression and Lasso regression can be found in [codio_assignment9_4.ipynb](module-9/edit/main/codio/codio_assignment9_4.ipynb)


## Reference Guide:  
https://classroom.emeritus.org/courses/9464/pages/module-9-transcripts-and-quick-reference-guide?module_item_id=2090387