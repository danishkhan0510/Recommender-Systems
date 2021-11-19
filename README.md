# Recommender-Systems
Deep Dive into various recommender systems  
### Project 1
I have created a simple content based movie recommender systems.  
The key components of this recommender system are-  
Ratings given by the user to the movies he has watched  
Genres of the movies  
We first create a sparse matrix of the movie genres filled with 1's and 0's for the entire movies dataframe. The value is 1 if the movie has a particular genre and 0 for the other genres. We do the same thing for the dataframe containing the movies and ratings of the new user. We multiply the ratings he has given to a movie with the genres of the movie. As a result we get scores for each genre and high scores indicate that the user prefers to watch movies of that kind(of those genres). We then multiply these scores with the genres of all movies in the entire movie dataframe and take a weighted average. If we sort this in descending order we get the movies to recommend on the top.
