<p align="center">
  <img width="500" src="https://github.com/Mr-Ahmad-Khalil/Sephora_Product_Analysis/blob/main/images/Sephora-Logo.png"/>
</p>
<br />
<br />

# Recommender System for Sephora Products

## Introduction

The dataset is collected from April 2020 Sephora (US) website using web scrapping methods such as BeautifulSoup and Selenium. Link to the dataset can be found [here](https://www.kaggle.com/raghadalharbi/all-products-available-on-sephora-website).

## The Process:

1. Problem Statement
2. Data Exploration
3. Feature Engineering
4. Modelling
5. Conclusion and Future works

-------------------------------------

## 1. Problem Statement: 
With lots of products, it's a hassle to browse through each and every product to find the perfect one that suits you.
To solve this, building a recommendation system based on the user features or favourite products will improve the process.

<img src="https://github.com/ahmdkhalil/Sephora_Recommender_System/blob/main/images/Gif_Compressed.gif" alt="Sephora App" width="200"/>


## 2. Data Exploration:
To better understand the dataset, we looked at the User Features distribution:

![skintone](https://github.com/Mr-Ahmad-Khalil/Sephora_Product_Analysis/blob/main/images/skin_tone.png)
![skintype](https://github.com/Mr-Ahmad-Khalil/Sephora_Product_Analysis/blob/main/images/skin_type.png)
![eyecolor](https://github.com/Mr-Ahmad-Khalil/Sephora_Product_Analysis/blob/main/images/eye_color.png)
![haircolor](https://github.com/Mr-Ahmad-Khalil/Sephora_Product_Analysis/blob/main/images/hair_color.png)
![ratingstars](https://github.com/Mr-Ahmad-Khalil/Sephora_Product_Analysis/blob/main/images/rating_stars.png)

## 3. Feature Engineering:

Two main task required:
1. Tokenize and Lemmatize Ingredient columns
2. Reclassify Ratings Stars columns to a binary value where below 5 is 0

## 4. Modelling:

I experimentd on a couple of different recommenders:
1. Content Based Recommender (User Features)
2. Collaborative Filtering Based on User Id
3. Content Based Recommender (Ingredient)

Evaluation was not possible without human feedbacks but for model 2: Collaborative filtering based on user id was the poorest because to search the product iteself, knowledge of the user id is required which is not possible for other than the individual user.

I chose to deploy the other two models as app_1 and app_2:
1. Content Based Recommender (User Features) as app_1
2. Content Based Recommender (Ingredient) as app_2


[Sephora App 1](https://sephora-app-1.herokuapp.com/) __________________ [Sephora App 2](https://sephora-app-2.herokuapp.com/)                                           
<img src="https://github.com/Mr-Ahmad-Khalil/Sephora_Product_Analysis/blob/main/images/sephora-app-1-400.png" alt="Sephora App 1" width="200" align="left"/>
<img src="https://github.com/Mr-Ahmad-Khalil/Sephora_Product_Analysis/blob/main/images/sephora-app2-400.png" alt="Sephora App 2" width="200"/>

## Conclusion and Future Works:
It's a lot of fun building a recommender app for a product brand. Gathering feedback from other users for evaluation is key. 

1. All three models require different inputs.
2. Collaborative Filtering based on User Id is not recommended because it's hard to find the specific user id.
3. Due to small data some user features only recommend a few products if not any.


In future works: 
1. Gathering feedback of the best recommender system is required.
2. Collect more data to get more accurate results
3. Upgrade input data to identify text image for unlisted products
4. Collaborate iwth business goals.





