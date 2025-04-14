
Movie Recommendation System

Welcome to my Movie Recommendation System project! This notebook implements multiple techniques to recommend movies to users based on their preferences and viewing patterns. It is built using the popular MovieLens 100K dataset, which contains ratings from real users on a wide variety of films.

Project Structure

This repository contains the following key files:

- Movie_Recommendation.ipynb — The main Jupyter Notebook with all code, explanations, and results.
- users.csv — Cleaned user data extracted from the original dataset.
- movies.csv — Cleaned movie metadata.
- ratings.csv — Cleaned user-movie rating data.
- Pixie_Algorithm_Explanation.md — Detailed explanation of the graph-based Pixie-inspired recommendation algorithm.
- Recommendation_Report.md — Full project report with methodology, results, and conclusions.

Features

The system implements three types of recommendation techniques:

1. User-Based Collaborative Filtering
   Recommends movies to a user by finding others with similar preferences and averaging their ratings.

2. Item-Based Collaborative Filtering
   Finds similar movies to a given movie by comparing how users rated them.

3. Graph-Based Recommendation (Pixie-Inspired)
   Uses random walks over a user-movie bipartite graph to simulate how users might discover new movies based on their past interests.

Dataset Overview

- Users: 943
- Movies: 1,682
- Ratings: 100,000
- The dataset was preprocessed to remove duplicates and handle missing values.

Results

Each model returns a ranked list of movie recommendations. The graph-based method, particularly the Pixie-style walk with smart restart logic, often surfaces more diverse or surprising titles based on movie-watching relationships.

How to Use

1. Clone this repo or download it as a ZIP.
2. Open Movie_Recommendation.ipynb in Jupyter Notebook.
3. Run all cells from top to bottom.
4. Try calling:

   weighted_pixie_recommend(1, walk_length=50, num=5)
   weighted_pixie_recommend("Jurassic Park (1993)", walk_length=50, num=5)

   to test the random walk recommender.

Future Improvements

- Combine user and item-based strategies into a hybrid model.
- Use genre or metadata to refine recommendations.
- Explore deep learning or graph neural networks for smarter personalization.

License

This project is for educational purposes. All data is sourced from the MovieLens 100K Dataset.
