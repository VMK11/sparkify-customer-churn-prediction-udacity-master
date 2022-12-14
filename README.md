# Udacity Capstone Project - Predict Customer Churn Rate - Sparkify

## Project Overview

In this project, we will attempt to identify the users that potentialy will churn from our music service. Sparkify (similar to Spotify) is a service with a subscription-based model where each user can try out the free-tier plan or use a specific monthly-based subscription plan. The users/customers can cancel their subscription at any time, so it's critical to to be able to identify those users in time and make an attempt to keep them using our services.

## Problem Introduction

Customer retention is one of the primary growth pillars for products with a subscription-based business model. In the current market the customers are free to choose from plenty of providers of the same service. There are many factors that drive the customers to churn and that could lead to both material losses and damage the damage to the  reputation would be significant.

The project's goal is to provide an answer to the question **Which users are at risk to churn** by identifying the users before they churn, Sparkify can **engage with them** and make them a more appealing offer and keep the customers active. That can potentialy reduce the costs of acquiring new customers.


## Strategy to solve the problem

In order to solve the problem the strategy below is followed:

1. **Pre-processing, cleaning & EDA** 
A basic pre-processing and an analysis of the data is performed. From that initial step, a basic data cleaning is performed e.g.  null value investigation and handling and questions like which customers churn the most, what is their gender, from which country, do they have premium or trial membership, etc. are answered. The goal was to gain a better understanding of the customer's behaviour and the data.

2. **Feature Engineering** 
In the second step, based on the analysis in the previous step some new features were created (feature engineering). e.g. the user's state, avg_songs_per_day, time feature transformation, etc.

3. **Pipeline Creation & Experimentation** 
The next step includes the ML pipeline creation and experimentation. In this stage, all the necessary data transformation steps are integrated into one pipeline. e.g. string indexer, encoders, assemblers and scalers. 

3. **ML Hyperparameter tuning and cross-validation** 
The hyper-paramter tuning step includes the process of finding the near-optimal model parameter candidates using data cross-validation. The grid-search and the BinaryClassificationEvaluator emthods were used to identify which pipeline/model performs the best in terms of performance metrics. 

4. **ML Pipeline Performance Evaluationt/Metrics**
The model's performance is evaluated using the unseen subset of the data e.g. test set. In order to have a more holistic view of the pipeline's performance the confusion matrix, accuracy, precision, recall and f-beta score are used. However, due to the highly unbalanced data only the confusion matrix and the f-1 score are used in order to evaluate the model's performance.

5. **Flask-Based Web App** 
Finally, an app is built where someone can enter the information about the user and get a classification of whether or not that user will chrun or not along with a probability estimate based on the model prediction.

## Results
The GBTClassifier were used to predict churn users and got the following performance - Consider the low performance because of the lack of time and computational resources:

Accuracy: 0.7658227848101266
Precision: 1.0
Recall: 0.05128205128205128
F1 Score: 0.09756097560975609

You can find detailed steps and results:
- In the WebApp screenshots:    https://github.com/VMK11/sparkify-customer-churn-prediction-udacity-master/tree/master/WebApp%20Screenshots
- In the notebook github repo:  https://github.com/VMK11/sparkify-customer-churn-prediction-udacity-master/blob/master/Sparkify.ipynb

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
  - Sparkify.ipynb 
  - Sparkify_ibm.ipynb
```
## Instructions for running the web app:

1. Run the following command **in the app's directory** to run the web app. `python run.py`
2. Go to http://0.0.0.0:3001/ to see the web app. # the port depends on the execution.

## Improvements/Limitations

- Use the entire dataset for training - Due to resouce and time limitations we didn't had the time to train and tune as many models as we would like.
- Spend more time on hyperparameter tuning.
- Find another way to deal with unbalanced data.
- Couldn't use the ppscore package - Power Predictive Score is a bivariate analysis
- Due to time/resources limitations the model is trained is a small subset. The mdoel must be trained using the entire dataset.

## Conclusion/Reflection
Over all the project was demanding in terms of data clearning and feature engineering. It was challenging to think about which user attributes to experiment with and what kinf of newly engineered features could provide predictive importance in the model. However, the real challenge came with the resources, the data preparation and modelling took a substancial amount of time ever during experimentation. That includes bith the IBM Watson Studio virtual machine and the Udacity workspace.

## Special thanks to

- https://github.com/LFattorini
- https://github.com/anand9499
- https://github.com/drnesr

## Licensing, Authors, Acknowledgements.

This project has been completed as part of the Data Science Nanodegree on [Udacity](www.udacity.com). The data was provided by Udacity.
