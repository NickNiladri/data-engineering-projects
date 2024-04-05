# Data Engineering Projects

This repository contains a PySpark project for music recommendation using collaborative filtering.

## Steps to Execute the Project

### Step 0: Load PySpark and Start a SparkSession

Before starting, ensure that Google Colab mounts your Google Drive for access in the Colab environment. If not using Colab, you can load the dataset using a URL.

Import necessary libraries and create a SparkSession named "Niladrireco".

### Step 1: Load the Raw Dataset

Load the dataset from a .csv file and infer the schema for the columns. Store it in a dataframe called `df_listenings`.

### Step 2: Data Processing / Cleanup

Clean up the data and preprocess it. Drop the 'date' column as it is not relevant for recommendations.

### Step 3: Aggregation

Aggregate the data to find out how many times each user has listened to a specific track. Limit the rows to 20,000 for faster processing.

### Step 4: Convert Columns to Unique Integers

Convert 'user_id' and 'track' columns to unique integer values using StringIndexer.

### Step 5: Train and Test the Data

Split the data into training and testing sets.

### Step 6: Generate Recommendations

Generate top track recommendations for each user.

## Note

This project deviates from standard practices in handling unseen labels during training and testing, using `setHandleInvalid` to keep such labels.

## How to Run

1. Clone the repository.
2. Set up PySpark environment.
3. Execute the code step by step as described above.

## References

- [PySpark Documentation](https://spark.apache.org/docs/latest/api/python/index.html)
- [StringIndexer Documentation](https://spark.apache.org/docs/latest/api/python/reference/api/pyspark.ml.feature.StringIndexer.html)
