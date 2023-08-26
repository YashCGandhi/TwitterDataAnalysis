# 1_twitter_snscrape.ipynb README

This README provides an overview of the script for collecting Twitter data using the `snscrape` tool. The script collects tweets related to specific hashtags and stores them in JSON files organized by dates.

## Overview

The provided script is designed to fetch tweets related to specific hashtags using the `snscrape` tool. It automates the process of collecting and storing tweet data in JSON files for further analysis.

## Script Purpose

The script serves the following purposes:

- Collects tweets based on a list of predefined hashtags.
- Divides the data into time intervals (months) and fetches tweets within those intervals.
- Stores the collected tweets in JSON files, organized by hashtag and date.

## Script Breakdown

The script is divided into several sections:

### 1. Importing Libraries

This section includes the necessary import statements for libraries used in the script.

### 2. Configuration and Parameters

The script sets the `res_limit` parameter to limit the number of tweets collected per query. It also defines a list of hashtags that you can customize according to your data collection requirements.

### 3. Data Collection Loop

The script enters a loop to collect tweets for each hashtag and date interval. It constructs the appropriate query for the `snscrape` tool and uses the `os.system()` function to execute the query.

### 4. Data Storage

The collected tweet data is stored in JSON files within folders named after each hashtag. The folders are organized by dates and intervals.

## Usage

To use the script:

1. Install the necessary libraries and ensure you have `snscrape` installed.
2. Adjust the list of hashtags (`tags`) based on your data collection needs.
3. Run the script in a compatible environment.
4. Collected tweet data will be stored in JSON files within organized folders.

## Note

- The script is designed for data collection using `snscrape`.
- The script uses a loop to fetch tweets for different hashtags and date intervals.

# 2_Combinetweets.ipynb README

This README provides an overview of the Spark script used to combine and filter tweet data collected from JSON files. The script processes individual JSON files containing tweet data and combines them into a single JSON file with selected fields.

## Overview

The provided script is designed to process and combine tweet data collected from multiple JSON files using Spark. It filters tweets based on language, selects specific fields, and combines the filtered tweets into a single JSON file.

## Script Purpose

The script serves the following purposes:

- Initializes a Spark session to process data efficiently.
- Collects a list of paths for all JSON files containing tweet data.
- Defines helper functions for filtering and selecting specific tweet fields.
- Combines and filters tweet data using Spark operations.
- Saves the combined and filtered tweet data into a single JSON file.

## Script Breakdown

The script is divided into several sections:

### 1. Importing Libraries

This section includes the necessary import statements for libraries used in the script, including `findspark` and `pyspark`.

### 2. Spark Initialization

This section initializes the Spark session, sets configuration parameters, and prepares the Spark context.

### 3. Get List of Paths

The script collects a list of file paths for all JSON files containing tweet data. These paths are stored in the `pathlist` variable.

### 4. Helper Functions

The script defines two helper functions:
- `get_data(rawdata)`: Extracts specific fields from raw tweet data.
- `savetweets(tweets)`: Saves a list of tweets as a combined JSON file.

### 5. Combining and Filtering

The script iterates through the collected file paths, reading each JSON file's content, and applying filtering and selection operations to the tweet data. Tweets are filtered based on language (only English tweets are considered), and selected fields are extracted using the `get_data` function.

### 6. Saving Combined Tweets

The combined and filtered tweets are stored in a single JSON file using the `savetweets` function. If a reset counter limit is reached, the current batch of tweets is saved, and the counter is reset.

### 7. Execution

The script's execution is timed using the `%%time` magic command. It provides information about the total file count and total tweet count after processing.

## Usage

To use the script:

1. Install the necessary libraries, including `findspark`, `pyspark`, and `dateutil`.
2. Adjust the `basepath` variable to point to the folder containing your JSON files.
3. Run the script in a compatible environment with Spark support.
4. Combined and filtered tweet data will be saved in a single JSON file.

## Note

- The script utilizes Spark for efficient data processing.
- It combines and filters tweet data based on language and selected fields.

## Author

Script created by Yash Chinmay Gandhi.



