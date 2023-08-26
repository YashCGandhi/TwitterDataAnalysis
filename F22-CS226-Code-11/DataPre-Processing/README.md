# PySpark Data Pre-processing Script README

This README provides an overview of the PySpark data pre-processing script and its functionalities.

## Overview

The provided script performs data pre-processing tasks on Twitter data using PySpark. It reads the data from a JSON file, applies various data cleaning and transformation operations, and extracts geographical information from user locations using the spaCy library.

## Script Breakdown

The script is divided into several sections:

### 1. Importing Libraries

This section includes the import statements for various libraries used throughout the script, such as PySpark, NLTK, NumPy, and spaCy.

### 2. Creating Spark Session

The script sets up a Spark session for data processing and analysis.

### 3. Reading and Filtering Data

Data is read from a JSON file and processed using PySpark's DataFrame API. Duplicate tweets are removed, and non-English tweets are filtered out.

### 4. Data Pre-processing

The script defines functions to remove emojis, numbers, and user mentions from tweet content. It also applies various regex replacements to clean the content. The NLTK library is used for text processing tasks such as tokenization, stopword removal, and lemmatization.

### 5. Storing Cleaned Data

The pre-processed data is stored in a DataFrame, and unnecessary columns like "tokens" are dropped. The clean data is then written to a new JSON file.

### 6. Geolocation Extraction (spaCy)

Geographical information is extracted from user locations using the spaCy library. The script uses spaCy's "en_core_web_sm" model to identify countries mentioned in user locations.

### 7. Storing Geolocation Data

Extracted country information is stored in a Pandas DataFrame and summarized to count the occurrences of each country. The final country count data is saved as a CSV file.

## Usage

To use the script:

1. Install the required libraries mentioned in the "Importing Libraries" section.
2. Adjust the input JSON file path as needed.
3. Run the script in a compatible environment.

## Note

- The script uses PySpark to handle large-scale data processing efficiently.
- NLTK is used for text processing tasks.
- The spaCy library is used for geolocation extraction.

## Author

Script created by Yash Chinmay Gandhi.



