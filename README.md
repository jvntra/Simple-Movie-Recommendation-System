# Recommendation Systems with MovieLens Data

Jean-Paul Ventura and Yehuda Schein 

Data Science cohort 062220

## Introduction

Recommender systems aka recommendation engines are information filtering tools that predict ratings for user-product interactions in big data environments (think netflix, spotify, google etc). The broad purpose of this computational technique is to provide users with recommendations to other products and assist the company returns through driven conversion. In addition to the latter, movie recommendation systems provide a mechanism to assist data professionals and stakeholders in classifying users with similar interests. This makes them an essential part of websites and ecommerce applications and the evaluation and marketing of a user base. 

## The Data & Context.

In this exercise, we've used the MovieLens small-dataset curated by the Grouplens research lab at the University of Minnesota. The content consists of approximately 100,000 ratings of a corpus of 9,000 movies with 3600 tags submitted by a 600-person user base. The dataset is distributed over four csv files which contain information on ratings, movies, links and tags. For our purposes we've only considered the **ratings** and the **movies** datasets with some additional information obtained by tmdb api calls to select movie titles from tmdb-specific coded movie ids native to the curated dataset.

**Ratings**

the ratings dataset is comprised of 100,836 observations which are records of the user id(userId), the id of the movie that was rated by said user (movieId) and the time at which the rating was recorded (timestamp).

**Movies**

the movies data table consists of tthe ID of the movies (movieId), the corresponding title (title) and genre of each movie (genres)

### Data Preprocessing & Structuring



## The Models

We chose to use two models to address two approaches in collaborative filtering recommendation engines. These models are KNN which is a Neigborhood-Based method of filtering (making automatic predictions) and SVD which is a model based method. 

**KNN:** 
    KNN is a machine learning algorithm to find clusters of similar users (neighbors) based on common movie ratings, and make predictions using the average rating of top-k nearest neighbors. It uses the weighted-average of the k-most similar neighbors to issue a predicted rating.

**SVD:** 
    SVD is another machine learning algorithm that tries to explain complex relationships between variables in a dataset by decomposing the dataset or matrix and centering on latent relationships much like PCA.
    It is found to be the most accurate approach to reduce problems with sparsity in the data as all users do not rate all movies leading to sparsity in the data. Another useful feature is that SVDs create embeddings (analogous to principle component loadings) which are low-dimensional hidden factors which for a certain user and item coupling can represent exogenous features of the data like how political a movie is, how much special effects it contained and perhaps how dialogue driven the movie is.
    
    
**Evaluation Metrics:**

   For our chosen models we primarily focused on RMSE as an evaluation metric since we want to evaluate how good our model predicts ratings a given user and movie. A lower RMSE is indicative of improved performance across model runs.

We focus on RMSE over MAE as our evaluation metric because RMSE penalizes larger errors more than MAE. They are both indifferent to the direction of errors and they are negatively oriented which means lower scores are better.

**KNN vs SVD:**

| KNN                                 | SVD                                                  |
|-------------------------------------|------------------------------------------------------|
| Complete input data is required     |Creates an abstraction that represents data (like PCs)|
| Does not scale well                 |Scales well|
| Pre-computation not possible        |pre-computation possible|
|Relies on user-itemsimilarity metrics|Relies on matrix factorization|

## Feature Engineering

**Average Rating**

Since the dataset is a collection of ratings by a number of different users for various movies, we compute the average rating for each movie in the dataset.

**Total Number of Ratings**

To some degree, the rating of a movie can be interpreted to be proportional to the total number of ratings it has. Therefor, we also consider the total number of ratings submitted for each movie.

## Insights and Suggestions

