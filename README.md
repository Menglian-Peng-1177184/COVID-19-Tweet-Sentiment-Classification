# COVID-19 Tweet Sentiment Classification

## Overview

This project applies machine learning techniques to classify the sentiment of tweets related to COVID-19. It explores how different text preprocessing methods and machine learning models can be used to analyse social media text and identify public sentiment during the pandemic.

The project compares three classification algorithms: Multinomial Naive Bayes, Multi-Layer Perceptron (MLP), and Linear Support Vector Machine (Linear SVM).

## Dataset

The project uses the **Coronavirus Tweets NLP Dataset**, containing tweets collected during the COVID-19 pandemic.

- Training dataset: 41,157 records
- Testing dataset: 3,798 records
- Main text column: `OriginalTweet`
- Target column: `Sentiment`

The dataset contains five sentiment categories:

- Extremely Positive
- Positive
- Neutral
- Negative
- Extremely Negative

## Methodology

### 1. Data Preprocessing

The text preprocessing steps include:

- Converting text to lowercase
- Removing URLs
- Removing non-alphabetic characters
- Removing stop words while retaining important negation words such as `no`, `nor`, and `not`
- Applying WordNet lemmatisation

### 2. Feature Extraction

TF-IDF (Term Frequency-Inverse Document Frequency) is used to convert text data into numerical features for machine learning models.

The vectoriser is configured with a maximum of 3,000 features.

### 3. Machine Learning Models

Three classification algorithms are implemented and compared:

| Model | Description |
|---|---|
| Multinomial Naive Bayes | A probabilistic model commonly used for text classification |
| Multi-Layer Perceptron (MLP) | A feedforward neural network that learns patterns in text features |
| Linear SVM | A linear Support Vector Machine used to separate sentiment categories |

### 4. Model Optimisation

GridSearchCV is used to explore different hyperparameter combinations and identify suitable model configurations.

- 3-fold cross-validation
- Macro F1-score for model selection
- Hyperparameter tuning for the classification models

### 5. Model Evaluation

The models are evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Classification reports

The experiments compare model performance to understand how different algorithms perform on multi-class sentiment classification.

## Technologies Used

- Python
- Pandas
- Scikit-learn
- NLTK
- TF-IDF
- Machine Learning
- Natural Language Processing (NLP)
- Jupyter Notebook

## Project Structure

```text
COVID-Tweet-Sentiment-Classification/
│
├── data/
│   └── COVID-19 tweet dataset
│
├── notebooks/
│   └── COVID_Tweet_Classification.ipynb
│
└── README.md
```

*The folder and notebook names above are examples. Adjust them to match the files in your repository.*

## How to Run

1. Clone or download this repository.
2. Install the required Python packages:

```bash
pip install pandas scikit-learn nltk gdown
```

3. Download or provide access to the COVID-19 tweet dataset.
4. Open the Jupyter Notebook.
5. Run the notebook cells in order to perform preprocessing, feature extraction, model training, hyperparameter tuning, and evaluation.

## Learning Outcomes

Through this project, I gained practical experience in:

- Cleaning and preprocessing unstructured text data.
- Applying NLP techniques to social media data.
- Transforming text into numerical features using TF-IDF.
- Implementing and comparing different machine learning classification algorithms.
- Using cross-validation and GridSearchCV for hyperparameter tuning.
- Evaluating multi-class classification models using different performance metrics.

## Project Purpose

This project was completed as part of a postgraduate Data Mining assignment. It demonstrates the application of machine learning and natural language processing techniques to a real-world text classification problem.
