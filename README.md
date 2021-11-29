# Recommendation System: Amazon Product Reviews

## Context

Online E-commerce websites like Amazon, Flipkart uses different recommendation models to provide personalized suggestions to different users. Amazon currently uses item-to-item collaborative filtering, which scales to massive data sets and produces high-quality recommendations in real-time. In this project, we built a recommendation system to recommend products to customers based on their previous ratings for other products. 


## Technologies Used: 

* Numpy 
* Pandas
* matplotlib
* seaborn
* sklearn metrics

## The Data

The Amazon dataset contains the following attributes: 
* **userId:** Every user identified with a unique id
* **productId**: Every product identified with a unique id
* **Rating**: Rating of the corresponding product by the corresponding user
* **timestamp**: Time of the rating

## Exploratory Data Analysis

In this section, we checked several characteristics of the data such as the data types, summary statistics, and distributions. For example, the distribution of the ratings is displayed below: 

![Screen Shot 2021-11-29 at 5 17 40 PM](https://user-images.githubusercontent.com/88220704/143957871-448778f3-4ed0-4144-af29-ab048a4892ec.png)

## Data Preparation

We then took a subset of the dataset by only keeping users who have given 50 or more datings in order to make the dataset less sparse and easy to work with. After creating an interaction matrix of products and users based on ratings we saw that the data is still highly sparse since the current number of ratings is just 0.17% of the possible number of ratings. 

After exploring and preprocessing the data, it is time to build the recommendation systems. In this project, we decided to make three different types of recommendation models. 

1. **Rank based Recommendation System**
2. **Collaborative Filtering based Recommendation System**
3. **Model based Collaborative filtering: Singular Value Decomposition**

## Rank based Recommendation System

In this section, we designed a function that gets the top products based on highest average rating and minimum number interactions. This system is a based on popularity, and does not take into account individual preferences. Using this function, we then tested it by recommending products to users 

