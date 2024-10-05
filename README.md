# Overview

In this project, I developed a mobile specification classification model using the Azure Machine Learning Python SDK v2, complemented by Azure AutoML for comparative analysis. The project involved creating an end-to-end machine learning pipeline that included data preprocessing, feature engineering, model training, performance fine-tuning, and deployment—all within Azure’s scalable cloud environment.

I utilized Azure ML SDK v2 to build a manually optimized pipeline and compared its performance against an AutoML approach. The AutoML method achieved an weighted F1 score of 90%, while the manually optimized pipeline reached an impressive weighted F1 score of 97%. This comparison underscores the effectiveness of manual feature selection and model tuning in enhancing classification accuracy, demonstrating the advantages of tailored machine learning solutions over automated ones.

# Azure AutoML Implementation

## Step 1: Split Data

The dataset is divided into training (0.8) and testing sets(0.2). The training set is used for cross-validation (k=5) to ensure reliable model performance and the testing set is used for evaluation. 

## Step 2: AutoML Training

AutoML trains on the training data with 5-fold cross-validation, testing multiple models. These are the parameters for AutoML. 
Featurization=TabularFeaturizationSettings(mode="Auto"), timeout_minutes=15, 
        trial_timeout_minutes=2, 
        max_trials=60,
        enable_early_termination=True,

## Step 3: Model Evaluation

The best model is selected and evaluated on the test data, and its performance is measured using the weighted F1 score,.... to assess its classification accuracy.

![image](https://github.com/user-attachments/assets/e528d936-b651-495f-b81b-6eb5bbe00e04)


![image](https://github.com/user-attachments/assets/d208d152-c918-40da-906b-1f172ae2e0c8)

# Manually Optimized Azure ML Pipeline

## Data Preprocessing

## Feature Engineering

## Model Selection

## Model FineTuning 

## Evaluation 
