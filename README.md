# Ensemble Project
This project includes 2 subprojects:
1. Predict Airbnb prices in New York City using ensemble models
2. Implement a decision tree from scratch in Python, which allows us to deal with both regression and classification tasks.
## Sub-Project 1: Predicting Airbnb Prices in New York City
### Overview
The first sub-project aims to predict Airbnb prices in New York City using ensemble machine learning techniques such as Random Forest, XGBoost, CatBoost, Adaboost, Bagging, and Gradient Boosting. The dataset will be preprocessed, and exploratory data analysis (EDA) will be performed, along with feature engineering. The performance of each model will be evaluated using evaluation metrics such as Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and R-squared.
### Installation
To run the code for this sub-project, please make sure that you have installed the following libraries:
- pandas
- numpy
- matplotlib
- seaborn 
- scikit-learn
- scipy
- sklearn
- statsmodels
- itertools 
- xgboost 
- catboost
### Usage
To run the code, please follow the steps below:
- Download the kaggle.json file.
- Open the Jupyter Notebook file Airbnb_Price_Prediction.ipynb and load the dataset directly from Kaggle.
- Run each cell in the notebook.

*Note - You can also download the dataset from [here](https://www.kaggle.com/datasets/dgomonov/new-york-city-airbnb-open-data) and upload it in the notebook.

### Results
The results show that CatBoost model (Scenario 3 - predicting on log price and using all data and features) performs the best with an R-squared value of 0.609483, an RMSE of 0.439591 and an MAE of 0.307836.
## Sub-Project 2: Implementing a Decision Tree from Scratch in Python
### Overview
For the second sub-project, we will implement a Decision Tree from scratch on Python, which will be able to handle both regression and classification tasks. We will use two datasets for this purpose, one for regression and the other for classification.
1. For the regression task, we will use the make_regression() function from Scikit-learn to generate a synthetic dataset. The dataset will have 2000 samples, 5 features, and 1 target variable. We will then evaluate the performance of the Decision Tree using various metrics such as Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and R-squared.
2. For the classification task, we will use the load_wine() function from Scikit-learn to load the wine dataset before splitting into training and testing set. We will then fit the Decision Tree model to the training set and evaluate its performance on the testing set using accuracy.
### Installation
To run the code for this sub-project, please make sure that you have installed the following libraries:
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- scipy 
- collections 
- sklearn
### Usage
To run the code, please follow the steps below:
- Open the Jupyter Notebook file Decision_tree_classifier_regressor.ipynb.
- Run each cell in the notebook.
### Results
The results show that the decision tree performs well for both classification and regression tasks. For the classification dataset, the decision tree achieves an accuracy of 0.916, while for the regression dataset, the decision tree achieves an R-squared value of 0.83.
