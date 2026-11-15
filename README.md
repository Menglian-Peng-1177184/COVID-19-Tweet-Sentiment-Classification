# COVID-19 Tweet Sentiment Classification

## Overview

This project explores sentiment classification of COVID-19-related tweets using Natural Language Processing (NLP) and machine learning techniques.

The main objectives are:

1. **Algorithm Comparison:** Compare the performance of different machine learning algorithms for multi-class sentiment classification.
2. **Preprocessing Comparison:** Investigate how different text preprocessing techniques and feature extraction methods affect classification performance.

Three machine learning algorithms are implemented: Multinomial Naive Bayes, Multi-Layer Perceptron (MLP), and Linear Support Vector Machine (Linear SVM).

## Dataset

The project uses the Coronavirus Tweets NLP Dataset, containing tweets collected during the COVID-19 pandemic.

- Training dataset: 41,157 records
- Testing dataset: 3,798 records
- Text column: `OriginalTweet`
- Target column: `Sentiment`

The dataset contains five sentiment categories:

- Extremely Positive
- Positive
- Neutral
- Negative
- Extremely Negative

## Methodology

### 1. Data Preprocessing Comparison

Different text preprocessing approaches are explored to investigate their effects on model performance.

The preprocessing techniques include:

- Converting text to lowercase
- Removing URLs
- Removing non-alphabetic characters
- Stop word removal, while retaining important negation words such as `no`, `nor`, and `not`
- WordNet lemmatisation

The experiments examine how preprocessing choices influence the quality of text features and classification results.

### 2. Feature Extraction

Text representation method is investigated:

- Term Frequency-Inverse Document Frequency (TF-IDF)

These technique convert textual data into numerical features that can be used by machine learning algorithms.

### 3. Machine Learning Algorithm Comparison

Three classification algorithms are implemented and compared:

| Algorithm | Description |
|---|---|
| Multinomial Naive Bayes | A probabilistic algorithm commonly used for text classification |
| Multi-Layer Perceptron (MLP) | A neural network that learns patterns from numerical text features |
| Linear SVM | A Support Vector Machine that uses a linear decision boundary for classification |

The comparison aims to identify the strengths and performance differences of each algorithm.

### 4. Hyperparameter Tuning

GridSearchCV is used to explore different hyperparameter combinations and identify suitable model configurations.

The experiments include:

- 3-fold cross-validation
- Macro F1-score for model selection
- Hyperparameter tuning for the classification models

### 5. Model Evaluation

Model performance is evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Classification reports

The results are used to compare the impact of preprocessing methods, feature extraction techniques, and machine learning algorithms.

## Technologies Used

- Python
- Pandas
- Scikit-learn
- NLTK
- Natural Language Processing (NLP)
- TF-IDF
- Bag of Words
- Machine Learning
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

*Adjust the folder and notebook names to match your actual repository.*

## How to Run

1. Clone or download this repository.
2. Open the Jupyter Notebook.
3. Run the notebook cells in order to perform data preprocessing, feature extraction, model training, hyperparameter tuning, and evaluation.

## Learning Outcomes

Through this project, I gained practical experience in:

- Exploring and preprocessing unstructured text data.
- Comparing different text preprocessing techniques.
- Applying Bag of Words and TF-IDF for feature extraction.
- Implementing and comparing multiple machine learning algorithms.
- Using cross-validation and GridSearchCV for hyperparameter tuning.
- Evaluating multi-class classification models using different performance metrics.
- Analysing how preprocessing and algorithm choices influence model performance.

## Project Purpose

This project was completed as part of a postgraduate Data Mining assignment. It demonstrates an experimental approach to NLP and machine learning by investigating how text preprocessing, feature extraction, and algorithm selection affect sentiment classification performance.
