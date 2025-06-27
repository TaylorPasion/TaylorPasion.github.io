---
layout: default
title: "Week 4"
permalink: /week4/
---

# Week 4: Netflix Ratings Analysis

---

## Day 1

### Overview

This week, we explored patterns in Netflix’s rating data using visualizations and began building a recommender system using a neural network. Below are the highlights and insights from Day 1.

---

### 📊 Distribution of Titles by Content Rating

This chart shows the number of titles available on Netflix by their content rating (e.g., PG, PG-13, R). It highlights that **Rated R** titles dominate the platform, while **TV-Y** titles (intended for very young audiences) are relatively rare.

<p align="center">
  <img src="/assets/img/number_of_titles_vs_rating.png" alt="Distribution of Ratings in Netflix Shared Dataset by Rating" width="1000" style="border-radius: 12px; box-shadow: 0 4px 12px rgba(0,0,0,0.15);" />
</p>

---

### 📺 Movies vs TV Shows by Rating

This visualization compares the count of movies and TV shows on Netflix. We found that **movies significantly outnumber TV shows**.

<p align="center">
  <img src="/assets/img/distribution_of_ratings.png" alt="Distribution of Ratings in Netflix Shared Dataset by Type" width="1000" style="border-radius: 12px; box-shadow: 0 4px 12px rgba(0,0,0,0.15);" />
</p>

---

### ⭐ Average Ratings of Netflix Titles

This chart illustrates the **average user ratings** across different Netflix titles. It helps reveal which titles resonated most with viewers.

<p align="center">
  <img src="/assets/img/average_netflix_rating.png" alt="Average Netflix Rating per Title" width="1000" style="border-radius: 12px; box-shadow: 0 4px 12px rgba(0,0,0,0.15);" />
</p>

---

## Day 2

### 🏆 Top 50 Highest Rated Movies

The graph below shows the **top 50 highest-rated movies** on Netflix. _Miss Congeniality_ tops the list with over 200,000 total user rating points. The 50th-ranked film, _Bringing Down the House_, still received an impressive ~120,000 total points. Each title's score reflects the total sum of user ratings.

<p align="center">
  <img src="/assets/img/top_50_movies.png" alt="Top 50 Rated Netflix Movies" width="1000" style="border-radius: 12px; box-shadow: 0 4px 12px rgba(0,0,0,0.15);" />
</p>

---

### 🧠 Building a Neural Network Recommender System

We created a neural network that predicts whether a user would enjoy a movie based on two inputs:

- **User ID** (Input A)
- **Movie ID** (Input B)

The model learns from how each user rated previous movies and how each movie was rated by others. Based on that, it generates a prediction for how a user would rate a new movie.

<p align="center">
  <img src="https://github.com/user-attachments/assets/843cf9b0-4bdd-4916-96d5-43579077f17d" alt="Neural Network Diagram" width="600" style="border-radius: 12px; box-shadow: 0 4px 12px rgba(0,0,0,0.15);" />
</p>

---

### 🧮 Model Architecture Summary

<p align="center">
  <img src="/assets/img/model_summary.png" 
       alt="Model Architecture Summary" 
       width="1000" 
       style="border-radius: 12px; box-shadow: 0 6px 16px rgba(0,0,0,0.2); margin: 20px 0;" />
</p>

This visual summarizes the architecture of our neural network recommender system. The model takes in two inputs—**user ID** and **movie ID**—and passes them through embedding layers. These embeddings are compared using a dot product and concatenated before passing through multiple dense layers. The final output is a **predicted rating score**, representing how much the model thinks the user would enjoy the movie.
