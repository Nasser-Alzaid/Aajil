# FinalFile: Purchase Order Data Analysis & Machine Learning

## Overview

This project explores and analyzes purchase order data using Python, pandas, and machine learning techniques. The goal is to clean the data, discover patterns, group and cluster purchase orders, and build predictive models to gain business insights.

---

## Problem-Solving Journey

### 1. **Data Import & Exploration**

- Loaded the dataset (`purchase-order-items.xlsx`) into a pandas DataFrame.
- Inspected the data structure and types using `df.info()` and `df.head()`.

### 2. **Data Cleaning**

- Dropped irrelevant columns: `Item Name`, `Currency Code`, `Tax ID`, and `Project ID`.
- Checked for duplicate or highly correlated columns (e.g., compared `Total Bcy` and `Sub Total Bcy`).
- Handled missing values using KNN imputation for numeric columns.

### 3. **Feature Engineering**

- Converted columns to appropriate data types (e.g., `Quantity` to integer).
- Grouped data by `Purchase Order ID` to calculate total values per order.

### 4. **Exploratory Data Analysis**

- Visualized correlations between features using heatmaps.
- Identified relationships and patterns in the data.

### 5. **Clustering and Grouping**

- **Clustering by Purchase Order:**  
  Used K-Means clustering to group purchase orders based on total `Quantity` and `Total Bcy` per order.  
  Visualized clusters with scatter plots to interpret groupings.
- **Grouping by Product:**  
  Grouped all `Item ID` and `Purchase Order ID` values for each unique `Product ID` into lists, allowing analysis of which items and orders are associated with each product.

### 6. **Machine Learning Model (Regression Example)**

- Built a regression model (Random Forest) to predict `Total Bcy` from `Quantity` and other features.
- Split the data into training and testing sets.
- Evaluated the model using metrics like Mean Squared Error and R² Score.

### 7. **Exporting Results**

- Saved the cleaned and processed DataFrame to `FinalFile.xlsx` for further use or reporting.

---

## How to Use

1. Clone this repository.
2. Place your `purchase-order-items.xlsx` file in the project directory.
3. Run the notebook `ML_Model.ipynb` step by step.
4. Review the generated `FinalFile.xlsx` for cleaned and enriched data.

---

## Key Learnings

- Data cleaning and preprocessing are crucial for reliable analysis.
- Clustering and grouping help uncover hidden patterns and segments in business data.
- Machine learning models can predict important business metrics and support decision-making.

---

## Requirements

- Python 3.x
- pandas, numpy, matplotlib, seaborn, scikit-learn, openpyxl

---

## Author

This project was developed as a practical exercise in data analysis and machine learning for purchase order
