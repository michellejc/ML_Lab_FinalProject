# Mental Health in the Tech Industry
By: Michelle JanneyCoyle, Masters of Data Science student at the Universtity of San Francisco (class of 2021)

## Research Question
Can we predict if a participant has sought treatment for a mental health condition based on survey responses related to mental health and work environment? 

Answering this question can help companies provide more effective support for those who might not otherwise seek out help and/or for mental health professionals who work with individuals in the tech industry.

## Notebook
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://github.com/michellejc/ML_Lab_FinalProject/blob/main/Modeling_Notebook.ipynb)

## Table of Contents
- Data Description 
- Data Preprocessing 
- Modeling
- Takeaways

## Data Description 
kaggle: https://www.kaggle.com/osmi/mental-health-in-tech-survey/data
The dataset from kaggle is a CSV of survey responses collected in 2014. The survey asked questions related to work environment and mental health. There are 26 features and 1259 rows

## Data Preprocessing
The data set is fairly clean so it necessetated faily little cleaning. In my analysis I drop Comments, State, and Work_interfere because they feature a significant number of missing values. I also choose to exclude timestamp because I do not want time to confound the findings.  Age is binned into 7 categories. 

## Modeling 
The model selection process takes place in two distinct steps. 
The first step selects three main candidate models using a random cross validation search and compares f1 and ROC scores. The top three scoring models are **SVC**, **Ridge Classifier**, and **Random Forest Classifier**. 

The next step uses Randomized Search CV to tune the hyperparameters for each of the three candidate models. The model that has the higest scores after tuning is **Ridge Classifier**

## Feature Importance

After selecting a candidate model I explore feature importance by running permutation importance and selecting the top ten features by mean importance (seen below). These importance are relative to this model, however they may be a helpful indicator for future modeling and/or for those interested in helping individuals in the tech industry seek help 

<img width="1393" alt="Screen Shot 2021-03-07 at 2 27 34 PM" src="https://user-images.githubusercontent.com/67610529/110257132-44e6ff80-7f51-11eb-97ae-f23804759976.png">

## Takeaways 
The final f1 and ROC scores (seen on the right suggest that predicting if someone has sought treatment from survey responses is possible. This is a positive outcome because it means that it is possible for companies to understand their staff through surveys and implement additional programming to help increase occurrences of seeking help.

However, Further modeling is necessary. This exploration just scratched the surface, and there are many opportunities for feature engineering and complex modeling that were not explored here. 




