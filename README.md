# priceofacar
GitHub Repository for work done on Professional Certificate in Machine Learning and Artificial Intelligence - Oct 2024

# Practical Application Assignment 11.1: What Drives the Price of a Car?

**Contents**

 * [Introduction](#Introduction)
 * [How to use the files in this repository?](#how-to-use-the-files-in-this-repository)
 * [Business Understanding](#Business-Understanding)
 * [Data Understanding](#Data-Understanding)
 * [Data Preparation](#Data-Preparation)
 * [Regression Model](#Regression-Model)
 * [Findings](#Findings)
 * [Next steps and Recommendations](#Next-steps-and-Recommendations)

 
## Introduction

This repository contains the Jupyter Notebook for the Application Assignment 11.1. This takes a sample jupyter notebook to complete the exercise to analyse Kaggle used car data in the data folder of this repository to build a machine learning application that evaluates if vehicles features like Fuel, Condition, Type, Color etc. can be used to determine used car prices for the Car Dealership and Sales Team. This evaluation will help the Car Dealership with fine tuning their inventory by stocking cars that consumers are interested in.

## How to use the files in this repository?

The notebooks are grouped into the following categories:
 * ``data`` – vehicles.csv data file from Kaggle Machine Learning dataset repository used in the notebooks
 * ``images`` – Image files used in Notebook and Project Description
 * ``notebook`` – What Drives the Price of a Car Notebook


## Business Understanding

The business objective is to identify key features for used car prices based on the dataset provided so that Car Dealers and their Sales Team can use these key features to understand the cars that they need to have in their inventory to increase sales.

For this application, we used a machine learning process which starts with gathering the data, cleaning, preparing and manipulating the data, training the model then testing to get predicted values and measure model accuracy. As part of the life cycle, additional data from sales should be used on an on-going bases to “improve” the model which leads to higher prediction accuracy on the factors that  consumers are looking for in used cars. 



## Data Understanding

The first thing that was apparent from the provided data was that it was not clean, it had missing values and some of the values were not realistic for used cars, for example, odometer with zero and single digit values; price with zero and single digits values.

The dataset contains 426,880 entries and 18 columns, including key attributes like price, year, manufacturer, model, condition, odometer reading, fuel type, and transmission. However, there are missing values in several columns, especially condition, cylinders, size, and VIN.

As you can see from the Diagram above, there are car prices with zero value for all conditions.

## Data Preparation

Summary of the Data Preparation is as follows:
- Remove records with Zero Prices and Odometer values
- Remove records where some of the factors are not populated
- Drop a number of factors (i.e., VIN, id, region etc.) that are not significant in user car price determination
- Review and remove the other factors (i.e., state, paint color, manufacturer, transmission etc.) and check if they have an impact on car price based on the provided data
- Filtering the data based on year on manufacture = 1990 as the number of vehicles before 1990 were very low


## Regression Models

We ran a number of models (5 to be exact) to create 5 ML Models or AI Applications using the full set of features after data manipulation and a subset of features based on the correlation matrix between the features and used car prices. 

Additional filtering (i.e., Price and Odometer > 4000 and Year > 2000) were also used to create datasets used from some of the models below.
