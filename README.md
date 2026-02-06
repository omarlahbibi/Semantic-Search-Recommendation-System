# Semantic-Search-Recommendation-System

## Overview

This project focuses on building a **search engine and recommendation system for E-commerce products**, using **classical Information Retrieval IR** techniques with **modern Embedding-based semantic search methods**.

The system is designed to take as input:

* **Product descriptions**
* **User preferences and interactions**
* **User search queries**

After a full preprocessing and representation, it outputs:

* **Accurate and relevant search results** aligned with user queries
* **Personalized product recommendations** tailored to user interests

The main goal was to test and compare traditional keyword-based retrieval methods with semantic and multilingual deep learning approaches to improve relevance, robustness, and user experience.

---

## System Architecture

The project consists of two core components:

1. **Recommendation System (Content-Based Filtering)**
2. **Search Engine (Semantic Retrieval)**

---

## Data Processing

All textual inputs (product descriptions, queries, and preferences) go through the following steps:

* Text cleaning (lowercasing, punctuation removal, stopword removal, etc)
* Tokenization and normalization
* Feature extraction and vectorization
* Similarity computation and ranking

This modular pipeline allows easy comparison between different retrieval and representation techniques.

---

## Recommendation System

The recommendation module is **content-based**, focusing on recommending products similar to items a user has previously interacted with.

### Methodology

* Represented product descriptions using **TF-IDF vectors**
* Computed **pairwise similarity scores** between products
* Recommended products with the highest similarity to the user’s interacted items

### Key Characteristics

* No reliance on user-user interactions
* Scales well to new products
* Fully interpretable and easy to evaluate

---

## Search Engine

The search engine retrieves products that best match a user’s query, progressing advanced semantic retrieval.

### 1. Embedding-Based Semantic Search

To overcome vocabulary mismatch and capture semantic meaning, the system was enhanced using:

* **Word2Vec embeddings** for distributed word representations
* **Sentence-BERT (SBERT)** for sentence-level semantic understanding

These approaches allow the system to retrieve relevant products even when the query and product description do not share exact keywords.

### 2. Retrieval Framework

* Used **PyTerrier** for indexing, retrieval, and experimentation
* Enabled flexible experimentation with ranking pipelines

### 3. Zero-Shot Retrieval

Thanks to embedding-based representations, the system supports **zero-shot retrieval**, meaning:

* No task-specific labeled training data is required
* Queries can be matched to relevant products even without keyword overlap

---

## Multilingual Deep Text Search

To support **multilingual search scenarios**, a deep text search tool was integrated:

* Enables retrieval across multiple languages
* Improves robustness for global E-commerce platforms
* Works seamlessly with embedding-based representations

---

## Technologies Used

* **Information Retrieval**: TF-IDF, PyTerrier
* **Embeddings**: Word2Vec, Sentence-BERT
* **Similarity Metrics**: Pairwise, Cosine similarity
* **Deep Learning**: Transformer-based text encoders
* **Languages & Tools**: Python, NLP libraries

---

## Future Improvements

* Incorporate user-based or hybrid recommendation models
* Add learning-to-rank approaches
* Integrate click-through data for evaluation
* Deploy as a real-time API for production use
