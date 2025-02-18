# task-2
NAME:S.Jerlin Christina
DOMAIN:Artifical Intellengence
DURATION:January to February
COMPANY:Codsoft
1. Objective
The goal of a recommendation system is to suggest relevant items (like movies, books, or products) to users based on their preferences. In this case, we built a movie recommendation system using collaborative filtering.

2. Collaborative Filtering
Collaborative filtering is one of the most popular techniques for building recommendation systems. It works by recommending items based on the preferences of similar users. There are two types:

User-based Collaborative Filtering: Recommend items based on users who are similar to the target user.
Item-based Collaborative Filtering: Recommend items that are similar to the ones the user has liked or rated highly.
In our case, we used User-based Collaborative Filtering, where we recommend movies that users with similar tastes have rated highly.

3. Steps in Building the System
1. Data Representation
The data is represented in the form of a user-item rating matrix. Each row represents a user, each column represents a movie, and the values represent the rating a user has given to a movie.
Missing values (when a user hasn't rated a movie) are represented as NaN.
2. User Similarity Calculation
To identify which users are similar, we calculate the cosine similarity between users. This measures how closely the rating patterns of two users match.
Cosine similarity is a value between -1 and 1. A value closer to 1 means the users have very similar ratings, while values closer to -1 indicate opposite preferences.
We used scikit-learn's cosine_similarity function to compute this similarity matrix.
3. Making Recommendations
Once we have the similarity scores between users, we identify the most similar users to the target user.
We then recommend movies that these similar users have rated highly, but the target user hasn't yet rated.
We apply a rating threshold (e.g., recommend movies that users have rated 3 or higher).
4. Output
The output is a list of movie recommendations that the system suggests to the target user based on the preferences of similar users.
