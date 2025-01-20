# module-9
Model Selection and Regularization

Live Session Notes:

## Office Hour with Savio Saldanha:
- Review StandardScaler with scikit-learn
- Review TransformedTargetRegressor

## For further study
- Look at quantile transformation when you require a normalized distribution after the transformation has been applied.
- Review Scikit-Learn's "Permutation feature importance API" for determining if a feature has a higher impact on a dataset.

## Regularization 
Regularization involves techniques that are used to optimize machine learning models by minimizing the adjusted loss function and preventing overfitting or underfitting. Ridge## regularization (L2) and LASSO regularization (L1) are the two main types of regularization.
- Ridge regularization (L2) is a regularized version of linear regression. Having a regularization term when added to the cost function forces the learning algorithm to fit the data and keep the model weights as small as possible. Ridge regression uses the L₂ norm of the vector w, which is the vector of the feature weights.
- LASSO regularization (L1) is another regularized version of linear regression that adds a regularization term to the cost function but uses the L₁ norm of the weight vector w.

Things to note about Ridge Regression:
- this type of regression is used to prevent overfitting by adding a penalty to the regression coefficients.
- when a larger alpha is introduced it reduces the complexity of the model by shrinking the coefficients toward zero. 

## Notes
- Pipe.get_params() gets the params used in a model defined in a pipe.

- Use Pandas help function: help(GridSearchCV) to get documentation along with GridSearchCV.cv_results_ and GridSearchCV.best_score_ for getting the results produced by the model being tested.

- Example using TransformedTargetRegressor and GridSearchCV can be found in [colab_activity9_1-Sequential_Feature_Selection.ipynb](module-9/edit/main/colab_activity9_1-Sequential_Feature_Selection.ipynb)
