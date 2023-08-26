# PySpark Sentiment Analysis Readme

This repository contains a PySpark code snippet for performing sentiment analysis on a dataset of tweets. The code demonstrates setting up a PySpark session, reading data from a JSON file, performing sentiment analysis using TextBlob, building machine learning models, and querying data using different Spark operations.

## Prerequisites

Before running the code, make sure you have the following prerequisites:

- Python with PySpark installed (`!pip install pyspark`)
- TextBlob library (`!pip install textblob`)
- Google Colab (or similar environment) for notebook execution
- Access to the provided dataset (JSON file)

## Code Overview

The code is divided into several sections, each performing specific tasks:

1. **Setting up Environment**: Installing required libraries and mounting Google Drive.

2. **Building Spark Session**: Creating a Spark session and reading the JSON dataset using Spark.

3. **Sentiment Analysis**: Using TextBlob library to calculate sentiment polarity for each tweet, categorizing them as positive, negative, or neutral.

4. **Building Machine Learning Models**: Constructing two different models - Logistic Regression and Naive Bayes, to predict sentiment based on the text content.

5. **Model Evaluation**: Evaluating model performance using accuracy, precision, recall, and F1-score metrics.

6. **Querying Data**: Demonstrating queries to find the most liked, most replied, and most retweeted tweets using different Spark operations.

7. **Month-wise Sentiment Counts**: Generating month-wise sentiment counts for positive, negative, and neutral sentiments.

## Execution

1. Clone or download this repository to your local environment.

2. Open the Jupyter notebook in a compatible environment (e.g., Google Colab).

3. Upload the provided JSON dataset to your Google Drive or provide the correct file path in the code.

4. Run each section of the notebook sequentially to execute the code.

## Results

The code demonstrates sentiment analysis on a dataset of tweets using PySpark. It builds machine learning models to predict sentiment and provides insights into the most liked, replied, and retweeted tweets. Additionally, it generates month-wise sentiment counts for further analysis.

Feel free to explore, modify, and extend the code for your specific use case.

## Author

Yash Chinmay Gandhi
