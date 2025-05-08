# Netflix Movie Recommendation System with Spark ALS
A scalable, collaborative filtering-based movie recommendation engine built with Apache Spark, trained on over 100 million ratings to deliver personalized suggestions and support cold-start scenarios through dynamic similarity modeling.

## 📌 Project Overview
Objective: Build a robust movie recommendation system leveraging large-scale user rating data.

Dataset: 100M+ ratings from 480K+ users.

Platform: Apache Spark (PySpark MLlib)

## 🧠 Key Highlights
### Data Preparation & Analysis
Preprocessed and validated sparse rating data (notably, ~35% movies rated by only one user).

Engineered user and item features to handle missing data and ensure matrix factorization effectiveness.

Used distributed computing on Spark for efficient processing of large-scale data.

### ALS-Based Recommendation Pipeline
Built a collaborative filtering model using Alternating Least Squares (ALS) from Spark MLlib.

Tuned model hyperparameters through grid search and cross-validation:

rank=5, regParam=0.1, maxIter=10

Achieved:

Train RMSE: 0.64

Test RMSE: 0.88

Improvement: 18% better than untuned baseline

### Real-Time Recommendation Engine
Computed cosine similarity between latent movie vectors to provide movie-to-movie recommendations.

Demonstrated 23% improvement over Euclidean distance for style-based matching.

Enabled top-K movie suggestions for cold-start users by dynamically updating similarity scores.

## ⚙️ Tech Stack
Language: Python (PySpark)

Framework: Apache Spark MLlib

Model: Alternating Least Squares (ALS)

Similarity Metric: Cosine Similarity (for cold-start recommendation)
