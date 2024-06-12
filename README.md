# Comparing Feature Selection Methods
The first approach is using sequential feature selection to sequentially add or delete features and only use those that improve the model. 
The second approach is using a regularized model to identify features based on non-zero coefficients. 
This activity focuses on comparing variations of both these methods.

Using both the SequentialFeatureSelection and RFE (recursive feature elimination) to build and compare regression models. 
Consider the following feature selection methods (leave all other arguments to default besides the estimator and n_features_to_select arguments):
- Ridge regressor to extract coefficients
- SequentialFeatureSelection using the Lasso to select 4 features
- RFE using Lasso to select 4 features.
For each of these, fit the training data X_train, y_train below. Compare the magnitude of the results of your Ridge model to those that result from feature selection methods.

### The Data
For this problem a dataset with information on red wine chemical compositions and their quality is given. Your goal is to use the properties of the wine to predict the quality. Below, the data is loaded and train/test splits constructed.

### Conclusion:

- All 3 models selected alcohol, volatile acidity and sulphates as top 3 features, however there is difference in 4th feature selected by these models 
- Lasso resulted in Zero coef for 4th feature for both SFS and RFE
- Also, note that the coefficients are same for top 3 using Lasso with SFS and RFE
- Selected best alpha and features (with Coefficients) by each models are shown below in descending order (using absolute values)

<img width="170" alt="image" src="https://github.com/mitbans/comparing-feature-selection-methods/assets/166747739/1eb208b0-dd8e-4dcd-b30d-e916f9eda3de"> <img width="252" alt="image" src="https://github.com/mitbans/comparing-feature-selection-methods/assets/166747739/7dc333f2-3bf5-43f5-b120-1adeda6593bb"> 
<img width="280" alt="image" src="https://github.com/mitbans/comparing-feature-selection-methods/assets/166747739/071625dc-616e-4d6f-b9b9-bce2064aedbc">

<img width="214" alt="image" src="https://github.com/mitbans/comparing-feature-selection-methods/assets/166747739/dec94625-d9cb-4f32-aac5-3dd2b58abd47">  <img width="213" alt="image" src="https://github.com/mitbans/comparing-feature-selection-methods/assets/166747739/798ea8f4-3f7e-4c48-9685-c7ccc282dacf">

Comparing the MSE as shown below, there is no difference in SFS using Lasso and RFE using Lasso. Test MSE is lowest for Ridge.

<img width="262" alt="image" src="https://github.com/mitbans/comparing-feature-selection-methods/assets/166747739/50cb0c8c-67de-43db-831d-927da0d723ab">

## Repository Structure
- <code>data/</code>: Contains dataset used in the analysis.
- <code>notebooks/feature_selection_methods.ipynb</code>: Jupyter notebook with code for data analysis.
- <code>README.md</code>: Summary of findings and link to notebook

## Notebook
The detailed analysis and code can be found in the Jupyter notebook <a href="https://github.com/mitbans/comparing-feature-selection-methods/blob/main/notebooks/feature_selection_methods.ipynb">here</a>.
