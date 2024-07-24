# Spotify-Hit/Miss-song-predictor

This project aims to predict whether a song will be a hit or a miss based on a Spotify dataset containing songs from the 1960s to the 2010s. Various machine learning techniques are applied, including Logistic Regression, Support Vector Machines (SVM), Random Forest, and Ensemble methods. The project involves data preprocessing, hyperparameter tuning, model evaluation, and result analysis.

## Table of Contents
- [Introduction](#introduction)
- [Data](#data)
- [Preprocessing](#preprocessing)
- [Logistic Regression](#logistic-regression)
- [Support Vector Machines](#support-vector-machines)
- [Random Forest](#random-forest)
- [Ensemble Techniques](#ensemble-techniques)
- [Model Evaluation](#model-evaluation)
- [Conclusion](#conclusion)
- [Future Improvements](#future-improvements)

## Introduction

Predicting the success of songs is a challenging task that can have significant implications for the music industry. This project utilizes machine learning algorithms to classify songs as hits or misses based on various features extracted from the Spotify dataset.

## Data

The dataset contains songs from different decades, spanning from the 1960s to the 2010s. The features include various audio attributes of the songs, such as danceability, energy, tempo, etc. The target variable is binary: 1 for hit songs and 0 for misses.

## Preprocessing

Data preprocessing involves:
- Dropping categorical variables: 'track', 'artist', 'uri'.
- Splitting the data into training, validation, and test sets.
- Standard scaling of the features.
- Handling missing values (there are none in this dataset).

## Logistic Regression

Logistic Regression models are trained using different solver hyperparameters and regularization settings. The performance is evaluated on training and validation data. The choice of solver and regularization did not have a significant impact on model performance, suggesting that the dataset might be linearly separable.

## Support Vector Machines

SVM models with various kernel functions (linear, polynomial, sigmoid, RBF) are trained and evaluated. RBF kernel outperformed the others due to its ability to handle complex datasets. Hyperparameters (C and gamma) were tuned to optimize model performance.

## Random Forest

Random Forest models with different hyperparameters (n_estimators, max_depth, etc.) were trained and evaluated. Feature importance was analyzed to understand the impact of different features on prediction.

## Ensemble Techniques

Ensemble techniques like Voting and Stacking were applied to combine the predictions of different models (Logistic Regression, SVM, Random Forest). Both hard and soft Voting methods were used, and Stacking was performed with AdaBoost and GradientBoosting as final estimators.

## Model Evaluation

The final model selected was the Stacking classifier with GradientBoosting as the final estimator. The model achieved an accuracy of 0.8069, recall of 0.8457, and precision of 0.7881 on the test dataset.

## Conclusion

This project demonstrates how various machine learning techniques can be applied to predict the success of songs based on audio attributes. The best-performing model was found to be the Stacking classifier with GradientBoosting, achieving reasonable accuracy and precision.

## Future Improvements

- Gathering more data may lead to better model generalization.
- Exploring additional features or transforming existing features could enhance model performance.
- Further hyperparameter tuning could be conducted to optimize models.
- Experimenting with different ensemble techniques and architectures may lead to even better results.
