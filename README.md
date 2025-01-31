
## SALES ANALYSIS OF AN E-COMMERCE STORE

### Key Low Metrics on customer’s data base to improve sales, customer retention and operational efficiency

## Introduction
This report outlines the process and insights derived from an e-commerce store sales analysis I carried out as a simulated hired Data Analyst.The purpose of the project is to help improve sales, customer retention and operational efficiency and as a hired data analyst my task is use the customers data base and analyze their historical data, uncover trends and provide recommendations for strategic improvements.

## Problem Statement

## 📂 Files in This Repository
- **Task_4_ecommerce_data_internpulse.ipynb** → Jupyter Notebook for data analysis.
- **dataset_for_ecommerce.xlsx** → The dataset used for analysis.
- **README.md** → Explanation of the project.

## Objectives
1. Sales Trends Analysis
a. Identify historical sales trends (e.g., monthly, seasonal, or annual patterns).
b. Highlight the top-performing product categories and assess their contribution to overall revenue.

2. Customer Retention and Loyalty
a. Calculate the customer retention rate and identify the percentage of returning customers.

3. Geographical Performance
a. Pinpoint regions with high and low sales performance.
b. Evaluate the possible reasons behind the sales differences (e.g., demographics, logistics).

4. Delivery and Sales Relationship
a. Assess how delivery status (e.g., on-time, delayed, canceled) impacts sales and customer satisfaction in various regions.

5. Shipping Type vs. Delivery Performance
a. Analyze how different shipping options (e.g., standard, expedited, or same-day) influence delivery performance.

6. Customer Segmentation
a. Perform customer segmentation to identify groups based on preferences, behavior, or demographics.
b. Discover which segments show the most interest in specific products or categories

## Methodology
This project was conducted using Excel and Python, with data sourced from an e-commerce store. The methodology followed a systematic approach that involved several key steps:

1. Data cleaning: The data was first cleaned using Microsoft Excel to ensure accuracy by addressing missing values, correcting data inconsistencies and standardizing entries.
2. Data transformation: key variables were transformed to make the data suitable for analysis.
3. Exploratory Data Analysis (EDA): Through EDA, I explored trends in customers, examine customers retention and operational efficiency in other to improve the sales of the business.
4. Advanced Analysis: I conducted more advanced analysis including predicting outcomes, uncovering trends and patterns, and also operational efficiency using Python
5. Dashboard Creation: I created an interactive dashboard in Python using matploylib.pylot and seaborn libraries.

## Analysis

### Objective 1. Sales Trends Analysis

a. Identify historical sales trends (e.g., monthly, seasonal, or annual patterns).

```python
# Import Necessary Libraries
import pandas as pd
import seaborn as sns
import numpy as np
import matplotlib.pyplot as plt

# Load the Excel file
data = pd.read_excel('/content/sample_data/dataset for ecommerce.xlsx')

## Monthly Sales Trend

```python
# Install necessary libraries
!pip install matplotlib seaborn

# Convert order_date to datetime
df['order_date'] = pd.to_datetime(df['order_date'])

# Extract year and month for trend analysis
df['year'] = df['order_date'].dt.year
df['month'] = df['order_date'].dt.month

# Monthly Sales Trend: Aggregate sales by month across all years
monthly_trends = df.groupby('month').sum(numeric_only=True)['sales_per_order'].reset_index()

# Plot Monthly Sales Trends
plt.figure(figsize=(10, 6))
sns.lineplot(data=monthly_trends, x='month', y='sales_per_order', marker='o', color='blue')
plt.title('Monthly Sales Trends (All Years)')
plt.xlabel('Month')
plt.ylabel('Total Sales')
plt.xticks(range(1, 13))  # Ensure months are displayed correctly
plt.show()


![image](https://github.com/user-attachments/assets/58a12a1c-1e7b-4e6a-8efc-a9505338cc00)


# Yearly Sales Trend

```python
# Yearly Sales Trend: Aggregate sales by year
yearly_trends = df.groupby('year').sum(numeric_only=True)['sales_per_order'].reset_index()
     

# Plot Yearly Sales Trends
plt.figure(figsize=(10, 6))
sns.barplot(data=yearly_trends, x='year', y='sales_per_order', palette='viridis')
plt.title('Yearly Sales Trends')
plt.xlabel('Year')
plt.ylabel('Total Sales')
plt.show()


