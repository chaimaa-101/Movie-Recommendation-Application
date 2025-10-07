# 🎬 Movie Recommendation System 

## Project Overview
This application is designed to personalize the cinematic experience for users. It leverages machine learning, content-based filtering, and sentiment analysis to suggest movies tailored to individual preferences. By integrating diverse datasets and APIs, the project delivers accurate, data-driven recommendations while providing users with an intuitive and interactive interface.


## Project Objectives
The project aims to:
* Provide personalized movie recommendations based on user interests.
* Improve user engagement and satisfaction through intelligent suggestions.
* Implement and compare Content-Based Filtering and Collaborative Filtering models.
* Visualize movie data insights using Python.
* Build an interactive application with a user-friendly interface.
 

## Sources of the Datasets
1. [IMDB 5000 Movie Dataset](https://www.kaggle.com/datasets/carolzhangdc/imdb-5000-movie-dataset)  
2. [The Movies Dataset](https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset)  
3. [TMDB Movie Metadata](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata/data?select=tmdb_5000_movies.csv)  
4. [List of American Films of 2018](https://en.wikipedia.org/wiki/List_of_American_films_of_2018)  
5. [List of American Films of 2019](https://en.wikipedia.org/wiki/List_of_American_films_of_2019)  
6. [List of American Films of 2020](https://en.wikipedia.org/wiki/List_of_American_films_of_2020)  
7. [List of American Films of 2021](https://en.wikipedia.org/wiki/List_of_American_films_of_2021)  
8. [List of American Films of 2022](https://en.wikipedia.org/wiki/List_of_American_films_of_2022)  
9. [List of American Films of 2023](https://en.wikipedia.org/wiki/List_of_American_films_of_2023)  
10. [List of American Films of 2024](https://en.wikipedia.org/wiki/List_of_American_films_of_2024)


# Project Architecture

## 1. Data Preparation
* **Datasets used:**
    * movie_metadata.csv, credits.csv, movies_metadata.csv from Kaggle.

    * Additional movie data (2016–2024) collected from Wikipedia via Web Scraping.

    * API enrichment from TMDb (The Movie Database) to retrieve missing information (genre, actors, directors).

* **Preprocessing steps:**
    * Data cleaning and normalization.
    * Feature extraction (genres, runtime, ratings, votes).
    * Integration and merging of multiple datasets for consistency.

## 2. Data Visualization
Comprehensive visualizations were performed to understand the dataset and extract insights, including:
* Top 10 directors, genres, and actors.
* Movie rating distributions.
* Average ratings by year.
* Evolution of movie production over time.
These analyses guided the selection of relevant features for model building.

## 3. Machine Learning Models
* **Content-Based Filtering**
    This approach recommends movies similar to those the user already liked by analyzing movie attributes such as genre, cast, and keywords.

    * **Technique used:** TF-IDF Vectorization and Cosine Similarity.
    * **Output:** A ranked list of the top 10 similar movies.

* **Collaborative Filtering (Comparative Model)**
    Recommendations are generated based on the preferences of users with similar tastes.
    * Implemented with a user–item matrix.
    * Similarity computed using Cosine and Jaccard measures.
    * Compared with the content-based model; however, due to missing user IDs and limited data, the collaborative model showed lower performance.

## 4. Sentiment Analysis
Sentiment analysis was integrated to analyze user reviews and improve recommendation accuracy.
* **Tool:** NLTK (Natural Language Toolkit).
* **Method:** TF-IDF + Multinomial Naïve Bayes Classifier.
* **Accuracy:** 97–98%.
* **Purpose:** Evaluate whether reviews are positive, negative, or neutral to better weight recommendations.

## 5. Application Development
The web application provides:
* **Search & Auto-complete:** Users can search for movies easily.
* **Movie Details Page:** Displays title, rating, duration, genres, cast, and synopsis.
* Actor Details: Additional info about actors.
* **Recommendation Page:** Suggests similar movies based on the selected one.
* **Sentiment Insights:** Displays aggregated sentiment from user reviews.

**Architecture:**
    * Python (Flask) backend.
    * HTML/CSS/JS frontend for interaction.
    * Integration with TMDB API for dynamic data retrieval.

---

## Technologies Used
| Category                    | Tools / Libraries                      |
| --------------------------- | -------------------------------------- |
| **Data Collection**         | Web Scraping (BeautifulSoup), TMDB API |
| **Data Processing**         | Pandas, NumPy, **pickle**              |
| **Visualization**           | Matplotlib, Seaborn                    |
| **Machine Learning**        | Scikit-learn, NLTK                     |
| **Application Development** | Flask, HTML, CSS, JavaScript           |
| **Dataset Sources**         | Kaggle, Wikipedia, TMDB                |


## Testing with Multiple Datasets
To ensure robustness and generalization, the model was also tested using the TMDB 5000 Movies Dataset. The content-based model maintained high accuracy and consistent performance across datasets, validating its reliability.

## Results and Insights

* **Model Accuracy (Sentiment Analysis):** ~98.7%
* **Content-Based Model:** Performed best for personalized movie suggestions.
* **Collaborative Model:** Less accurate due to lack of user-specific data.


## Application Interface in Pictures

**Home Page of the Application**  
![Home Page](static/screenshots/Home%20Page.png)

**Movie Suggestions (Autocomplete)**  
![Movie Suggestions](static/screenshots/Movie%20Suggestions.png)

**Description of the Searched Movie**  
![Movie Description](static/screenshots/Movie%20Description.png)

**Actors of the Movie**  
![Actors](static/screenshots/Actors.png)

**Actor Information**  
![Actor Info](static/screenshots/Actor%20Info.png)

**User Reviews Analysis**  
![Reviews Analysis](static/screenshots/Reviews%20Analysis.png)

**Recommendation Result**  
![Recommendation Result](static/screenshots/Recommendation%20Result.png)


## Contributors
- [Ahnin Chaimaa](https://github.com/chaimaa-101) 
- [Bnyiche Mouna](https://github.com/itsmawna) 
- [Eddaoudy Aya](https://github.com/EddaoudyAya) 
- [El Alami Nihad](https://github.com/nihadel7) 


## ✨ Happy Coding & Movie Hunting 🎬 !!



