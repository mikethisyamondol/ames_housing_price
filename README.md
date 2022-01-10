# TL;DR

This project is based off the Ames IA Housing Price dataset from Kaggle (https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data). As the name suggests, the idea is to predict housing prices based off different attributes such as square footage, quality/condition, location, etc. 
<br>
<br>
The first part of this project which is found in the "Ames IA Housing Prices - EDA" notebook walks through general EDA, pre-processing, feature engineering, and feature selection. The data as received from Kaggle contains a lot of null values which needed to be cleaned up before any modeling takes place. Luckily, after closer inspection of the data dictionary (data_description.txt), it seems as though a lot of the null values corresponded to a house not containing a feature such as a basement, garage, or pool. 
