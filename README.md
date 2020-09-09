# Recommendation Systems with MovieLens Data

Jean-Paul Ventura and Yehuda Schein 
Data Science cohort 062220

## Introduction

Recommender systems aka recommndation engines are information filtering tools that predict ratings for user-product interactions in big data environments (think netflix, spotify, google etc). The broad purpose of this computational technique is to provide users with recommendations to other products and assist the company returns through driven conversion. In addition to the latter, movie recommendation systems provide a mechanism to assist data professionals and stakeholders in classifying users with similar interests. This makes them an essential part of websites and ecommerce applications and the evaluation and marketing of a user base. 

# The Data

In this exercise, we've used the MovieLens data set curated by ,, which consists of approximately 100,000 ratings of a corpus of 9,000 movies over a 600-person user base. The dataset is distributed over four csv files which contain information on ratings, movies, links and tags. For our purposes we've only considered the **ratings** and the **movies** datasets with some additional information obtained by tmdb api calls to select movie titles from tmdb-specific coded movie ids native to the curated dataset.

**Ratings**

the ratings dataset is comprised of 100,836 observations which are records of the user id(userId), the id of the movie that was rated by said user (movieId) and the time at which the rating was recorded (timestamp).

**Movies**

the movies data table consists of tthe ID of the movies (movieId), the corresponding title (title) and genre of each movie (genres)

### Data Preprocessing & Structuring

xxxxx

## The Models

xxxxx

## Feature Engineering

**Average Rating**

Since the dataset is a collection of ratings by a number of different users for various movies, we compute the average rating for each movie in the dataset.

**Total Number of Ratings**

To some degree, the rating of a movie can be interpreted to be proportional to the total number of ratings it has. Therefor, we also consider the total number of ratings submitted for each movie.

## Insights and Suggestions

## Future Directions
