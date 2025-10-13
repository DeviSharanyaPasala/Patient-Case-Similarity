# Patient Case Similarity Analysis Using NLP and Machine Learning

**Author:** Devi Sharanya Pasala  

**Department of Information Science and Technology, University at Albany, SUNY, NY, USA**  

**Email:** [dpasala@albany.edu](mailto:dpasala@albany.edu)  

---

## Project Overview

This project presents an **NLP-based system** that identifies and groups similar patient cases using the **South African Heart Disease (SAHeart)** dataset.  
The model extracts structured insights from unstructured medical records through **TF-IDF** and **cosine similarity**, supporting early diagnosis and clinical decision-making.  
Clustering techniques further group patients with similar medical profiles, enhancing interpretability and diagnostic accuracy.

---

## Objectives

* To extract structured features from medical records using TF-IDF.  
* To measure similarity between patient cases using cosine similarity.  
* To apply clustering algorithms for grouping similar patient profiles.  
* To develop a backend prototype using Flask for real-time similarity queries.  

---

## Models and Methods

The study followed an **NLP-driven analytical approach** integrating traditional machine learning techniques:

* **Text Feature Extraction:** TF-IDF Vectorization  
* **Similarity Measurement:** Cosine Similarity  
* **Clustering Algorithm:** K-Means Clustering  
* **Dimensionality Reduction:** PCA (for visualization)  
* **Backend Framework:** Flask (for patient query and case retrieval)  

Each patient record was converted into a simulated medical note, preprocessed with **NLTK**, and analyzed through feature extraction and similarity computation.

---

## Dataset

* **Source:** South African Heart Disease (SAHeart) Dataset  
* **Content:** 462 patient records  
* **Attributes:** sbp, tobacco, ldl, adiposity, famhist, typea, obesity, alcohol, age, chd  
* **Label:** chd (1 = presence of heart disease, 0 = absence)  
* **File Format:** CSV  

This dataset was chosen due to its relevance to cardiovascular diagnosis and its well-balanced feature distribution for modeling.

---

## Implementation Steps

1. **Data Loading and Preprocessing**
   * Load dataset from Google Drive.
   * Encode categorical variables and handle missing values.  

2. **Unstructured Data Simulation**
   * Convert structured fields into medical note–style text entries.

3. **Text Cleaning and Feature Extraction**
   * Remove stopwords, punctuation, and apply TF-IDF vectorization.  

4. **Cosine Similarity and Clustering**
   * Compute pairwise similarity between cases.
   * Apply K-Means clustering to group similar profiles.

5. **Visualization**
   * Use PCA to reduce dimensionality for 2D cluster visualization.

6. **Flask Backend**
   * Deploy a prototype Flask API for querying similar patient cases.

---

## Results

* Successfully clustered patient cases with similar cardiovascular profiles.  
* Cosine similarity effectively identified patients with shared risk factors.  
* Clustering provided interpretable groupings (high-risk, moderate-risk, low-risk).  
* Flask API allows retrieval of similar cases for clinical decision support.

---

## Key Findings

* NLP-based similarity methods can enhance patient stratification and diagnosis.  
* TF-IDF and cosine similarity provided strong performance for small datasets.  
* Clustering identified underlying patient subgroups based on clinical features.  
* The framework can be extended to larger EHR datasets for practical deployment.

---

## Conclusion

The project demonstrates that **text-based similarity modeling** combined with clustering can effectively identify patients with similar health patterns.  
By converting structured data into unstructured text and leveraging NLP, this approach bridges the gap between traditional health analytics and real-world medical text processing.  
With real patient notes, this framework could evolve into a **clinical decision support system (CDSS)** to assist physicians in diagnosing heart-related conditions.

---

## Technologies Used

* Python  
* Pandas, NumPy  
* Scikit-learn  
* NLTK  
* Matplotlib  
* Flask  
* Google Colab  

---

## Contact

For questions or collaboration, contact:  
**Devi Sharanya Pasala**  
[dpasala@albany.edu](mailto:dpasala@albany.edu)

---

### If you find this project useful, please consider giving it a star on GitHub!
