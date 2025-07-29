# Sales_Performance_Analysis
R &amp; S Superstore is a leading retail company with operations across multiple locations and a diverse range of products. The shareholders aim to find more ways to improve the store’s productivity. The dashboard is the result attained from understanding the shareholders requirements to uncovering meaningful and actionable insights. 

# Executive Summary
This report presents a detailed analysis of sales performance of R & S superstore. Based on the star schema data model and KPIs extracted from the dataset. The objective is to evaluate key sales indicators, identify trends, and provide actionable insights to support business growth and operational efficiency.

![dashboard](https://github.com/LawanMercy/Sales_Performance_Analysis/blob/main/dashboard.jpeg)

### Data Source

The dataset used for this project was gotten from R&S Supermarket, it contained detailed information about sales transactions made by the store.

### Tools
- Microsoft Excel - for data cleaning and transformation, pivot table, data modeling, dashboard.

### Data Cleaning and Transformation

The data was loaded into Excel Power Query, where I performed cleaning and transformation. I checked for null values and errors, and found none in the dataset. I verified the data types for each column, and while most were correct, I changed the data type for the Postal Code and Product ID columns from 'Number' to 'Text'. I also split the Location ID column using the 'Split Column by Delimiter' command, which separated it into two columns. I deleted 'Location ID.2' as it was not needed for the analysis and renamed 'Location ID.1' to 'Location ID'. Finally, I changed its data type to 'Text'.
![Data Transformation](
### Data Modeling
-
