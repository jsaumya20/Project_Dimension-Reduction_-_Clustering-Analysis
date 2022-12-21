# Project: Dimension Reduction & Clustering-Analysis on the Housing Dataset

![image](https://user-images.githubusercontent.com/91350558/208846735-d0e08b1a-8ef8-436c-932d-1d29095cd096.png)

I will be using the well known housing data set for this project.

## Introduction
The project is to predict house sale price. With 79 explanatory variables describing (almost) every aspect of residential homes, the challenge is to predict the final price of each home. The data includes many categorical variables and traditional dimension reduction and clustering techniques cannot be applied directly to categorical data. This project explores two methods to perform house price prediction using numerical and categorical features.

Dimension reduction using
i. PCA for numerical variables
ii. MCA for categorical variables
K-medoids clustering using Gower distance

## Data Preparation
Download the dataset from https://www.kaggle.com/c/house-prices-advanced-regression-techniques/overview Remove missing value records before proceeding.

## Description
Part 1 - Dimension reduction: Dimension reduction is performed using Principal componenet analysis (PCA) for numerical features and Multiple correspondence analysis (MCA) for categorical fatures. Prediction is performed on the new features using linear regression with ridge regularization model. The model results are then compared with base model to test the performance.

Part 2: Clustering Analysis: K-medoids clustering is performed using Gower distance as a distance measure. The Gower distance is essentially a special distance metric that measures numerical data and categorical data separately, then combine them to form a distance calculation

## Finding

Part 1 - Dimension reduction:
#### After applying dimension reduction, training accuracy was 81%, test accuracy was 73.2%.
#### Number of components were reduced while tuning hyper parameters to avoid overfitting.
#### Without dimension reduction, accuracy is 73.4%. This is slightly better than accuracy with dimension reduction. Although, it could have been caused by overfitting.

Part 2: Clustering Analysis:
#### Normalized Mutual Information (NMI) is a normalization of the Mutual Information (MI) score to scale the results between 0 (no mutual information) and 1 (perfect correlation).
#### Using NMI score we are determining the score of clustering. Low NMI shows that class members are mostly dispersed among various clusters.
#### NMI for the first clustering (0.184) is the lowest It would mean we would prefer the clustering size 3
#### As number of clusters decreases, NMI score seems to improve

## References:
​
https://pyclustering.github.io/docs/0.9.0/html/d0/dd3/classpyclustering_1_1cluster_1_1kmedoids_1_1kmedoids.html
​
https://medium.com/analytics-vidhya/gowers-distance-899f9c4bd553
​
https://scikit-learn.org/stable/modules/clustering.html
​
https://scikit-learn.org/stable/modules/generated/sklearn.metrics.normalized_mutual_info_score.html
​
https://course.ccs.neu.edu/cs6140sp15/7_locality_cluster/Assignment-6/NMI.pdf
   
