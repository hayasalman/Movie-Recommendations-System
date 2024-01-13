## Movies Recommendations System 

![image-cover-top-air-force-movies@2x](https://github.com/hayasalman/Movie-Recommendations-System/assets/71796909/776bd659-1d82-4f44-ba58-60eb48b94998)

## Overview

Online streaming platforms like Netflix have plenty of movies in their repository and if we can build a Recommendation System to recommend relevant 
movies to users, based on their historical interactions, this would improve customer satisfaction and hence, it will also improve the revenue of the 
platform. The techniques that we will learn here will not only be limited to movies, it can be any item for which you want to build a recommendation 
system.

### Objective

In this project we will be building various recommendation systems:
    
  1. Knowledge/Rank based recommendation system.
    
  2. Similarity-Based Collaborative filtering.
    
  3. Matrix Factorization Based Collaborative Filtering.
  

## Approaches & Methodologies

- Performed a quick overview about the dataset like the dataset shape , data types,..etc.

- Performed exploratory data analysis (EDA).

## Modeling

1. **Rank-Based Recommendation System**
   
     - Rank-based recommendation systems provide recommendations based on the most popular items. This kind of recommendation system is useful when 
       we have cold start problems. Cold start refers to the issue when we get a new user into the system and the machine is not able to recommend 
       movies to the new user, as the user did not have any historical interactions in the dataset. In those cases, we can use rank-based 
       recommendation system to recommend movies to the new user.
       
2. **User based Collaborative Filtering Recommendation System**

    There are different types of Collaborative Filtering:

      - **User-User Similarity Based.**
  
        *We are building similarity-based recommendation systems using cosine/msd similarity and using KNN to find similar users which are the 
         nearest neighbor to the given use.*
        
      - **Item-Item similarity based.**

        *We are building similarity-based recommendation systems using cosine/msd similarity and using KNN to find similar items which are the 
         nearest neighbor to the given use.*
        
      - **Matrix Factorization using Singular Value Decomposition (SVD).**
        
           *Model-based Collaborative Filtering is a personalized recommendation system, the recommendations are based on the past behavior of the 
            user and it is not dependent on any additional information. We use latent features to find recommendations for each user.*

  ## Performance Evaluation & Draw Conclusions

  - **RMSE** : is not the only metric we can use here. We can also examine two fundamental measures, precision and recall. We also add a parameter k 
      which is helpful in understanding problems with multiple rating outputs.

- **Precision@k** : it is the fraction of recommended items that are relevant in top k predictions. Value of k is the number of recommendations to 
    be provided to the user. One can choose a variable number of recommendations to be given to a unique user.

- **Recall@k** : it is the fraction of relevant items that are recommended to the user in top k predictions.

- **Recall** : it is the fraction of actually relevant items that are recommended to the user i.e. if out of 10 relevant movies, 6 are recommended 
    to the user then recall is 0.60. Higher the value of recall better is the model. 

- **Precision** : it is the fraction of recommended items that are relevant actually i.e. if out of 10 recommended items, 6 are found relevant by 
    the user then precision is 0.60. The higher the value of precision better is the model.

  ### **Final conclusions**

  - The final model will denpend on the business requirements as whether they have to minimize RMSE or go with maximizing Precision/Recall.
    
  - Tuned SVD has better RMSE than all models but Collaborative Filtering using user-user based interaction is also giving good results based on 
    Precsion and recall @k for K=10.

    *Matrix Factorization has lower RMSE due to the reason that it assumes that both items and users are present in some low dimensional space 
     describing their properties and recommend a item based on its proximity to the user in the latent space. Implying it accounts for latent 
     factors as well.*

 ## Business Insights

 - As per the number of unique users **671** and movies **9066**, there is a possibility of 671* 9066 = 6,083,286 ratings in the dataset. But we 
   only have 100,004 ratings , i.e. not every user has rated every movie in the dataset.

- In some cases, a lot of interactions isn't always a good sign in which maybe there are movies with very high interactions, but these interactions 
  are of the ratings 1 and 2 rather than 4 or 5 which simply means that this movie is disliked by the majority of users..

- Based on the data distribution of the number of interactions by users we observed that it's more skewed toward the right which means only a few 
  users interacted with more than 500 movies.
  
 ## References

 [Movies Recommendation System IPYNB File](https://github.com/hayasalman/Movie-Recommendations-System/blob/main/Movie_Recommendation_System%20_.ipynb)
