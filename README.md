## **Movie Recommendation (Content-Based Filtering)**

This project builds a Content-Based Movie Recommender System that suggests similar movies based on movie metadata such as overview, genres, cast, and keywords.

The system uses Natural Language Processing (TF-IDF) and Cosine Similarity to find related movies.

## **📊 Dataset**

We used the TMDB movie dataset available on Kaggle:

👉 [TMDB Movies Dataset](https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset)

**Files used:**
- movies_metadata.csv
- credits.csv
- keywords.csv

## **⚙️ Technologies Used**
- Python  
- Pandas & NumPy  
- Scikit-Learn  
- TF-IDF Vectorization  
- Cosine Similarity (linear_kernel optimization)  
- Matplotlib & Seaborn  
- Pickle (Model Saving)  

## **🔍 Project Workflow**
1. Data Loading & Cleaning  
2. Metadata Processing (genres, cast, keywords)  
3. Feature Engineering (combined text features)  
4. TF-IDF Vectorization  
5. Similarity Calculation (Memory Efficient)  
6. Movie Recommendation Function  
7. Evaluation using genre relevance  
8. Confusion Matrix & Heatmaps  
9. Model Serialization  

## **🧠 Recommendation Logic**
Instead of computing a huge similarity matrix, the system calculates similarity on-demand using:

linear_kernel(tfidf_matrix[idx], tfidf_matrix)


This prevents RAM crashes and makes the system scalable.

## **📈 Evaluation Metrics**
Since recommender systems are not traditional classifiers, relevance is evaluated using genre overlap:
- Accuracy  
- Precision  
- Recall  
- Confusion Matrix  
- Heatmap Visualization  

## **🚀 Run the Project**
1️⃣ **Install Requirements**
```bash
pip install pandas numpy scikit-learn matplotlib seaborn

## **2️⃣ Run Notebook / Script**
Run the Python notebook or script containing the recommendation function.

## **📦 Model File**
The trained model is saved as:

`movie_recommender.pkl`

It stores:
- TF-IDF vectorizer
- TF-IDF matrix
- Movies metadata
- Title index mapping

## **📌 Example Output**
**Input:**  
Avatar  

**Output:**  
- Guardians of the Galaxy  
- John Carter  
- Star Wars  
- Interstellar  
- Avengers
