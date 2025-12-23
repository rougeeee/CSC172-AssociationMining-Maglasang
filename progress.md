# CSC172 Association Rule Mining Project Progress Report
**Student:** Preciano B. Maglasang Jr., 2022-2298 

**Date:** 12/23/2025  

**Repository:** [https://github.com/rougeeee/CSC173-AssociationMining-Maglasang](https://github.com/rougeeee/CSC172-AssociationMining-Maglasang) 


## 📊 Current Status
| Milestone | Status | Notes |
|-----------|--------|-------|
| Dataset Preparation	| ✅ Completed	| MovieLens Latest Small downloaded from Kaggle |
| Data Preprocessing	| ✅ Completed	| Ratings filtered, genres split, transactions created |
| Frequent Itemset Mining	| ✅ Completed	| Apriori applied with optimized parameters |
| Association Rule Generation	| ⚠️ Optimized	| Performance improved using higher support & max_len |
Results Interpretation	| ⏳ In Progress	| Analyzing top rules and visualizations |

## 1. Dataset Progress
- Dataset: MovieLens Latest Small (Kaggle)
- Total users (transactions): ~600
- Total ratings: ~100,000
- Genres considered: Action, Adventure, Comedy, Drama, Romance, Sci-Fi, Thriller, Horror, etc.
- Preprocessing applied:
  - Ratings ≥ 3.5 treated as “watched”
  - Genres split into individual items
  - Grouped by userId to form transactions
  - One-hot encoding using TransactionEncoder

**Sample transaction format:**
- User 1 → {Action, Adventure, Sci-Fi}
- User 2 → {Romance, Drama}

## 2. Mining Progress
- Frequent Itemset Mining
- Algorithm: Apriori
- Minimum Support: 0.08 (optimized for speed)
- Maximum Itemset Length: 3

**Result:**
- Frequent genre combinations such as {Action, Adventure}, {Romance, Drama}, and {Comedy, Romance} were successfully identified.

**Association Rule Generation**\
- **Metrics used:**
  - Support
  - Confidence (≥ 0.6)
  - Lift

**Sample Rules (Top Results):**
| Antecedent	| Consequent	| Support	| Confidence	| Lift |
|-------------|-------------|---------|-------------|------|
| Action	| Adventure	| 0.21	| 0.68	| 1.32 |
| Romance	| Drama	| 0.18	| 0.72	| 1.41 |
| Comedy	| Romance	| 0.12	| 0.65	| 1.25 |

## 3. Challenges Encountered & Solutions
| Issue	| Status	| Resolution |
| Slow rule generation	| ✅ Fixed	| Increased min_support and limited max_len |
| Too many candidate rules |	✅ Fixed	| Sorted by lift and kept top 10 rules |
| High computation time	| ⚠️ Improved	| Dataset sampling used during testing |
| Interpretation of results	| ⏳ Ongoing	| Added network graph visualization |

## 4. Next Steps (Before Final Submission)
- {✅}Finalize interpretation of top association rules
- {✅}Generate final network graph and tables
- {✅}Write conclusions and discussion section
- {✅}Clean and finalize README.md
- {✅}Prepare screenshots for notebook and GitHub
