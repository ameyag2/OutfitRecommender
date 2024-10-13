# OutfitRecommender
Outfit Recommender is built using various recommandation algorithms such as popularity based ,content based and collaborative filtering.

Popularity Based Recommender System works on the principle of popularity and or anything which is in trend. It recommends products based on Total Number of Ratings on products and average product rating given by users and fetch popular amongst them.

Content Based Recommender System works on the principle of similar content. It recommends products based on similar content of the product.The model recommands similar products to the user based on cosine similarity.

The whole Dataset Has been taken from kaggle. This dataset holds 15K records. It is a product listing from Myntra.com for the period of June 2019 to August 2019.

Dataset Link: https://www.kaggle.com/datasets/promptcloud/all-products-from-myntracom-2019

Link to youtube demo:

Goals of the project
The main goal of this project is to provide a personalized fashion recommendation system that can help users find fashion products that match their preferences. The system also aims to provide an interactive user interface that is easy to use and navigate.
Process
The first step in developing this project was to collect and prepare the dataset of 17000 Myntra products. Next, different machine learning algorithms such as popularity-based, collaborative filtering, hybrid, and ResNet-based feature extraction were trained using this dataset. Then, these algorithms and features were integrated into the Flask backend.

For the front-end, Reactjs and Bootstrap were used to create an interactive user interface. Firebase authentication was also integrated into the system to ensure secure user authentication.
Features
1. Image-based fashion recommendation: 
Users can upload images of fashion products they like, and the system will recommend similar products based on the ResNet-based feature extraction.

2. Different recommendation algorithms: 
The system uses different recommendation algorithms such as popularity-based, collaborative filtering, and hybrid to provide a variety of recommendations to users.

3. Personalized recommendations: 
The system provides personalized recommendations to users based on their preferences and past interactions with the website.

4. Secure authentication: 
Firebase authentication is used to ensure that only authorized users can access the website.

5. Interactive user interface: 
The system has an interactive user interface created using Reactjs and Bootstrap, making it easy for users to navigate and use the website.
Resources
The Dataset used in this project is taken from kaggle. It is a product listing from Myntra.com for the period of June 2019 to August 2019. This dataset holds 15K records.

Dataset Link: https://www.kaggle.com/datasets/promptcloud/all-products-from-myntracom-2019

Tech Stack
Client: React, Materil-UI, react-bootstrap

Server: Python, Flask

Database: Firebase

API Reference
Get 100 best selling Products- Popularity based recommendation

  GET /api/bestsellers

Get BestSelling products for men- Popularity based recommendation

  GET /menProducts

Get BestSelling products for women- Popularity based recommendation

  GET /womenProducts

Get all products data

  GET /allProducts

Get Similar Items - Content Based Recommandation
  
GET /prod/${title}

Parameter	Type	Description
title	string	Title of the product from which fetch all similar products

Get Recommandation of products based on ratings- Collaborative Filtering

  GET /recommand/${title}

Get Recommandation of products based on ratings- Collaborative Filtering

  GET /recommand/${title}

Parameter	Type	Description
title	string	Title of the product from which fetch related products which user should buy based on ratings
get the similar products available on website based on image- Fashion recommandation using Resnet model
  
GET /imageData

Send uploaded image data to backend for image preprocessing, feature extraction and recommandation
  
POST /imageData

