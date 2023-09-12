# Code Overview

The code is written in Python and utilizes popular data science libraries such as Pandas, Matplotlib, Seaborn, NumPy, and Scipy. It also includes machine learning models from scikit-learn and XGBoost for regression tasks.

## Data Loading

The project starts by loading the training and testing datasets from the following URLs:

- Training dataset: [train.csv](https://raw.githubusercontent.com/ASatya-J107/Data_Science_Project_3_Regression/main/train.csv)
- Testing dataset: [test.csv](https://raw.githubusercontent.com/ASatya-J107/Data_Science_Project_3_Regression/main/test.csv)

The training dataset is loaded into `df_train`, and the testing dataset is loaded into `df_test`.

## Data Exploration and Preprocessing

The code performs the following data exploration and preprocessing steps:

1. Display basic information about the training dataset using `df_train.info()`.
2. Select specific columns of interest from the training and testing datasets.
3. Display descriptive statistics of the 'SalePrice' column in the training dataset.
4. Visualize the distribution of 'SalePrice' using a histogram and calculate skewness and kurtosis.
5. Create scatterplots and boxplots to explore relationships between features and the target variable.

## Data Transformation

The code performs data transformation to improve the distribution of the target variable 'SalePrice':

1. Apply a logarithmic transformation to 'SalePrice' and visualize the transformed distribution.
2. Use a QQ-plot to check the normality of 'SalePrice' after transformation.

## Feature Engineering

Feature engineering steps include:

1. Merging the training and testing datasets.
2. Handling missing values for specific columns ('MiscFeature', 'GarageArea', 'KitchenQual').
3. Encoding categorical variables ('OverallQual', 'OverallCond', 'KitchenQual').
4. Applying Box-Cox transformation to skewed numerical features.
5. One-hot encoding categorical variables.
6. Scaling the features using RobustScaler.

## Model Building and Evaluation

The code evaluates the performance of several regression models using K-Fold cross-validation:

1. Linear Regression (`LinearRegression`).
2. Lasso Regression (`Lasso`).
3. Support Vector Machine (`SVR`).
4. XGBoost Regression (`XGBRegressor`).

Each model is tested and evaluated using the R-squared score.

#### Predicting Sale Prices for New Data

The code includes a section for making predictions for new data. It demonstrates how to preprocess and transform new data and use the trained XGBoost model to predict the sale price for a sample house.
