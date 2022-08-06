# Udacity Capstone Project - Predict Customer Churn Rate - Sparkify


## Project Overview

**Sparkify is a simulated popular music service** similar to Spotify. Sparkify is a **subscription-based service** where each user can try out through the **free-tier** plan or by using a **specific subscription plan where someone pays a fixed monthly fee**. The users can **modify or cancel their subscription at any time**, so it's critical to to be able to identify which users are going to cancel their subscription (e.g. churn).

## Problem Statement

The project's **goal** is to provide answers as to:<br>

1. Which users are at risk of churn

By **identifying the users before they churn**, Sparkify can **engage with them** and make them a more appealing offer and keep the customer active. That can potentialy reduce the costs of acquiring new customers.

Due to resouce and time limitations we didn't had the time to train and tune as many models as we would like. As a result, one **binary classification models** was trained , where the target variable is 0 if the customer did not churn and 1 otherwise.

**To conclude to the best performing model** that enable us to provide an estimation with regard to the user's intention to cancel or not the subscription, the following tasks are complete: <br>

1. **Data analysis and pre-processing**
2. **ML Pipeline and experimentation**
3. **Test each model on the test set**
4. **ML Hyperparameter tuning and cross-validation**
5. **ml model peformance evaluation**

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
  - Sparkify.ipynb 
  - Sparkify_ibm.ipynb
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
