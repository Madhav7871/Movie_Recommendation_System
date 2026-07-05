# 🎬 Movie Recommendation System

A content-based movie recommendation engine built in Python using `pandas` and `scikit-learn`. This system suggests movies by analyzing genre similarities and ranking the results by audience ratings. 🌟

## 🚀 Project Overview
The core of this project is to go beyond simple rating-based recommendations. By leveraging **Cosine Similarity** on movie genres, the system identifies movies that "feel" similar to the user's choice and then refines the list to show only the highest-rated titles. 🧠✨

## ✨ Features
*   **🔍 Content-Based Filtering**: Uses `TfidfVectorizer` to analyze the genre metadata of over 16,000 movies.
*   **📊 Dual-Stage Ranking**: First, it finds the top 50 most similar movies by genre, then sorts them by `average_rating` to ensure quality.
*   **💻 Interactive Interface**: Designed to run seamlessly in Google Colab with clean, formatted HTML table outputs.

## 🛠️ Tech Stack
*   **Language**: Python 🐍
*   **Data Analysis**: `pandas` 🐼
*   **Machine Learning**: `scikit-learn` (`TfidfVectorizer`, `cosine_similarity`)
*   **Environment**: Google Colab / Jupyter Notebook ☁️

## ⚙️ How It Works
1.  **Data Preprocessing**: Handles missing values in the `genres` column and prepares the dataset. 🧹
2.  **Vectorization**: Converts text-based genres into a numerical matrix. 🔢
3.  **Similarity Calculation**: Computes the cosine similarity between movies to understand their relationship. 📐
4.  **Recommendation Logic**:
    *   Finds movies with the highest genre correlation. 🤝
    *   Filters out the most relevant candidates. 🎯
    *   Ranks the final list by `average_rating` and `num_votes`. ⭐

## 📝 Usage
Simply run the code in a Jupyter or Colab notebook. When prompted:
1.  Enter the title of a movie you enjoy. 🎞️
2.  The system will output a clean table of 10 similar movies, including their genres and ratings. ✅

## 💡 Example
```python
# The system takes your input and generates a clean recommendation table
movie_name = input("Enter a movie name: ")
recommendations = recommend(movie_name)
display(recommendations)
