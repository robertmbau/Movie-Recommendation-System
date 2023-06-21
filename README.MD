# MOVIE RECOMMENDATION SYSTEM

**Contributors**:
 [Dennis Mwanzia](https://github.com/DennisMwanzia),
 [Amos Kipkirui](https://github.com/Amoskipkirui),
 [Robert Mbau](https://github.com/robertmbau),
 [Fiona Kungu](https://github.com/Fiona-Kungu),
 [Maureen Kitanga](https://github.com/ndungek),
 [Edwin Muhia](https://github.com/rurungamuhia)

 <img src= "Images/movie.png" alt="Movie Recommendation" > 

## Overview
MovieXplosion, a new streaming platform wants to improve their user satisfaction. The performance of the platform is dependent on how they can keep user engaged, one way to do this is by providing tailor-made recommendations to the users to drive them to spend more time on the platform.
The project aims to develop a system that suggests movies to users. We will implement this using collaborative filtering, content-based filtering and hybrid approaches.

## Problem Statement
The current system that the platform employs does not provide suitable recommendations to users which has led to low user engagement, satisfaction and retention. The system also has no way of providing new users with good recommendations and the existing users do not receive tailor-made recommendations.
The new system aims to bypass these issues and provide relevant recommendations to all users.

## Data
The data used was sourced from [MovieLens](https://grouplens.org/datasets/movielens/latest/), we used the small dataset due to limited computational power.

The data contains information about movies, ratings by users and other relevant information.
The data used can be found in the folder `Data`.

## Data Preparation

The data from the website had few issues with only 8 rows with missing values in one column.
The dataframes from `ratings.csv`, `movies.csv` and `tags.csv` were merged.

## Modeling Process

Used `Surprise` library is used to load the data.
Three different models i.e `SVD`, `KNN Basic` and `KNN with Means`.
`RMSE` was used to evaluate the performance of the models.
We used `GridSearchCV` to search for the best parametres.

## Evaluation
In the intial modeling, `SVD` produced an `RMSE` of `0.87`, `KNN Basic` produced an `RMSE` of `0.97` and `KNN with Means` had an `RMSE` of `0.90`.

`SVD` was the best performing model with an initial `RMSE` of `0.87`.

By using the best parametres, `SVD` improved a bit and posted an `RMSE` of `0.86`.
## Conclusion

`SVD` is the best model for this project which is evident with it performing better than the other models.

The model was able to give top 5 predictions to a user based on their previous ratings.
The cold start problem was solved by giving new users a short survey to rate certain movies and from that the system provided recommendations.

## Citations

F. Maxwell Harper and Joseph A. Konstan. 2015. The MovieLens Datasets: History and Context. ACM Transactions on Interactive Intelligent Systems (TiiS) 5, 4: 19:1–19:19. https://doi.org/10.1145/2827872

## Repository Structure

```

├── Data
├── Images
├── Movie Recommendation Systems.ipynb
├── notebook.pdf
├── presentation.pdf
├── README.MD
└── 
```

