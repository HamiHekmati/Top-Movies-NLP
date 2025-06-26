### Movie Recommendation with Topic Modeling and Sentence Transformers

This project presents a complete workflow for building and evaluating content-based movie recommendation systems using both traditional topic modeling and modern transformer-based semantic similarity methods. The notebook walks through every major step, from text cleaning and feature engineering to named entity recognition, sentiment analysis, topic extraction, similarity computation, and critical evaluation. The primary objective is to demonstrate how natural language processing (NLP) techniques can be used to discover thematic, contextual, and emotional relationships between movies using only their plot descriptions.

### Overview

Recommending movies based on plot, theme, and mood is a central challenge in content-based recommender systems. This project addresses the problem by comparing two main approaches: topic modeling (with NMF and TF-IDF) and deep semantic modeling (using Sentence Transformers). By transforming plot summaries into topic vectors or dense neural embeddings, and by extracting sentiment and entities, the solution enables robust matching and ranking of movies by their narrative, contextual, and emotional similarity. Key steps include text normalization, named entity recognition, sentiment analysis with both VADER and DistilBERT, feature extraction, topic assignment, and the computation of similarity scores for movie recommendations.

### Dataset

The dataset used in this project is sourced from Kaggle’s [TMDB Top Movies Dataset](https://www.kaggle.com/datasets/spypsc07/imdb-top-movies-dataset/data) and contains detailed information on 9,420 movies from a wide range of eras, genres, and cultures. Each record in the dataset provides the movie’s title, one or more associated genres, and a concise plot description. The collection spans globally acclaimed classics, modern blockbusters, and international masterpieces, including a variety of genres such as drama, comedy, crime, romance, animation, fantasy, and action. With more than 9,000 unique titles and a rich mix of genre combinations, this dataset offers a realistic and diverse foundation for building and evaluating content-based movie recommendation systems. Throughout the project, movie descriptions are used as the primary source for extracting themes, sentiment, named entities, and dense semantic features, supporting a comprehensive analysis of narrative similarity and recommendation performance.

### Project Workflow

The workflow begins with thorough text preprocessing, including cleaning, tokenization, and lemmatization of movie descriptions. Named Entity Recognition (NER) is applied to extract structured information such as names, places, and dates from each plot summary, enriching the data for further analysis.

Sentiment analysis is performed using both VADER (a lexicon-based tool) and DistilBERT (a transformer-based model) to provide a nuanced view of the emotional tone in each plot summary, allowing comparison between classical and deep learning sentiment scores.

For feature engineering, a TF-IDF matrix is generated to highlight the most distinctive words across the corpus. Non-negative Matrix Factorization (NMF) is then applied for topic modeling, identifying dominant themes and assigning each movie a vector of topic weights. This allows for an interpretable, high-level analysis of movie content.

To recommend similar movies, cosine similarity is computed between movies based on their topic vectors, and the most closely related films are identified for each query title. The limitations of this approach are discussed, and enhancements such as improved preprocessing and minimum similarity thresholds are suggested.

For more accurate and context-aware recommendations, Sentence Transformers are used to embed each movie description into a dense semantic vector. Cosine similarity between these embeddings provides a powerful modern baseline for semantic matching, enabling the identification of films that are narratively and contextually aligned, even when surface vocabulary differs.

### Key Features & Techniques

This project features end-to-end NLP preprocessing (including NER and lemmatization), dual sentiment analysis approaches (VADER and DistilBERT), and two distinct vectorization strategies (topic modeling and sentence embedding). Careful visualization and analysis accompany each step, including bar plots for genre distribution, tables of top terms and topics, and qualitative inspection of recommendation results. The code includes robust functions for generating recommendations by title, supporting both traditional and modern NLP methods.

### Results

Analysis demonstrates that topic modeling can successfully group movies by high-level themes, but often misses finer narrative or emotional connections. Embedding-based similarity using Sentence Transformers yields more accurate and contextually meaningful recommendations, closely matching movies by semantic content rather than just thematic overlap. Sentiment analysis with both VADER and DistilBERT adds an extra dimension for exploring tone and mood. Tables and visualizations throughout the notebook make it easy to interpret and critique results.

### Contact

For questions, suggestions, or collaboration, please connect via [LinkedIn](https://www.linkedin.com/in/hami-hekmati-399932154/) or by opening an issue in this repository. This project was developed by Hami Hekmati as part of a data science and NLP portfolio to showcase expertise in modern recommendation systems.