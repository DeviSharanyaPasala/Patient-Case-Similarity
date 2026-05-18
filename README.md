# Patient Case Similarity

Finding similar patient cases from medical records using NLP and clustering, built on the South African Heart Disease dataset.

The approach converts structured patient records into text descriptions, runs TF-IDF vectorization, and uses cosine similarity to find patients with matching risk profiles. K-Means then groups patients into clusters and a set of classifiers predict heart disease presence.

## How it works

- Each patient record is converted into a medical note style text description
- Text is cleaned and vectorized using TF-IDF
- Cosine similarity matrix (462x462) finds the most similar cases for any given patient
- K-Means clustering groups patients into 4 risk profiles
- Multiple classifiers are trained to predict coronary heart disease

## Dataset

South African Heart Disease (SAHeart) dataset. 462 patients, features include systolic blood pressure, LDL cholesterol, tobacco use, obesity, adiposity, type A behavior score, alcohol intake, family history, and age. Binary label for coronary heart disease presence.

## Results

**Classifier comparison:**

| Model | Accuracy | F1-Score | AUC |
|-------|----------|----------|-----|
| Logistic Regression | 0.7634 | 0.6333 | 0.8006 |
| Gradient Boosting | 0.7312 | 0.5763 | 0.7448 |
| Random Forest | 0.7097 | 0.5574 | 0.7301 |
| K-Nearest Neighbors | 0.6559 | 0.3846 | 0.6261 |
| Support Vector Machine | 0.6452 | 0.1081 | 0.6839 |
| Decision Tree | 0.6022 | 0.4638 | 0.5743 |

Logistic Regression performed best with 76.3% accuracy and AUC of 0.80.

**Clustering (K-Means, 4 clusters, Silhouette Score: 0.0111):**

- Cluster 0: High CHD risk, elevated blood pressure, high LDL, high tobacco use, increased alcohol intake
- Cluster 1: Low risk
- Cluster 2: High CHD risk, elevated blood pressure, high tobacco use
- Cluster 3: High LDL, high tobacco use, increased alcohol intake

## How to run

```bash
pip install -r requirements.txt
jupyter notebook Patient_Case_Similarity.ipynb
```

## Stack

Python, Pandas, Scikit-learn, NLTK, Seaborn, Matplotlib
