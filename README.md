# Ames Housing Price Prediction Project


## ML Assignment 1 - House Price Prediction

### Introduction
This project aims to predict house prices on the Ames housing dataset from Kaggle using regression techniques. The emphasis is on following best practices like:

- Git version control and GitHub flow
- Dependency management with poetry
- Documentation and visualizations
- Comparison of multiple regression algorithms
- The development will be done issue-by-issue. For each issue, a new branch will be created, changes made, and a pull request initiated before merging to main.

## Details

This project aims to accurately predict house prices based on a variety of features, using a dataset from a Kaggle competition. The goal is to experiment with different machine learning techniques, practice end to end machine learning workflows and build intuition around model performance.  




## 1. Data Exploration

In our first notebook, `1_data_exploration.ipynb`, we get our hands dirty with the data. We load up the Ames Housing dataset and take a good look at its structure and features. We then explore each feature, checking out their distributions, how they relate to our target variable (SalePrice), and their correlations with other features.

We use a bunch of visualization techniques, like histograms, boxplots, and scatter plots, to get a better feel for the data. We plot the distributions of numerical features like 'GrLivArea', 'TotalBsmtSF', '1stFlrSF', and 'MasVnrArea' to understand their skewness and potential outliers. We also analyze categorical features like 'Neighborhood', 'ExterQual', 'Foundation', and 'SaleCondition' to understand their unique values and potential impact on the housing prices.

## 2. Data Cleaning and Preprocessing

In the second notebook, `2_data_cleaning_and_processing_and_feature_engineering.ipynb`, we roll up our sleeves and prepare our dataset for modeling. We start by handling missing values, filling them with appropriate values based on the feature's description and our domain knowledge. For instance, missing values in features like 'PoolQC', 'MiscFeature', 'Alley', 'Fence', and 'FireplaceQu' are filled with "None" or 0, indicating the absence of that feature in the house.

We also perform feature engineering, creating new features based on our domain knowledge and insights from the EDA. For example, we create a 'TotalArea' feature that combines the total area of all floors and the basement. We also create interaction features like 'OverallQual_GrLivArea' to capture the combined effect of overall quality and above-ground living area on the housing prices.

Finally, we scale the numerical features to ensure they are on the same scale, which is important for many machine learning algorithms. We also encode the categorical variables into a format that can be provided to a machine learning algorithm.

## 3. Model Building, Training, and Evaluation

In the third notebook, `3_model_building_training_evaluation.ipynb`, we build, train, and evaluate various machine learning models for our housing prices prediction task. We start by splitting our dataset into training and validation sets. We then train different models, including Linear Regression, Random Forest, and Neural Network, on these datasets and evaluate their performance using Root Mean Squared Error (RMSE).

We also experiment with different combinations of preprocessing and feature engineering steps to see which one produces the best results. For instance, we train models on datasets where features with zero Mutual Information (MI) score have been dropped, and on datasets where further feature selection and dimensionality reduction methods, such as Principal Component Analysis (PCA), have been applied.

Throughout the process, we aim to understand the impact of our preprocessing and feature engineering decisions and guide us in improving our models. We also aim to create a system that can generate explanations for code chunks that are relevant to the goals of the notebook, helping others understand the rationale and purpose behind the code and inspire good documentation practices.

## Running the Project

This project uses [Poetry](https://python-poetry.org/) for dependency management. To run this project:

1. Clone the repository.
2. Install Poetry using the [official instructions](https://python-poetry.org/docs/#installation)
3. Navigate to the project directory and run `poetry install` to install dependencies.
4. Run `poetry shell` to activate the virtual environment.
5. Download the datasets from the kaggle link and create a folder for your data in your projects root directory.
5. Open the notebooks using Jupyter Notebook or any other notebook viewer and run the cells in order.





## References

- https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/overview

