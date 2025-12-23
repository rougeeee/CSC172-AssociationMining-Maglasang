
# CSC173 Association Rule Mining Project Proposal
**Student:** Preciano B. Maglasang Jr., 2022-2298  
**Date:** 12/23/2025

## 1. Project Title 
Movie Genre Watching Pattern Analysis Using Association Rule Mining

## 2. Problem Statement
Streaming platforms and movie recommendation systems rely on understanding user preferences. However, discovering patterns in user movie-watching habits can be difficult due to the large number of movies and diverse genres. This project aims to identify associations between movie genres frequently watched together by users. The insights can improve personalized recommendations and help streaming platforms optimize content delivery.

## 3. Objectives
- Discover frequent movie genre combinations using association rule mining.
- Generate association rules with support, confidence, and lift metrics.
- Provide insights for personalized movie recommendations based on user behavior.

## 4. Dataset Plan
- Source: [MovieLens Latest Small Dataset – Kaggle](https://www.kaggle.com/datasets/grouplens/movielens-latest-small), ~100,000 ratings
- Classes: Movie genres including Action, Adventure, Romance, Drama, Sci-Fi, Comedy, Thriller, Horror, etc.
- Acquisition: Download publicly available dataset from Kaggle; preprocess ratings ≥ 3.5 to indicate “watched”.
## 5. Technical Approach
- Architecture Sketch: User-movie transactions → one-hot encoding → frequent itemsets → association rules
- Model: Apriori Algorithm for frequent itemset mining
- Framework: Python (pandas, mlxtend)
- Hardware: Local machine or Google Colab

## 6. Expected Challenges & Mitigations
**Challenge:** Some genres may be too rare, producing few rules
- **Solution:** Adjust minimum support threshold to balance between frequent and meaningful rules

**Challenge:** Large number of users may slow computation
- **Solution:** Use a subset of the dataset (e.g., first 5,000 users) for initial testing

**Challenge:** Interpreting results effectively for recommendations
- **Solution:** Visualize rules using bar plots and network graphs for easier interpretation
