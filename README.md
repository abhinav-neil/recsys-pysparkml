# Recommender System with PySpark ML

A book recommendation system using collaborative filtering built using PySpark ML.

## Data

The dataset contains book attributes and user ratings from the Amazon bookstore <a href="https://www.kaggle.com/datasets/saurabhbagchi/books-dataset"> (source) </a>.

## Methodology

- Create spark session and load data into spark dataframe
- Feature engineering
    - Convert string cols to integer
- Model
    - Alternating Least Squares (ALS) model for collaborative filtering from Spark ML Lib
    - Fit model to train set
    - Predict on test set and evaluate root mean squared error (RMSE)
- Generate recommendations
    - Predict ratings on unrated books for each user, using fitted model
    - Recommend top-n books
