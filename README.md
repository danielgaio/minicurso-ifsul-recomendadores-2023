# minicurso-ifsul-recomendadores-2023
 Minicurso apresentado no IFSUL de Bagé no dia 05/12/2023, com tema "Introdução aos sistemas de recomendação". O minicurso é composto por uma apresentação conceitual de slides, 2 notebooks de overview do python e pandas e notebook de criação de sistema de recomendação de filmes.

# Instalar dependências

```pipenv install```

# ML use cases in banking
* Fraud detection
* Managing and understanding customer data
* Risk modeling for investment banks
* Personalized marketing (recommendation engine)
* Predictive analytics (forecast indicators)
* Costumer segmentation (clustering)
* Costumer support and service (chatbots)
* Credit decisioning and underwriting
* Recommender Systems for Personalized Financial Advice:
    * https://www.youtube.com/watch?v=H8rWjyZpkGo
    * Not a very good idea to recommend for a client to buy an asset just because the client probably likes the asset. That doesn't mean that the client will earn money with the asset.

# Notes on Tensorflow stack for Recommendation
On the Tensorflow stack we can use the ScaNN library to do the similarity search. ScaNN is a library for Approximate Nearest Neighbor (ANN) search. It is designed for high-dimensional vector similarity search and it is optimized for maximum throughput and minimum latency. It is also designed to be easy to use, with a simple API that is similar to that of TensorFlow's other machine learning libraries.

On top of ScaNN we can use the TFRS library to build a recommendation system. TFRS is a TensorFlow library for building recommender system models. It helps with the full workflow of building a recommender system: data preparation, model formulation, training, evaluation, and deployment.

And we can use the tensorflow learning to rank techniques in addition to Scann and TFRS.

On the youtube tensorflow tutorial the basic steps presented so far are:
* (Retrieval fase): Create a model that given a user, returns a list of movies that, based on other users, the user might like.
* (Ranking fase): A model that predicts the rating that the user would give to each one of the movies in the list. Then rank the movies by the predicted rating.
* Leverage context features to improve the model and recommendations.

**Scann** is just a library for approximate nearest neighbor search. It is not a recommendation system library. It is just a library that can be used to build a recommendation system.

TF ranking (learning to rank) can be used to rank answers to a question. It can be used to rank movies for a user. It can be used to rank products for a user. It can be used to rank ads for a user.

## Collaborative filtering
Collaborative filtering is a type of recommendation system that uses the ratings of the users to recommend items that are similar to the ones that the user liked in the past.

This approach provides serendipitous recommendations. It can recommend items that the user would never think of.

### Item - Item collaborative filtering
This is a type of collaborative filtering that uses the similarity between items in order to recommend items.
The similarity between items is calculated based on the similarity of their ratings by users.

In practice tends to be better then user-user collaborative filtering. Items are simpler than users. Items are more clearly classifiable than users.

### User - User collaborative filtering
This is a type of collaborative filtering that uses the similarity between users in order to recommend items.
The similarity between users is calculated based on the similarity of their ratings for items.

## Content based filtering
Content based filtering is a type of recommendation system that uses the features of the items to recommend items that are similar to the ones that the user liked in the past.

# The data
* https://www.kaggle.com/competitions/santander-product-recommendation/data

# Youtube tutorial that does a recomendation sistem with cosine similarity
Is a simple procedure that can be used as a last resort for the minicourse

https://www.youtube.com/watch?v=ijtxuF_5kEU