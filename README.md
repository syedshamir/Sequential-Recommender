# Sequential-Recommender
Sequential Recommendation understands the sequential user behaviors, the interactions between users and items, and preferences and item popularity over time.

Suggest items which may be of interest to a user by mainly modelling the sequential dependencies over the user-item interactions.

Sequential Recommendation understands the sequential user behaviors, the interactions between users and items, and the evolution of users’ preferences and item popularity over time.

It takes individual 3 users and recommend movies to them based on their most similar peers users. Most similar users can be found by using Pearson Similarity. 
Based on the rating and movies watched by most similiar peers, scores are then calculated for the movies based on rating and similarity score. Top 20 movies are then recommended to each 3 users. These 3 are now considered as a group,
so for group recommendation, here 2 approches are udertaken
1) LEAST MISERY APPROACH
2) Averge Aggregate Approach

For the least misery, the user with the lowest score of the recommeded movies will be preferred in group recommendation.
For theAvg Aggregate approach, group recommendation is based on average of 3 users score/ratings to their individual recommended movies.


Group based recommendation is used as a starting point for sequential recommendation.

Each Current iteration takes previous iteration Individual and group recommendation.

In each iteration, previous recommended individual user movies are not considered. 

Alpha is calculated by taking difference of avg. Kendel Tau distance between users recom. and avg. Kendel Tau distance b/w user and group recom. i.e by taking disagreements in considereation

alpha =  ( KTavg_grp - KTavg_user )
Alpha will be use now to get score for group recommendation movies scores.


With in each iteration, group and user satisfaction is calculated
