# module-9
Model Selection and Regularization

Live Session Notes:

## Office Hour with Savio Saldanha:
-- Review StandardScaler with scikit-learn
-- Review TransformedTargetRegressor

## For further study
-- Look at quantile transformation when you require a normalized distribution after the transformation has been applied.
-- Review Scikit-Learn's "Permutation feature importance API" for determining if a feature has a higher impact on a dataset.

## Notes
Pipe.get_params() gets the params used in a model defined in a pipe.

Need to review using SciKit-Learns GridSearchCV with Pipe.get_params().  This allows a model to get excersised on the same dataset using various configuration parameters.

Use Pandas help function: help(GridSearchCV) to get documentation.
along with GridSearchCV.cv_results_ and GridSearchCV.best_score_ for getting the results produced by the model being tested.

Example using TransformedTargetRegressor can be found in "colab_activity9_1-Sequential_Feature_Selection.ipynb"
