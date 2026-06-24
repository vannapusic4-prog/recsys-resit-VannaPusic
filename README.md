# Recommender Systems resit (Diginetica & Retail Rocket)

This repository contains the individual resit assignment for the Recommender Systems case (System Development for Marketing, Amsterdam University of Applied Sciences). Two recommender system techniques are built from scratch (using only numpy, pandas and scikit-learn, no dedicated recommender libraries) and applied to two e-commerce datasets.

## Techniques

- **Technique A – SVD**, complemented with **SVD++** as a bonus, trained from scratch with stochastic gradient descent (Koren et al., 2009).
- **Technique D – Item-based collaborative filtering (Item-KNN)**, evaluated both as a rating prediction task and as a classification task.

Both techniques are applied to both datasets and evaluated with predictive (RMSE/MAE), classification (precision/recall/F1/AUC-ROC) and ranking (Precision@K/Recall@K/HitRate@K) metrics, with a popularity baseline for comparison.

## Notebooks

The notebooks are organised as one EDA/cleaning notebook and one modelling notebook per dataset. They should be run in order, because each EDA notebook saves a processed interaction file that the matching modelling notebook loads.

1. `Diginetica EDA.ipynb` – Diginetica data cleaning, EDA and feature engineering
2. `Diginetica Models.ipynb` – SVD, SVD++ and Item-KNN on Diginetica
3. `Retailrocket EDA.ipynb` – Retail Rocket data cleaning, EDA and feature engineering
4. `Retailrocket Models.ipynb` – SVD, SVD++ and Item-KNN on Retail Rocket

The processed interaction files (`diginetica_interactions.parquet` and `retailrocket_interactions.parquet`) are included so the modelling notebooks can be run without re-running the full EDA.

## Data

The raw data files are too large to include in this repository. The complete project, including all raw data files, has been uploaded as a zip file directly via Brightspace. To run the notebooks from the raw data, use the files from that zip.

The processed interaction files (`diginetica_interactions.parquet` and `retailrocket_interactions.parquet`) are included in this repository as well, so the modelling notebooks can be run without re-running the full EDA.

## Use of AI Tools

AI tools were used in a supporting role only, not to generate the solution. They were consulted to clarify recommender system concepts, to help with debugging, to explain how certain methods or libraries work when needed, and to help make sure that the interpretations and the steps taken were worded clearly and correctly. 

## References

Bhaumik, D. (2024a). RecSys – Basic Techniques [Lecture slides]. Amsterdam University of Applied Sciences.

Bhaumik, D. (2024b). RecSys – Techniques 2 [Lecture slides]. Amsterdam University of Applied Sciences.

Ji, Y., Sun, A., Zhang, J., & Li, C. (2020). A re-visit of the popularity baseline in recommender systems. In *Proceedings of the 43rd International ACM SIGIR Conference on Research and Development in Information Retrieval* (pp. 1749–1752). https://doi.org/10.1145/3397271.3401233

Koren, Y., Bell, R., & Volinsky, C. (2009). Matrix factorization techniques for recommender systems. *Computer, 42*(8), 30–37. https://doi.org/10.1109/MC.2009.263
