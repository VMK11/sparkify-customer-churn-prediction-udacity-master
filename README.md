# Udacity Capstone Project - Predict Customer Churn Rate - Sparkify


## Project Overview

**Sparkify is a simulated popular music service** similar to Spotify with a **subscription-based business model**. Each user can listen to their favorite music every day either through the **free-tier** plan or by using a **subscription plan where she pays a fixed monthly fee**. Users can **modify their subscription at any time**, so it's critical to know in advance which users are going to cancel their subscription.

## Problem Statement

The project's **goal** is to provide answers as to:<br>

1. Which users are at risk of churn

By **identifying the users before they churn**, Sparkify can **engage with them** the make them a more appealing offer and keep the customer active. That can potentialy reduce the costs of acquiring new customers.

Due to resouce and time limitations we didn't had the time to train and tune as many models as we would like. As a result, one **binary classification models** was trained , where the target variable is 0 if the customer did not churn and 1 otherwise.

**To identify the best model** that helps us in predicting customer churn, we complete the following tasks: <br>

- **Analyze and preprocess the data**
- **Use Machine learning pipelines**
- **Train the classifier on the training set**
- **Test each model on the test set**
- **Hyperparameter tuning and cross-validation**
- **Model evaluation**

Finally, a **flask based web app** is built where someone can **enter the information about the user** and get **classification** based on the model prediction

## Installation

* Python3
* Pyspark
* Numpy, Pandas
* Data Visualization: Seaborn, Matplotlib, ppscore
* Web App: Flask 


## File Description

```bash
- WebApp
  - templates
    - master.html 
    - go.html 
  - static
    - githublogo2.png  
    - images.png 
  - run.py  
  - cvModel_gbt.mdl 
    - stages
    - metadata
  - Sparkify.ipynb # Jupyter notebook that contains detailed data analysis and model building with Spark (Pyspark and SparkML libraries) ran on the small subset
  - Sparkify_ibm.ipynb # Jupyter notebook that contains the analysis ran using the full available dataset on AWS EMR
```
## Instructions for running the web app:

1. Run the following command **in the app's directory** to run the web app. `python run.py`
2. Go to http://0.0.0.0:3001/ to see the web app. # the port depends on the execution.

## Future Improvements

To improve the performance: <br>

- Spend more time on hyperparameter tuning.
- Find another way to deal with unbalanced data.
- Due to time/resources limitations the model is trained is a small subset. The mdoel must be trained using the entire dataset.

## Special thanks to

- https://github.com/LFattorini
- https://github.com/anand9499
- https://github.com/drnesr

## Licensing, Authors, Acknowledgements.

This project has been completed as part of the Data Science Nanodegree on [Udacity](www.udacity.com). The data was provided by Udacity.
