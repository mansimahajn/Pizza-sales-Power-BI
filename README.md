# Pizza Sales Dashboard


## Objective
The primary objective of this project is to create an interactive Power BI dashboard that provides comprehensive analysis and visualization of pizza sales data. The dashboard aims to help stakeholders understand sales performance, identify trends, and make informed decisions based on data insights. By leveraging Power BI’s advanced data visualization capabilities, the project delivers a detailed overview of sales dynamics, including revenue generation, order trends, and product performance.


## Features

### First Dashoard


**1. KPI Cards**: Displays critical metrics such as total revenue, average order value, total pizzas sold, total orders, and average pizzas per order.


**2. Trend Charts**: Visualizes daily and monthly trends in total orders.


**3. Donut Charts**: Shows sales percentages by pizza category and size.


**4. Funnel Chart**: Illustrates total pizzas sold by category.


**5. Filters**: Provides filters by pizza category and date range, with interactive elements for in-depth data analysis.


**6. Insights**: Includes key observations and annotations to highlight important data trends and patterns.


### Second Dashboard


**1. Top/Bottom Performers**: Identifies the top 5 and bottom 5 pizzas by revenue, quantity, and total orders.


**2. Performance Analysis**: Analyzes the best and worst-performing pizzas to support strategic business decisions.


## Insights
The dashboard enables users to gain several key insights:

**Sales Performance**: Track overall sales performance and understand daily and monthly trends in order volumes and revenue.

**Product Performance**: Evaluate which pizza categories and sizes contribute most to total sales.

**Revenue Distribution**: Analyze revenue distribution across different pizza types and sizes.

**Top and Bottom Sellers**: Identify the best and worst-performing pizzas based on revenue, order quantity, and sales.

## Formulas Used

**Total Revenue** = SUM(Sales[Revenue])

**Average Order Value** = AVERAGE(Sales[OrderValue])

**Total Pizzas Sold** = SUM(Sales[PizzasSold])

**Total Orders** = COUNT(Sales[OrderID])

**Average Pizzas per Order** = DIVIDE([Total Pizzas Sold], [Total Orders])

**Sales Percentage by Category** = DIVIDE(SUM(Sales[Revenue]), CALCULATE(SUM(Sales[Revenue]), ALL(Sales[Category])))

**Sales Percentage by Size** = DIVIDE(SUM(Sales[Revenue]), CALCULATE(SUM(Sales[Revenue]), ALL(Sales[Size])))

**Top 5 Pizzas by Revenue** = TOPN(5, SUMMARIZE(Sales, Sales[PizzaName], "Revenue", SUM(Sales[Revenue])), [Revenue], DESC)

**Bottom 5 Pizzas by Revenue** = TOPN(5, SUMMARIZE(Sales, Sales[PizzaName], "Revenue", SUM(Sales[Revenue])), [Revenue], ASC)

## Conclusion
This project highlights the use of Power BI for effective data visualization and analysis. The interactive dashboard provides a detailed understanding of sales trends, product performance, and revenue generation, supporting data-driven business decisions.

