# TL;DR

This project is based off the Ames IA Housing Price dataset from Kaggle (https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data). As the name suggests, the idea is to predict housing prices based off different attributes such as square footage, quality/condition, location, etc. 
<br>
<br>
The first part of this project which is found in the in the EDA and Transformation sections of the attached Colab notebook walks through general EDA, pre-processing, feature engineering, and feature selection. The data as received from Kaggle contains a lot of null values which needed to be cleaned up before any modeling takes place. Luckily, after closer inspection of the data dictionary (data_description.txt), it seems as though a lot of the null values corresponded to a house not containing a feature such as a basement, garage, or pool. After cleaning, a few features were created to reduce any potential multicollinearity, and a handful of features were highlited as potential predictors of housing price, based off correlation. TotalSF (TotalBsmtSF + 1stFlrSF + 2ndFlrSF'), OverallQual, Neighborhood, KitchenQual, GarageCars, and TotalBaths (FullBath + BsmtFullBath + 0.5*(HalfBath + BsmtHalfBath)) seem to be good indicators of price. Further more, it seems as though interaction terms between TotalSF and OverallQual provide a better fit against SalePrice and thus will be explored in the Modeling portion of the notebook.
<br>
<br>
Modeling part I relies soley on standard linear regression using sk-learn's LinearRegression(). Both simple linear regression and multiple linear regression are used to predict SalePrice.
<br>
<br>
Modeling part II utlizes regularization, specifically Lasso (L1), Ridge, (L2), and Elastic Net regressions. Additional predictors are passed in these models, as the L1 and L2 coefficients are able to penalize non-important features so that the model is not overfit. 
