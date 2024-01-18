# Movie Recommendation System Using Collaborative Filtering

## Overview

![recommendations readme](https://github.com/Perception-ui/phase_4/assets/139771882/39015c1f-e986-43fc-8570-95464634040b)

This project involved developing a movie recommendation system using collaborative filtering techniques on the MovieLens dataset. The goal was to provide users with personalized top 5 movie suggestions based on their preferences and historical ratings.

The document covers the full data science life cycle from business understanding, data cleaning, exploratory analysis, modeling, evaluation, to final model deployment.

## Business Understanding
The key business objective was to elevate user engagement and satisfaction on a streaming platform by offering tailored movie recommendations. This could lead to extended time spent on the platform and increased revenue.

The success metrics focused on measuring the accuracy, relevance, and user satisfaction provided by the recommendation system. Metrics like RMSE, precision, recall were crucial.

Research questions revolved around understanding which movie features have the highest correlation with user ratings, how rating frequencies influence accuracy, and evaluating the collaborative filtering performance.

## Data Understanding

The MovieLens dataset consists of 100,000 ratings from 610 users across 9,742 movies ranging from March 1996 to September 2018.

It comprises 4 key data files - movies, links, ratings, tags. The movies and ratings files were the primary data sources.

The movies file contains movie titles, genres. The ratings file has details of user ratings on a 5-star scale.

## Data Preparation

Data preparation involved merging the key movies and ratings data files into a single DataFrame using pandas.

Extensive data cleaning was performed - missing value treatment, duplicate removal, feature engineering (extracting hour and month from timestamps).

## Exploratory Data Analysis
Both univariate and bivariate analyses were performed:

Analyzed peak hourly and monthly viewing trends and rating patterns

Computed average ratings per user and overall distributions

Studied correlations of ratings with genres using plots and heatmaps

Identified most frequently rated and highest/lowest rated movies

## Model Building

Leveraged Surprise library to develop a collaborative filtering recommendation system

Compared multiple techniques - KNNBasic, KNNBaseline, KNNWithMeans, SVD

Tuned hyperparameters using grid search to improve RMSE

Final model: Matrix factorization SVD algorithm with 50 latent factors and 0.05 regularization that obtained the lowest RMSE of 0.8691 on the test set.
Model Usage

Generated movie recommendations for users by predicting their rating for all movies using the trained SVD model.
Returned top 5 movies with the highest predicted ratings.
