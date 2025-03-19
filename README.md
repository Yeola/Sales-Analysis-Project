#  E-Commerce Sales Analysis

## Table of Contents

- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Preparation](#data-preparation)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Findings](#findings)
- [Recommendations](#recommendations)
  

### Project Overview

This data analysis project aims to provide insights into the sales performance of an e-commerce company over the year. By analyzing various aspects of the sales data, we seek to identify trends,make data-driven recommendations, and gain a deeper understanding of the company's performance.

### Data Sources

Sales Data: The primary dataset used for this analysis is the "pizza_sales.csv" file, containing detailed information about each sale made by the company.

### Tools

- Excel - Data Preparation
- SQL server - Data Analysis
- PowerBI - Creating Reports

### Data Preparation

In the initial data preparation phase,we performed the following tasks;
- Data loading and inspection
- Data cleaning and formatting.

### Exploratory Data Analysis

- What is the overall sales trends?
- Which products are top sellers?
- what are the peak sales periods?

### Data Analysis

One  of the Analysis in SQL:
Total sales by pizza_size in january
```
Select pizza_size,
cast(sum(total_price) as decimal(10,2)) as Total_sales,cast(sum(total_price) * 100 /(select sum(total_price) from pizza_sales,
where Datepart(quarter,order_date)=1) as decimal(10,2)) as PCTsales
from pizza_sales
where Datepart(quarter,order_date)=1,
group by pizza_size,
order by PCTsales Desc
```

### Findings

The analysis results are summarized as follows:
1. The Pizza sales have been good over the months, With a noticeable peak in january, because of the festivities and july because of the summer and holiday season, while the weekend(Thursday,Friday,Saturday) has the highest sales of the week .
2. The classic Pizza category has the highest sales among the pizza categories.
3. The large(L) Pizza_size has the highest percentage of sales compared to other sizes.
4. The top 5 Pizzas by Revenue are; The thai chicken pizza, The Barbecue chicken pizza, The California Chicken pizza, The Classic deluxe pizza, The Spicy Italian pizza5  
5. The Bottom 5 Pizzas by Revenue are; The Spinach Pesto pizza, The Mediterranean pizza, The Spinach supreme pizza, The Green garden pizza, The Brie carre pizza.

### Recommendations

- Implement seasonal promotions & dicounts during peak sales seasons to maximize revenue : Winter warmth deals in january and Summer feast combos in july, Also implement "Weekend special deals" such as Buy one get one free (BOGO) offers,combo meals or limited-time discounts .
- Focus on expanding and promoting the pizzas in The Classic pizza category.
- Implement a customer segmentstion strategy like loyalty points or dicounts to target high-LTV customers to encourge customer retention and maximize revenue.


