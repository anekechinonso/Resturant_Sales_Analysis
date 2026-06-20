# Resturant_Sales_Analysis
Restaurant Sales Prediction and Revenue Driver Analysis
Work Overview
This project focused on restaurant transaction data to get the key factors influencing revenue and to build a model capable of predicting restaurant sales (Revenue).
The analysis combines Preparing data, data cleaning, exploratory data , feature engineering, visualisation, and predictive modelling to provide actionable business insights for restaurant management.

Business Problem
Restaurant owners need to understand the factors driving sales performance in order to improve profitability, optimise pricing strategies, and make informed operational decisions.
The primary objectives of this project are:
1.	Predict restaurant sales (Revenue) using the transaction data.
2.	Identify the key revenue drivers contributing to overall restaurant performance.
3.	Generate actionable insights from customer purchasing behaviour and payment patterns.

Dataset Description
The dataset contains restaurant transaction records with the following features:
Feature	Description
Order ID	Unique identifier for each order
Customer ID	Unique customer identifier
Category	Product category
Item	Product purchased
Price	Unit price of item
Quantity	Quantity ordered
Order Total	Total value of transaction
Order Date	Date of purchase
Payment Method	Method used for payment
Dataset Size
•	Rows: 17,534
•	Columns: 9

Data Cleaning and Wrangling
Several preprocessing steps were performed to prepare and improve data quality analysis.
Missing Value Treatment
Item Feature
Missing values were replaced with:
"Unknown"
Payment Method feature
Missing values were replaced using the mode:
strategy="Selecting the first value
Price
Missing values were imputed using the median value
Quantity
Missing values were imputed using the median value.
Order Total
Missing values were engineered using:
Order Total = Price × Quantity
Date Transformation
The Order Date column was converted into datetime format and engineered to create additional  features were extracted:
•	Year
•	Month
•	Quarter
•	Day

Exploratory Data Analysis (EDA)
The exploratory analysis focused on identifying revenue patterns, customer behaviour, and sales trends.
Key Questions Explored
•	Which product categories generate the highest revenue?
•	Which item are the best sellers?
•	Which payment methods are most frequently used?
•	How does revenue change over time?
•	Which year realized a higher revenue?

Visualisations
The following visualisations were created:
1. Revenue by Category
Bar chart showing revenue contribution by product category.
2. Category Revenue by share
Pie chart displaying the percentage contribution of each category.
3. Revenue by Payment Method
Bar chart Analysis of customer payment preferences.
4. Monthly Revenue Trend
Line chart showing revenue patterns over the course of 2022 and 2023.
5. Price Distribution
Histogram used to identify pricing patterns and potential outliers.
7. Price vs Order Total
Scatter plot with regression trendline showing the relationship between pricing and sales.
8. Top 10 Selling Items
Horizontal bar chart highlighting the most purchased menu items.

Machine Learning Workflow
Step 1: Define Target Variable
y = Revenue
Step 2: Define Features
Features used for prediction:
•	Category
•	Item
•	Price
•	Quantity
•	Payment Method
•	Order_Year
•	Order_month
•	Order_day
•	Quarter
Step 3: Train-Test Split
The dataset was divided into training and testing sets.
Step 4: Preprocessing Pipeline
The modelling pipeline included:
•	Missing value imputation
•	Categorical encoding
•	Feature transformation
Step 5: Baseline Model
A baseline model was established using the mean order value.
Step 6: Model Training
Models evaluated included:
Random Forest Regressor
Used this model due to superior predictive performance.

Model Performance
Random Forest Regressor
Metric	Score
MAE	0.09
R²	0.997
Interpretation
The model explained approximately 99.7% of the variation in restaurant sales and achieved a very low prediction error.
Kindly note that: 
Revenue = Price × Quantity
Since both Price and Quantity were included as predictor variables, the model benefited from information that directly determines the target variable.
This may introduce target leakage and explains the exceptionally high predictive performance.

Key Business Insights
Revenue Drivers
•	Main Dishes generated the highest revenue contribution.
•	Desserts and Starters contributed significantly to overall sales.
•	Drinks generated the lowest revenue among product categories.
Customer Behaviour
•	Credit Card payments were the most commonly used payment method.
•	Several items consistently outperformed others in sales volume/. Items like Pasta Alfredo, Side Salad and Ice cream.
Sales Trends
•	Seasonal patterns became visible after aggregating sales by month.

Business Recommendations
1. Focus on High-Revenue Categories
Increase promotions and menu visibility for Main Dishes.
2. Cross-Selling Opportunities
Bundle Main Dishes with Desserts and Drinks to increase average order value.
3. Payment Incentives
Encourage Digital Wallet and Card payments.
4. Product Optimisation
Monitor top-performing items and remove or change consistently underperforming product items.

Technologies Used
•	Python
•	Pandas
•	NumPy
•	Plotly Express
•	Scikit-learn
•	Jupyter Notebook

Future Improvements
•	Predict daily or monthly revenue instead of individual order totals.
•	Reduce target leakage by excluding variables directly used to calculate Order Total.

Visualisation

<img width="983" height="525" alt="category revenue by share" src="https://github.com/user-attachments/assets/330265e8-57ba-4e97-bc59-ac25f023d68c" />

