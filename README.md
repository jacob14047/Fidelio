# Fidelio, pipeline hybrid movie recommender system

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange)
![Pandas](https://img.shields.io/badge/Data-Pandas-150458)
<div align="center"><img src="logo.png" alt="Fidelio Logo" height = 200px width = 200px></div>

A **pipeline movie recommendation system** developed as part of the Machine Learning (ML) course.

## Pipeline Architecture

This project implements an hybrid methodology to solve the cold-start problem and improve recommendation accuracy:

### 🔹 Pipeline: The Gradient Boosted Hybrid
A feature-based machine learning approach that treats recommendation as a regression/ranking problem:
1.  **Content Encoding:** Metadata is encoded into numerical features.
2.  **Collaborative Features:** User and Item embeddings/vectors are used as input features.
3.  **Gradient Boosting Machine (GBM):** A Tree-based model (Hist Gradient Boosting) is trained on these combined features to predict the specific user rating.

## Data Sources & Acknowledgments

This project utilizes a custom dataset constructed by merging user ratings with rich movie metadata collected from multiple sources:

* **MovieLens Dataset**  
  User–item ratings are derived from the MovieLens datasets provided by GroupLens Research.  
  These ratings form the backbone of the collaborative filtering pipeline.  
  * https://grouplens.org/datasets/movielens/

* **The Movie Database (TMDB) API**  
  Rich movie metadata (TMDB IDs, cast, crew, directors, genres) was collected programmatically via the TMDB API and used primarily for content-based modeling.  
  * https://developers.themoviedb.org/3

* **Rotten Tomatoes Reviews Dataset**  
  A large-scale dataset of critic and audience reviews scraped from Rotten Tomatoes, used to enrich item representations and provide additional signals for cold-start movies and sentiment-aware modeling.  
  * https://www.kaggle.com/datasets/priyamchoksi/rotten-tomato-movie-reviews-1-44m-rows


## Trained Model

Due to GitHub file size limitations, the trained models and datasets are not included in this repository.

You can download the trained models and datasets from Hugging Face:
https://huggingface.co/jacob14047/Fidelio/












