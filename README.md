# Project_4_Group_9
Project 4

## Diabetes Prediction Analysis

### Introduction

This repository contains code and analysis for predicting diabetes based on various factors using Python and machine learning techniques.

### Dataset

The dataset used for this analysis is named "Diabetes_Prediction_2018_2022.csv". It contains information about individuals' health-related attributes such as diabetes status, blood pressure, cholesterol levels, BMI, lifestyle factors, and demographic information.


#### Data Exploration

The analysis begins with exploring the dataset using pandas. Key steps include:
- Loading the dataset into a pandas DataFrame.
- Checking the first few rows, summary statistics, and data types of the variables.
- Examining the shape of the dataset to understand its dimensions.

The data contains no nulls. Many of the attributes are discrete in value, and most of these are binary. 

#### Variable Analysis

The analysis delves into understanding the relationship between various variables and diabetes status. Key steps include:
- Scaling the features using MinMaxScaler to ensure each feature contributes equally to the analysis.
- Visualizing the relationship between each feature and diabetes status using scatter plots.
- Creating a pairplot to visualize the pairwise relationships between different features.
- Calculating the correlation matrix to identify correlations between features and diabetes status.

Scaling had no effect on the pairplots, and scaling had no effect on the correlation heatmapping. Some variables that were more corrlated to each other when compared to other pairings were （PhysHlth, DiffWalk), (GenHlth, DiffWalk), (GenHlth, PhysHlth), (MentHlth, PhysHlth), and (GenHlth, MentHlth).
Diabetes_012 itself seemed to be the most highly correlated to GenHlth, HighBP, BMI, and DiffWalk compared to other attributes. 

#### Principal Component Analysis (PCA)

PCA is applied to reduce the dimensionality of the dataset and identify the key components contributing to diabetes prediction. Key steps include:
- Performing PCA on the dataset to extract principal components.
- Exploring the explained variance ratio to understand the contribution of each component.
- Visualizing the principal components using scatter plots and identifying the top contributing variables for each component.
- Analyzing the scatter plots for different combinations of principal components to understand their relationship with diabetes status.

This was done first without data scaling, and then again with scaling. Scaling **did** have an effect on PCA. Upon using scaling, the variability explained went from the top 3 principal components explaining 93% of the variability to then then needing the top 10 principal components to explain only 84% of the variability. 

Finding the top contributing attributes to each principal component revealed:
- **Before scaling**: mental health (MentHlth) was among the highest contributers for the top 4 principal components. For PC1, the top contributor was PhysHlth. For PC2, the top contributor was BMI. For PC3, the top was MentHlth. And, for PC4, the top contributor was Age.
- **After scaling**: Smoke was among the top contributors for PC1, PC2, and PC4. For PC1, the top contributor was HighBP. For PC2, the top contributor was Sex followed by Fruits. For PC3, the top contributor was Sex followed by PhysicalActivity. And, for PC1, the top contributor was Smoke followed by Fruits.

**Effect of scaling**: while scaling did create a PCA model whose variability isn't thoroughly explained by the first 3-5 principal components, scaling did provide principal components with more unique combinations of attributes that contributed to each component.
