# Funding Success Analysis Report

## Overview

This analysis evaluates the best machine learning model combination, 'the best neural network' that will help the nonprofit foundation Alphabet Soup select the applicants with the best chance of success in their ventures.

## Results

* Data Preprocessing
    * The target variable has the label IS_SUCCESSFUL.
    * The feature variables have the labels APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT.
    * The variables EIN and NAME are neither a target nor a feature so they are removed.

* Compiling, Training, and Evaluating the Model
    * With three layers (80 neurons on input layer, 30 neurons on hidden layer, 1 neuron on output layer) using relu and sigmoid activation functions, the highest predictive accuracy of 74% on train data and 73% on test data were reached.
    * The target predictive accuracy of higher than 75% was not attained.
    * To increase model performance, the following were attempted:
        * Some columns (features) were dropped.
        * More bins were created for rare values of ORGANIZATION, INCOME_AMT, and ASK_AMT.
        * Input layer's input dimension is adjusted when column(s) is(are) dropped or bin(s) is(are) created.
        * Number of layers, number of neurons and different activation functions were used, with manual tuning and HyperParameter Tuning.
        * Number of epochs was changed, used 50 or 100.

## Summary

The overall results of this analysis reached moderate success only, the predictive accuracy peaking at 74%, with different configurations used. The hyperparameter tuning was used many times and some columns rare values were binned but that didn't help find a neural network model that hits the target performance of higher than 75% accuracy.

Since this is a classification learning, a Logistic Regression could also solve this problem.
