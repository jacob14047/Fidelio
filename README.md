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

## Preliminary instructions and dependencies:

Since this project is somewhat tied to the fidelio website you should first clone that repository,even though by itself the model works just fine, by doing: git clone https://github.com/Lucas5N/fidelio.git to your IDE of choice

1) download python -m venv .venv
2) source .venv/bin/activate
3) pip install fastapi uvicorn pydantic pandas scikit-learn joblib numpy


## Downloading and running:
Since the download and run process is similar for all the models we'll show you how to perform it on the lightest one, the content-based one specifically.

1) go to Models and download contentBased2.pkl
2) download app.py
3) download requirements.txt
4) do: source venv/bin/activate.fish  (Here we're on fish but change this command to make it work for your particular system)
5) do: python -m uvicorn app:app --reload
6) Run the fidelio website (you could've had it running before the installation process, it is not time dependent)
7) Create a profile, add some movies to a list and then go to your profile page and see the recommendations.












