# Python_Diwali_Sales_Analysis
Data Analyst project analyzing Diwali sales, customer behavior, product categories, and regional trends using Python and EDA techniques.
🪔 Diwali Sales Analysis
📌 Project Overview

This project performs Exploratory Data Analysis (EDA) on Diwali sales data to understand customer purchasing behavior, product performance, and sales trends.

The analysis was performed using Python, Pandas, NumPy, Matplotlib, and Seaborn.

The goal is to identify useful business insights that can help businesses understand their customers and improve sales strategies.

🎯 Project Objectives
Analyze customer purchasing behavior
Identify high-performing customer segments
Analyze sales by gender and age group
Identify top-performing states
Analyze sales based on occupation
Identify popular product categories
Find products with high demand
Understand regional and demographic sales patterns
Generate business recommendations from the data
📊 Dataset

The project uses a Diwali Sales dataset containing customer and purchase information.

Important Features
Column	Description
User_ID	Unique customer ID
Cust_name	Customer name
Product_ID	Product identifier
Gender	Customer gender
Age Group	Customer age category
Age	Customer age
Marital_Status	Marital status
State	Customer state
Zone	Geographical zone
Occupation	Customer occupation
Product_Category	Product category
Orders	Number of orders
Amount	Purchase amount
Status	Order status
🛠️ Tools & Technologies
Python
Pandas
NumPy
Matplotlib
Seaborn
Jupyter Notebook
🔄 Project Workflow
Dataset
   ↓
Data Loading
   ↓
Data Cleaning
   ↓
Data Exploration
   ↓
Exploratory Data Analysis
   ↓
Data Visualization
   ↓
Business Insights
   ↓
Recommendations
🧹 Data Cleaning

The following data-cleaning activities were performed:

Loaded the CSV dataset using Pandas
Checked dataset shape
Checked column names
Checked missing values
Removed unnecessary columns
Checked duplicate records
Corrected data types where required
Verified numerical and categorical columns

Example:

import pandas as pd

df = pd.read_csv("Diwali Sales Data.csv", encoding="unicode_escape")

print(df.shape)
print(df.info())
print(df.isnull().sum())
📈 Exploratory Data Analysis
1. Gender Analysis

Analyzed purchasing behavior based on customer gender.

import seaborn as sns
import matplotlib.pyplot as plt

sns.countplot(data=df, x="Gender")
plt.title("Customer Distribution by Gender")
plt.show()

The analysis can be extended to compare both number of customers and total purchase amount by gender.

2. Age Group Analysis

Analyzed sales across different age groups.

sns.countplot(data=df, x="Age Group")
plt.title("Sales by Age Group")
plt.show()

This helps identify the age groups that contribute significantly to the business.

3. State-wise Analysis

Analyzed sales and order volume across different states.

state_sales = df.groupby("State")["Amount"].sum().sort_values(ascending=False)

print(state_sales.head(10))

This helps identify high-performing geographical markets.

4. Occupation Analysis

Analyzed purchasing behavior based on customer occupation.

occupation_sales = df.groupby("Occupation")["Amount"].sum().sort_values(ascending=False)

print(occupation_sales)

This helps businesses understand which professional groups contribute more to sales.

5. Product Category Analysis

Analyzed product categories based on sales and order quantity.

category_sales = df.groupby("Product_Category")["Amount"].sum().sort_values(
    ascending=False
)

print(category_sales)

This helps identify popular product categories.

6. Marital Status Analysis

Analyzed customer purchasing behavior based on marital status.

marital_sales = df.groupby("Marital_Status")["Amount"].sum()

print(marital_sales)
7. Top Products

Identified products with higher order volumes.

top_products = df.groupby("Product_ID")["Orders"].sum().sort_values(
    ascending=False
)

print(top_products.head(10))
📊 Key Business Insights

The analysis helps identify patterns such as:

Female customers represent a strong purchasing segment.
Customers in the 26–35 age group are an important customer segment.
Certain states contribute significantly more to overall sales.
Some occupational groups show stronger purchasing behavior.
Food, Clothing, and Electronics are important product categories in the dataset.
Customer demographics can be used to create more targeted marketing campaigns.
Product and regional analysis can help businesses optimize inventory and promotions.

Note: Exact percentages and sales values should be calculated from the dataset rather than estimated.

💡 Business Recommendations

Based on the analysis, businesses can:

Target high-value customer segments with personalized offers.
Focus marketing campaigns on high-performing states.
Promote popular product categories during festive seasons.
Use customer demographics for targeted advertising.
Maintain sufficient inventory for high-demand products.
Analyze customer purchasing patterns to improve future campaigns.
Create personalized offers based on customer characteristics.
📸 Project Visualizations

The project includes visualizations such as:

Gender-wise analysis
Age-group analysis
State-wise sales
Occupation-wise sales
Marital-status analysis
Product-category analysis
Top products
Customer distribution
📁 Project Structure
Diwali-Sales-Analysis/
│
├── Diwali_Sales_Analysis.ipynb
├── Diwali Sales Data.csv
├── README.md
├── requirements.txt
│
└── Images/
    ├── gender_analysis.png
    ├── age_group_analysis.png
    ├── state_analysis.png
    ├── occupation_analysis.png
    └── category_analysis.png
