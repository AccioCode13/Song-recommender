🎵 Song Recommender System

A content-based song recommendation engine using lyrics and natural language processing (NLP). Built using the Spotify Million Song Dataset and powered by TF-IDF vectorization, KNN similarity search, and unsupervised genre clustering.

🔍 Features

🔤 Lyrics Preprocessing: Stopword removal, lemmatization, and cleaning
📊 TF-IDF Vectorization: Converts lyrics into numerical features
🔎 KNN with Cosine Similarity: Finds songs with lyrically similar themes
🎯 Genre Clustering (K-Means): Auto-tags songs into unsupervised genre clusters using their lyrics
🎧 Genre-Based Recommendations: Optionally filter suggestions by genre
💥 Handles Missing or Fuzzy Song Titles Gracefully

📁 Dataset

Source: Kaggle - Spotify Million Song Dataset

Total Songs: ~650,000+
Subset Used: 20,000 for efficiency and prototyping
Fields Used: song, artist, lyrics

🧠 How It Works

Data Preprocessing:
-Remove missing values
-Clean lyrics (punctuation, casing)
-Tokenize + Lemmatize + Remove stopwords
TF-IDF Vectorization:
-Each song lyric is transformed into a sparse vector
-Limited to max_features=3000 for performance
Genre Tagging:
-KMeans clustering on TF-IDF vectors
-Adds a genre_label column based on lyrical themes
Song Recommendation:
-Input a song title (and optional artist)
-Finds similar songs based on lyric similarity
-Optionally filtered by genre

