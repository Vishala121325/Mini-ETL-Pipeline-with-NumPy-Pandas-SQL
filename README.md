# Week 2 – Mini ETL Pipeline with NumPy, Pandas & SQL

## Project Overview
This repository contains a **mini ETL (Extract–Transform–Load) pipeline** built using **Python**, **NumPy**, **Pandas**, and **SQLite**. The pipeline processes messy real-world datasets (e.g., Flipkart product reviews or India Census data) and demonstrates SQL query capabilities on the transformed data.

This project is part of my **Predictive Maintenance / Data Engineering learning roadmap** and represents the Week 2 milestone.

---

## Project Goals
- Extract raw data from a CSV file.
- Transform the data by cleaning, handling missing values, removing duplicates, and feature engineering.
- Load the cleaned data into a **SQLite database**.
- Run SQL queries for aggregation, filtering, and analytics.
- Showcase **NumPy vectorization** and **Pandas internals** for efficient data processing.

---

## Technologies Used
- Python 3
- Pandas
- NumPy
- SQLAlchemy + SQLite
- Google Colab

---

## Project Structure
Week2-ETL-Pipeline/
- etl_pipeline.ipynb # Main Colab notebook with ETL code
- README.md
- data/
-- Dataset-SA.csv # Example dataset (not included)

---

## Pipeline Steps

### 1️⃣ Extract
- Upload and read a CSV file into a Pandas DataFrame.
- Inspect dataset shape, column types, and missing values.

### 2️⃣ Transform
- Remove duplicate rows.
- Clean text fields (e.g., reviews) and standardize case.
- Handle missing or non-numeric values in numeric columns (e.g., ratings).
- Feature engineering:
  - `review_length` → length of review text.
  - `high_rating` → binary flag for ratings ≥ 4.
- Use **NumPy vectorized operations** for efficiency.

### 3️⃣ Load
- Save the cleaned dataset into a **SQLite database** using SQLAlchemy.
- Database table: `mytable`.

### 4️⃣ SQL Queries
Example queries performed on the loaded table:
- Count of reviews per product.
- Average rating per product (with minimum review filter).
- Categorization of reviews by length (short/medium/long).
- Filter high-rating reviews.

---

## Usage Instructions

1. Open the Colab notebook.
2. Install required packages:

```python
!pip install sqlalchemy sqlite-utils

Upload your CSV dataset via the notebook file upload dialog.

Run the ETL pipeline cells: extract → transform → load.

Run example SQL queries on the cleaned database.

Optionally, download the resulting SQLite database.

---

## Outcome

Successfully built a mini ETL pipeline that processes messy datasets.

Cleaned and transformed data efficiently using Pandas and NumPy.

Stored transformed data in SQLite and demonstrated multiple SQL queries.

Prepared the dataset for further modeling or analytics.
