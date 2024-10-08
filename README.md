# Restaurant-Recommendation-System
This project is a Restaurant Recommendation System built using a machine learning-based approach. It recommends restaurants based on the similarity of customer reviews. The system is implemented using TF-IDF and Cosine Similarity for text-based recommendation.
# Features
Text-based recommendations: Uses restaurant reviews to recommend similar restaurants.
Cosine Similarity: Calculates the similarity between restaurants based on reviews.
Data preprocessing: Handles data cleaning, such as removing stopwords, punctuations, and URLs from the text reviews.
Mean Rating Normalization: Scales restaurant ratings between 1 and 5.
# Dataset
The dataset used in this project is Zomato Restaurant Data, containing details like restaurant names, ratings, reviews, costs, etc. The dataset can be downloaded from the below link
```
https://drive.google.com/file/d/1cctIlxOBh2bOzSCx0Sd2t--NgkG05XEF/view?usp=sharing
```
# Installation
Clone the repository:
```
git clone https://github.com/yourusername/restaurant-recommendation-system.git
cd restaurant-recommendation-system
```

Install the necessary dependencies:

You can use the following command to install all the required packages in a Python virtual environment:
```
pip install -r requirements.txt
```
Here's a list of the main libraries used:
```
numpy
pandas
seaborn
matplotlib
scikit-learn
nltk


```
Download NLTK stopwords:

```
python -c "import nltk; nltk.download('stopwords')"

```

# Usage
Preprocessing the Data:

The dataset undergoes several transformations:

Columns like url, phone, dish_liked, etc., are removed.
Null values are removed.
Costs are converted to numeric values.
Restaurant ratings are cleaned and normalized.
Punctuations, URLs, and stopwords are removed from the reviews.

# Testing the Recommendation Function:

The recommendation function can be tested using the restaurant's name. For example:
```
recommend('Pai Vihar')

```

This function will return the top 10 restaurants similar to "Pai Vihar" based on the reviews.


# Data Preprocessing
The following steps are performed to clean and preprocess the data:

Removing Unnecessary Columns: Columns like url, dish_liked, and phone that do not contribute to the recommendation system are removed.

Handling Duplicates: Any duplicate entries are dropped from the dataset.

Converting Costs to Numeric Values: The cost column values are converted to numeric by replacing commas with dots.

Cleaning Ratings: The rate column is cleaned to remove non-numeric values and normalized between 1 and 5.

Text Preprocessing:

Lowercasing the reviews.
Removing punctuation, stopwords, and URLs from the reviews.
TF-IDF Matrix: A TF-IDF matrix is created from the reviews to quantify the importance of words.

Cosine Similarity: Cosine similarity is computed to measure the similarity between restaurant reviews.

# Recommendation Algorithm
The system takes a restaurant name as input.
It computes the cosine similarity between the given restaurant's reviews and the rest of the dataset.
It selects the top 30 most similar restaurants based on cosine similarity scores.
Out of the top 30, it returns the 10 highest-rated restaurants.


# Results
The system will output the Top 10 restaurants based on customer reviews, cuisines, cost, and ratings.

# Technologies Used
Python: For all computations, data handling, and building the recommendation system.
Pandas: For data manipulation and preprocessing.
Scikit-learn: For implementing TF-IDF and Cosine Similarity.
# Future Improvements
Advanced NLP: Implement more advanced NLP techniques like Word2Vec or BERT for better semantic understanding.
User-based Recommendations: Add user-based collaborative filtering for personalized recommendations.
Real-time Data: Connect with real-time APIs to get live restaurant reviews and update the system dynamically.
# License
This project is licensed under the MIT License - see the LICENSE file for details.


