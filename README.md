# Movie-recommendation-system

**Motivation:**

Recommendation systems are widely used in different big names, such as e-commerce companies like Amazon and Taobao, social media platforms like Youtube and Tiktok. Good recommendation systems are win-win for both customers and the companies, which can not only improve customers' using experience and also increase companies' profits. For example, if one user love the movie recommendations Netflix provided, then the user tend to choose Netflix other than other websites when he or she wants to find a movie. User stickiness will increase and will bring the company more profits. 

In this project, an Alternating Least Squares(ALS) model was trained  based on MovieLens Latest Datasets (Small: 100,000 ratings and 3,600 tag applications applied to 9,000 movies by 600 users. Last updated 9/2018) in colab SPARK to give movie recommendations to users.


**Step1: Data exploratory analysis**
* Find the number of users and movies (rated before or not)
* List movie categories and count the number of movies per category

**Step2: Trained the recommendation model and tune the hyperparameters**
* Check the distribution of avergae rating per user and per movie
* Split the "ratings" dataset into training set (80%) and testign set (20%)
* Set Root Mean Square Error (RMSE) as the metric
* Apply 5-fold corss validation to find the best hyperparameters

**Step3: Give the predicted ratings to movies for each user**
* Check the rmse on testing set using model from step 2

**Step4: Give movie recommendations based on user id and movie id** 
* Give movie recommendations to user 575, 232
* Find similar movies for movie 463, 471 based on l2 distance of itemfactors


**Output and Conclusion:**
* Parameters of the Best Model: Rank=5, MaxIter=10, RegParam=0.1
* Performance of the CVmodel on the training set: RMSE = 0.6397; Performance of the CVmodel on the testing set: RMSE = 0.8799; the model is a little bit overfitting but the performance is acceptable.
