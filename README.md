## Project objectives
Big data is now utilized at every level in business context. For online book retailers, product ratings can play a huge role for making sound business decisions. As the data on product ratings continue to grow over time, companies can take advantage of this information and enhance customer experiences.
For this project I want to see whether book recommendation system help book retail in giving out the best recommendation for their customer. 

## Data Pre-Processing
For this project, I am using the data from the following link: https://www.kaggle.com/zygmunt/goodbooks-10k
The data contains 4 datasets: books.csv - metadata for each book (goodreads IDs, authors, title, average rating, etc.) - (1000 x 23), book_tags.csv - contains tags/shelves/genres assigned by users to books. Tags in this file are represented by their IDs. - (999912 x 3),
tags.csv - translates tag IDs to names - (34252 x 2), and rating.csv - contains ratings - (5976479 x 3). 

As the first step, I combined the csv files into one dataframe to ensure that only relevant features are used. Secondly, I ensure that the data is clean before I go into explaratory data analysis and modeling. 

## Explaratory Data Analysis
I look for insights I can use to enhance my book recommendation systems. The focus in the EDA is to understand which books are popular, what are the factors that influence books' popularity, and whether the books popularity are biased. 

## Modeling 
For this project, I attempted to create a recommender system using two models.

#### 1. Collaborative Filtering using Nearest Neighbors
NN is a machine learning algorithm to find clusters of similar users based on common book ratings, and make predictions using the average rating of top nearest neighbors. 

#### 2. Content-Based Filtering using CountVectorizer and TFidfVectorizer
This algorithm recommends products which are similar to the ones that a user has liked in the past. For this model, the recommendations are based on author and genres. 

## Conclusion
Both model seems to give out reasonable recommendations that will help customers
who are looking for their next read. However each models come with their own weaknesses.

#### Content-Based Filtering
To get a better recommendation using content-based filtering, there needs to be data on either book descriptions or written text review. Had these two features exist, we may be able to get a better recommendations.

#### Collaborative Filtering
As collaborative filtering rely on ratings given by the users, the data may be bias as popular books may receive more ratings.
