# Automobile Data Cleaning Pipeline 🚗

## Project Overview
This project involves building a comprehensive data preprocessing pipeline using Python and Jupyter Notebook. The goal was to clean a raw automotive dataset to make it suitable for machine learning or analysis. The process addresses common data quality issues such as missing values, outliers, inconsistent formatting, and scaling.

This repository was created as part of a Data Science assignment to demonstrate proficiency in data wrangling techniques.

## Dataset
* **Input File:** `DATASET FOR ASSIGNMENT # 1.csv` (Raw automotive data)
* **Output File:** `cleaned_automotive_data.csv` (Processed and standardized data)
* **Domain:** Automotive (Features include make, horsepower, engine size, price, etc.)

## Technologies Used
* **Python 3.x**
* **Pandas:** For data manipulation and dataframe management.
* **NumPy:** For numerical operations.
* **Scikit-Learn:** specifically `SimpleImputer` for missing values and `StandardScaler` for normalization.
* **Matplotlib/Seaborn:** Imported for potential visualization support.

## Data Cleaning Steps
Following the assignment requirements, the notebook implements the following 8-step pipeline:

1.  **Remove Irrelevant Data:** Checked dataset columns for relevance to the domain.
2.  **Remove Duplicates:** Identified and dropped duplicate rows to ensure data uniqueness.
3.  **Remove Unnecessary Spaces:** Stripped leading/trailing whitespace from string columns.
4.  **Handle Inconsistent Capitalization:** Standardized text data to "Title Case" to fix issues like "alfa-romero" vs "Alfa-Romero".
5.  **Data Type Conversion:** * Converted '?' placeholders to `NaN`.
    * Coerced numeric columns to correct `float/int` types.
    * Converted categorical variables (e.g., make, fuel-type) to `category` dtype.
6.  **Handle Missing Values (Imputation):**
    * **Numeric Data:** Imputed using the **Median** strategy (more robust to outliers than Mean).
    * **Categorical Data:** Imputed using the **Most Frequent** (Mode) strategy.
7.  **Handle Outliers:** Detects outliers using the IQR (Interquartile Range) method and handles them via **Capping** (setting to lower/upper bounds) rather than deletion to preserve data volume.
8.  **Standardization:** Applied `StandardScaler` (Z-score normalization) to all numeric features to bring them onto a similar scale (mean=0, std=1).

## How to Run
1.  Clone this repository.
2.  Ensure you have the required libraries installed:
    ```bash
    pip install pandas numpy scikit-learn matplotlib seaborn
    ```
3.  Place the raw dataset (`DATASET FOR ASSIGNMENT # 1.csv`) in the root directory.
4.  Open `231980059_Nayab.ipynb` in Jupyter Notebook or JupyterLab.
5.  Run all cells to generate the cleaned CSV file.

## Author
* **Nayab** 
