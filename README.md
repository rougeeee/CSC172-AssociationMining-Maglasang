# Movie Genre Watching Pattern Analysis using Association Rule Mining
**CSC172 Data Mining and Analysis Final Project**  
*Mindanao State University - Iligan Institute of Technology*  
**Student:** Preciano B. Maglasang Jr., 2022-2298 
**Semester:**  AY 2025-2026 Sem 1  
[![Python](https://img.shields.io/badge/Python-3.8+-blue)](https://python.org) [![PyTorch](https://img.shields.io/badge/PyTorch-2.0-orange)](https://pytorch.org)

## Abstract
This project analyzes movie-watching patterns to discover relationships between genres frequently watched together. Using the MovieLens Latest Small dataset from Kaggle (~100,000 ratings), the project applies the Apriori algorithm to extract frequent genre combinations and generate association rules with metrics such as support, confidence, and lift. The results can inform personalized movie recommendations and provide insights into user preferences. Top rules indicate strong associations between genres like Action–Adventure and Romance–Drama, demonstrating practical applications for streaming platforms. The contributions include a full preprocessing pipeline, rule generation, and visualizations of the top associations.

## Table of Contents
- [Introduction](#introduction)
- [Related Work](#related-work)
- [Methodology](#methodology)
- [Experiments & Results](#experiments--results)
- [Discussion](#discussion)
- [Ethical Considerations](#ethical-considerations)
- [Conclusion](#conclusion)
- [Installation](#installation)
- [References](#references)

## Introduction
### Problem Statement
Streaming platforms struggle to understand user preferences across the vast range of movies. Identifying which genres are frequently watched together can enhance recommendation systems and improve user experience. This project analyzes user ratings to uncover genre associations using association rule mining techniques, providing actionable insights for content curation and personalized recommendations.

### Objectives
- Identify frequent genre combinations using the Apriori algorithm.
- Generate association rules with support, confidence, and lift.
- Visualize the top rules for interpretation and insights.

## Related Work
- MovieLens dataset frequently used for collaborative filtering and recommendation studies.
- Association Rule Mining applied in e-commerce and content recommendation.
Gap: Few studies explore direct genre association patterns for small streaming datasets, making this project locally relevant.

## Methodology
### Dataset
- **Source:** [MovieLens Latest Small – Kaggle](https://www.kaggle.com/datasets/grouplens/movielens-latest-small)
 (~100k ratings)
- **Features:** userId, movieId, rating, genres
- **Preprocessing:** Ratings ≥3.5 considered “watched,” genres split into lists, grouped by user for transactions.

### Architecture
#### Association Rule Mining Pipeline
- Convert user-genre transactions into one-hot encoded format.
- Apply Apriori algorithm with minimum support of 0.05.
- Generate association rules with minimum confidence of 0.6.
- Sort rules by lift and visualize top associations using a network graph.


## Experiments & Results
Top Rules (Example)
| Antecedent	| Consequent	| Support	| Confidence	| Lift |
|-------------|-------------|---------|-------------|------|
| IMAX, Film-Noir	| Documentary	| 0.17	| 0.66	| 2.12 |
| Film-Noir, Children	| Documentary	| 0.18	| 0.64	| 2.05 |
| Documentary, Musical	| Film-Noir	| 0.17	| 0.7	| 2.05 |

<img width="1270" height="768" alt="image" src="https://github.com/user-attachments/assets/6ae46d69-0954-43fe-943b-94ceab42384f" />

### Demo
Video: [CSC172_Maglasang_Final.mp4](https://drive.google.com/drive/folders/1UkbXyJSbzTVtFKcuMpukK938qX7PQwH6?usp=sharing)

## Discussion
- **Strengths:** Reveals strong genre pairings, easy to interpret, applicable for recommendation.
- **Limitations:** Rare genres may produce few rules; dataset may not represent all users.
- **Insights:** Rules confirm intuitive pairings (Action–Adventure, Romance–Drama), and network visualization helps identify influential genres.
  
## Ethical Considerations
- **Bias:** Dataset skews toward popular movies; niche genres underrepresented.
- **Privacy:** No personally identifiable information is exposed.
- **Misuse:** Results are for recommendation purposes only, not predictive of user behavior beyond dataset.

## Conclusion
This project successfully extracts genre association rules using ARM from the MovieLens dataset, providing interpretable patterns for movie recommendation systems. Future work includes applying the method to larger datasets, integrating with collaborative filtering, and testing personalized recommendation performance.

## Installation
1. Clone repo: `git clone https://github.com/rougeeee/CSC173-AssociationMining-MovieGenre`
2. Install deps: `pip install -r requirements.txt`
3. Download MovieLens dataset from Kaggle and place CSV files in data/.
   - **requirements.txt**
     - pandas
     - mlxtend
     - networkx
     - matplotlib

## References
[1] Grouplens. "MovieLens Latest Small Dataset," Kaggle, 2023.
[2] Agrawal, R., Srikant, R. "Fast algorithms for mining association rules," VLDB, 1994.
[3] Raschka, S. "mlxtend: Machine Learning Extensions," 2021.

## GitHub Pages
View this project site: [[https://github.com/rougeeee/CSC172-AssociationMining-Maglasang/](https://github.com/rougeeee/CSC172-AssociationMining-Maglasang)]
