# 🎬 Movie Recommender System

A **Content-Based Movie Recommender System** built using **Natural Language Processing (NLP)** and **Machine Learning**. The application recommends movies based on their similarity in genres, keywords, cast, crew, and movie overview using the **TMDB 5000 Movies Dataset**.


## 🌐 Live Demo

🔗 **[Try the application here](https://cine-compass-2005.streamlit.app/)**

---

## 📌 Overview

This project recommends movies similar to a selected movie by analyzing textual metadata. It leverages NLP techniques to process movie information and uses cosine similarity to identify the most relevant recommendations. Movie posters are fetched dynamically using the TMDB API.

---

## ✨ Features

- Content-based movie recommendation system
- NLP-based feature engineering
- Text preprocessing using stemming
- Feature extraction using Bag of Words (CountVectorizer)
- Cosine similarity-based recommendation engine
- Dynamic movie posters using the TMDB API
- Interactive web interface
- Optimized recommendation storage for faster loading and deployment

---

## 🛠️ Tech Stack

- Python
- Pandas
- NumPy
- Scikit-learn
- NLTK
- Streamlit
- Requests
- TMDB API

---

## 📂 Dataset

This project uses the **TMDB 5000 Movies Dataset** available on Kaggle.

Dataset:
https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata

The dataset is **not included** in this repository due to its size. Download the following files and place them in the project directory before running the notebook:

- `tmdb_5000_movies.csv`
- `tmdb_5000_credits.csv`

---

## 📁 Project Structure

```text
Movie-Recommender-System/
│
├── app.py
├── requirements.txt
├── README.md
├── .gitignore
│
├── model/
│   ├── movie_list.pkl
│   └── top_recommendations.pkl
│
├── movie recommender system.ipynb
└── LICENSE
```

---

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/srijitaaa2005/MOVIE-RECOMMENDER-SYSTEM.git
```

Navigate to the project directory:

```bash
cd MOVIE-RECOMMENDER-SYSTEM
```

Create a virtual environment:

```bash
python -m venv .venv
```

Activate the virtual environment.

**Windows**

```bash
.venv\Scripts\activate
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

---

## 🔑 TMDB API Key

Create a `.env` file in the project root directory and add your TMDB API key:

```text
TMDB_API_KEY=your_api_key_here
```

You can obtain a free API key by creating an account on **The Movie Database (TMDB)**.

---

## ▶️ Running the Application

```bash
streamlit run app.py
```

---

## 🧠 How It Works

1. Merge the movies and credits datasets.
2. Perform data preprocessing and feature engineering.
3. Apply stemming and create a combined text representation for each movie.
4. Convert text into numerical vectors using **CountVectorizer**.
5. Compute cosine similarity between movies.
6. Store only the **Top 10 recommendations** for each movie to reduce storage requirements.
7. Recommend similar movies and display their posters using the TMDB API.

---

## 📈 Optimization

Instead of storing the complete cosine similarity matrix, the project stores only the **Top 10 recommended movie indices** for each movie. This significantly reduces storage requirements while maintaining the same recommendation quality and improving application startup time.

---

## 📜 License

This project is licensed under the MIT License.

