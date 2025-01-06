# Collaborative-Filtering-Based-Recommender-System
I start by merging datasets, especially the movie ratings dataset, to create a structured DataFrame with movies and ratings for each user.Then
I calculate the mean rating for each movie to understand the general user sentiment towards each movie. This helps me know which movies are liked the most by users.
3. Counting Number of Ratings
I calculate how many users have rated each movie. Movies with more ratings can be considered more reliable when recommending.
4. Exploratory Data Analysis (EDA)
Using visualizations (e.g., histograms), I analyze the distribution of ratings and the number of ratings per movie to get insights into how frequently users rate movies and how their ratings are spread.
5. Creating a Pivot Table (User-Movie Matrix)
I create a pivot table with user_id as rows, movie_title as columns, and rating as the values. This matrix helps in analyzing which movies users have rated and enables similarity calculations.
6. Calculating Correlation (Similarity) Between Movies
Using the corrwith() function, I calculate the correlation between a movie's ratings and all other movies. This measures how similar the ratings patterns are.
Higher correlation values (closer to 1) indicate that two movies are similar in how users rate them.
7. Joining Rating Count Data
I add the number of ratings for each movie to the correlation results, as more ratings usually indicate a more reliable similarity score.
8. Filtering by Minimum Number of Ratings
To improve the quality of recommendations, I filter out movies with fewer than 100 ratings. This ensures that the similarity calculation is based on movies with enough user feedback to be reliable.
9. Displaying the Most Similar Movies
After filtering, I display the movies most similar to a given movie (e.g., "Star Wars" or "Liar Liar") based on their correlation scores.
10. Final Output
The system recommends movies that have similar ratings to the movie I am interested in, filtered by movies with a significant number of ratings.
