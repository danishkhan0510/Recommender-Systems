# Recommender-Systems
Deep Dive into various recommender systems  
### Project 1
This is a  simple content based movie recommender system using user ratings.  
The key components of this recommender system are-  
Ratings given by the user to the movies he has watched  
Genres of the movies  
We first create a sparse matrix of the movie genres filled with 1's and 0's for the entire movies dataframe. The value is 1 if the movie has a particular genre and 0 for the other genres. We do the same thing for the dataframe containing the movies and ratings of the new user. We multiply the ratings he has given to a movie with the genres of the movie. As a result we get scores for each genre and high scores indicate that the user prefers to watch movies of that kind(of those genres). We then multiply these scores with the genres of all movies in the entire movie dataframe and take a weighted average. If we sort this in descending order we get the movies to recommend on the top.  

### Project 2
This is a content based movie recommendation system using the description of movies.  
In this we take only five essential features i.e. title, actors, genre, writers, directors from the dataset rest are ignored. Using those five essential features we calculate similarity between movies using TF-IDF vectorizer and cosine similarity. So, All related movies which is having more cosine similarity score with the given movies are printed in descending order.  

You can see that we are using the features(like genre) of the movies in content based filtering. There are many advantages and disadvantages of content based filtering.  
**Advantages**  
The model doesn't need any data about other users, since the recommendations are specific to this user. This makes it easier to scale to a large number of users.  
The model can capture the specific interests of a user, and can recommend niche items that very few other users are interested in.  
**Disadvantages**  
Since the feature representation of the items are hand-engineered to some extent, this technique requires a lot of domain knowledge. Therefore, the model can only be as good as the hand-engineered features.  
The model can only make recommendations based on existing interests of the user. In other words, the model has limited ability to expand on the users' existing interests.
