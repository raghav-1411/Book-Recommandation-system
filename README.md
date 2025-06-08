# 📚 Hybrid Book Recommendation System

A personalized book recommendation engine combining **Content-Based Filtering**, **Collaborative Filtering**, and **Graph-Based Search** to suggest books users are likely to enjoy.

> ⚠️ Currently, the **Hybrid Integration** is a work in progress. Content-Based and Collaborative Filtering modules are fully implemented and tested.

---

## 🔍 Problem Statement

With thousands of books available, readers often face **decision fatigue**. Traditional recommendation systems may:
- Lack personalization
- Fail to recommend lesser-known books
- Struggle with sparse data

Our goal is to build a **hybrid system** that overcomes these challenges by combining the strengths of multiple recommendation strategies.

---

## 🧠 Methodology

### 1. Content-Based Filtering (✔️ Implemented)
- **Technique**: TF-IDF + Cosine Similarity
- **Data Used**: Titles, Authors, Tags
- **Description**: Recommends books similar to a selected one based on textual metadata.

### 2. Collaborative Filtering (✔️ Implemented)
- **Technique**: Singular Value Decomposition (SVD)
- **Data Used**: User-book ratings matrix
- **Description**: Suggests books liked by users with similar tastes.

### 3. Graph-Based Search (✔️ Prototype)
- **Technique**: A* Algorithm on a Book Similarity Graph
- **Description**: Finds optimal recommendation paths in a similarity network of books.

### 4. Hybrid Recommendation System (🛠️ Pending)
- **Goal**: Combine scores from all three techniques using weighted averages.
- **Plan**: Incorporate dynamic weights and heuristics for final recommendation ranking.

---

## 🗂️ Dataset

- Source: [Goodreads-10k Dataset](https://www.kaggle.com/datasets)
- Includes: Book metadata, user ratings, tags

---

## 🛠️ How to Run

### Prerequisites
- Python 3.8+
- Jupyter Notebook / Google Colab
- Required Libraries:
  - `pandas`, `numpy`, `scikit-learn`
  - `surprise` (for SVD)
  - `networkx` (for graph-based recommendation)

### Files
- `ai project.ipynb`: Contains the current implementation.
- `HybridBookRecommender_Colab.ipynb`: Ready-to-run notebook for Google Colab.
- `Hybrid Book Recommendation System.pptx`: Project overview and presentation slides.

---

## 🧪 Example Usage

```python
# Content-Based Recommendation
get_content_recs("The Hobbit")

# Collaborative Filtering (SVD-based)
get_collab_recs(user_id=5)

# Graph-Based Recommendation (Prototype)
get_graph_recs("1984")

# Hybrid (Coming Soon)
hybrid_recommend(user_id=5, book_title="The Alchemist")
