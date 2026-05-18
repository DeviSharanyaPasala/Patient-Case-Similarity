# Patient Case Similarity

An NLP system that finds similar patient cases using TF-IDF and cosine similarity, built on the South African Heart Disease dataset. The goal is to surface historical cases with similar risk profiles given a new patient input.

## How it works

Structured patient records are converted into short text descriptions to simulate medical notes. TF-IDF vectorization extracts features from the text after NLTK preprocessing. Cosine similarity then measures how close any two patient profiles are. K-Means clustering groups patients into risk tiers, and PCA reduces the feature space to 2D for visualization. A Flask API prototype allows querying for the most similar cases given a new patient input.

## Model

- Text representation: TF-IDF vectorization
- Similarity metric: Cosine similarity
- Clustering: K-Means (3 clusters: high, moderate, low risk)
- Visualization: PCA (2 components)
- API: Flask

## Dataset

South African Heart Disease (SAHeart) dataset.
- 462 patient records
- Features: systolic blood pressure, tobacco use, LDL cholesterol, adiposity, family history, type A behavior, obesity, alcohol use, age
- Label: binary (1 = coronary heart disease present, 0 = absent)

## Results

- Cosine similarity successfully identified patients with shared cardiovascular risk factors
- K-Means clustering produced three interpretable patient subgroups
- PCA visualization clearly shows separation between risk groups
- Flask API returns top similar cases for a given patient profile

## Stack

Python, Pandas, NumPy, Scikit-learn, NLTK, Flask, Matplotlib
