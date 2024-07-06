Source Jupiter file to refer for all executions and graphs:
[rotten_tomatoes.ipynb](https://github.com/vikrammuduvadi/RottenTomatoes/blob/main/rotten_tomatoes.ipynb)

*********************Summary of findings********************
Objective was to predict the tomatometer ratings of Rotten Tomatoes website
Eventually the goal could be to predict the box office outcome of movies

https://www.kaggle.com/datasets/stefanoleone992/rotten-tomatoes-movies-and-critic-reviews-dataset?select=rotten_tomatoes_movies.csv

1. Data trimming happened to eliminate all duplicate, null, nan values 
2. Ordinal Encoding and One hot encoding were applied to non numerical values
3. With detailed data analysis, we concluded to use these input features would 
work best
     0   content_rating      8077 non-null   object 
     1   runtime             8077 non-null   float64
     2   tomatometer_rating  8077 non-null   float64
     3   audience_status     8077 non-null   int64  
     4   audience_rating     8077 non-null   float64
4. The data set was divided into training and testing data set (75/25)
5. KNN and Decision Tree models were used to train and test the data
6. Decision tree performed better with 85% accuracy rate, however KNN 
   struggled at around 55% accuracy rate
7. We then decided to remove audience count metric and re-run the modeling
At this point both models (KNN, Decision Tree) performed well with around 86% accuracy
8. Hyper tuning of the parameters happened for Decision tree and it was found that 
with max tree depth of 5, the accuracy of the Decision tree model hit around 90%
