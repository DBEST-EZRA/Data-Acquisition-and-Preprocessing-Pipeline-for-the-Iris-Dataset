# Data Acquisition and Preprocessing Pipeline for the Iris Dataset

## Overview
This project implements a data acquisition and preprocessing pipeline for the Iris dataset. The pipeline processes raw data into a clean, normalized form and stores it in a SQLite database for analysis. The main steps include **Data Acquisition**, **Feature Extraction**, **Data Transformation**, and **Data Loading**.

---

## Pipeline Steps

### 1. Data Acquisition
The Iris dataset is loaded using the `sklearn.datasets` library. It includes measurements for three species of flowers:  
- *setosa*  
- *versicolor*  
- *virginica*  

The dataset provides information on sepal and petal dimensions along with the species label.

---

### 2. Feature Extraction
Relevant features are selected to simplify the dataset, focusing on:  
- `sepal length (cm)`  
- `sepal width (cm)`  
- `species`  

This step ensures that only the most relevant information is used for downstream tasks.

---

### 3. Data Transformation
The numerical features (`sepal length` and `sepal width`) are normalized to a range of [0, 1] using `MinMaxScaler`. This transformation ensures that all features are on a comparable scale, which is essential for analysis and machine learning.

---

### 4. Data Loading
The processed data is stored in a SQLite database named `iris_data.db`. This allows for efficient storage and retrieval of the cleaned dataset for further use.

---

## Testing
- **Unit Tests**: Validate individual functions, such as feature extraction, to ensure they perform as expected.
- **Integration Test**: Verify the entire pipeline from data acquisition to database storage.

---

## Results
The pipeline processes the Iris dataset successfully, resulting in:
1. Cleaned and normalized data.
2. Storage in a structured SQLite database (`iris_data.db`).

The database is now ready for further analysis or integration into other workflows.

---

## Dependencies
The following Python libraries are required:
- `pandas`
- `sklearn`
- `sqlalchemy`

Install them using:
```bash
pip install pandas scikit-learn sqlalchemy
