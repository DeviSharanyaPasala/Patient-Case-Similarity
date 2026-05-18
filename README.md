# Patient Case Similarity

I built this to explore whether you could use NLP techniques on structured medical data by first converting it into text, then treating it like a document similarity problem.

The dataset is the South African Heart Disease (SAHeart) dataset - 462 patients with features like blood pressure, LDL cholesterol, tobacco use, obesity, and age. I converted each patient record into a short medical note, ran TF-IDF on it, and used cosine similarity to find patients with similar profiles.

K-Means clustering then grouped patients into risk tiers, and PCA brought it down to 2D so the clusters are actually visible. There's also a small Flask API that takes a patient profile as input and returns the most similar cases.

## What's in the notebook

- Data loading and preprocessing from the SAHeart CSV
- Converting structured rows into unstructured text records
- TF-IDF vectorization with NLTK preprocessing
- Pairwise cosine similarity computation
- K-Means clustering with PCA visualization
- Flask API prototype for case retrieval

## Dataset

SAHeart dataset - 462 records, 9 clinical features, binary label for heart disease presence.

## Stack

Python, Pandas, Scikit-learn, NLTK, Flask, Matplotlib
