
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

# Display the first 5 rows
print(data.head())

```plaintext
customer_id  customer_full_name  category_name       product_name                            customer_segment  customer_city   customer_state  customer_country  customer_region  delivery_status  order_date           order_id          ship_date          shipping_type  order_item_discount  sales_per_order  order_quantity  profit_per_order  
C_ID_55205   Mary Howell        Office Supplies    Xerox 1898                              Consumer          Quincy         Massachusetts  United States   East            Late delivery    2015-01-02 00:00:00  CA-2015-140795  2015-03-02 00:00:00  Standard Class  8.80                 159.96           1              -32.20  
C_ID_33852   Mary Childs        Furniture          Chromcraft Conference Tables           Consumer          South Bend     Indiana        United States   Central         Late delivery    2015-01-03 00:00:00  CA-2015-104269  2015-06-03 00:00:00  Second Class    89.99                499.95           5              192.68  
C_ID_44861   Mary Yedwab        Office Supplies    Eureka Sanitaire Commercial Upright    Consumer          Chicago        Illinois       United States   Central         Shipping on time 2015-01-03 00:00:00  CA-2016-124107  2015-05-03 00:00:00  Standard Class  34.00                199.99           4              43.16  
C_ID_36140   Theresa McAdams    Office Supplies    Kleencut Forged Office Shears         Home Office      Morgan Hill    California     United States   West            Advance shipping 2015-01-03 00:00:00  US-2016-164966  2015-05-03 00:00:00  Standard Class  20.00                499.95           5              225.58  
C_ID_47887   Ronald Cooley      Office Supplies    Cameo Buff Policy Envelopes           Consumer          Parma          Ohio           United States   East            Shipping on time 2015-01-03 
