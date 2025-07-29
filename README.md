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

![Data Transformation](https://github.com/LawanMercy/Sales_Performance_Analysis/blob/main/Data%20Transformation.png)

### Data Modeling
1. I first identidied the entities and attributes.
2. Entities: product, Customers, Location.
3. The Dim Customers was created
4. The facts table contains the measures and the facts about the data.

| Table Name       | Type      | Key Field   | Description                                            |
| ---------------- | --------- | ----------- | ------------------------------------------------------ |
| Dim Customers    | Dimension | Customer ID | Contains customer details like name                    |
| Dim Product      | Dimension | Product ID  | Categorizes products by name, category, sub-category   |
| Dim Location     | Dimension | Location ID | Contains geographic attributes (city, state, region)   |
| Dim Calendar     | Dimension | Date        | Time attributes such as year, quarter, month           |
| Order Fact Table | Fact      | Order ID    | Core transactional data: sales, profit, quantity, etc. |

<p>
  <img src="https://github.com/LawanMercy/Sales_Performance_Analysis/blob/main/Dim%20Customers.png?raw=true" width="500">
  <img src="https://github.com/LawanMercy/Sales_Performance_Analysis/blob/main/Dim%20Location.png?raw=true" width="500">
</p>

<p>
  <img src="https://github.com/LawanMercy/Sales_Performance_Analysis/blob/main/Dim%20Product.png?raw=true" width="500">
    <img src="https://github.com/LawanMercy/Sales_Performance_Analysis/blob/main/Dim%20Calender.png?raw=true" width="500">
</p>

![Order Fact Table](https://github.com/LawanMercy/Sales_Performance_Analysis/blob/main/Order%20Facts%20Table.png)


### ER Diagram

The following Entity-Relationship diagram illustrates the star schema model used in this analysis. The data originates from a facts order table supported by five dimension tables:

![ER Diagram](https://github.com/LawanMercy/Sales_Performance_Analysis/blob/main/ER%20Diagram.png)

### Table Relationship
- Fact to Dimensions Relationships:
    - Many-to-one from Order Fact Table to:
        - Dim Product via Product ID
        - Dim Customers via Customer ID
        - Dim Calender via Order Date
        - Dim Location via Location ID
- This relationship ensures referential integrity and enable multi-perspective analysis

### Key Metrics and Key Performance Indicators Analyzed

The following Entity-Relationship diagram illustrates the star schema model used in this analysis. The data originates from a facts order table supported by five dimension tables:

The following metrics are derived from the Order Fact Table:
| Metrics      | Value   | 
| ---------------- | --------- |
| Total Profit   | $286,397 |
| Total Product     | 1,894 items |
| Total Orders    |9,994 | 
| Total Revenue    | $2,297,201  |
| Previous Year Revenue |$2,297,201 |
| Average Shipping Days |4 |

**Trend Analysis**
- **Sales Over Time**
  - Highest sales observed in Q4 across most years, likely due to holiday shopping
  - Month-over-month sales fluctuated with spikes in November and December
  - Weekly patterns show Monday and Friday as peak sales days
- **Profit Over Time**
  - Profit trends mirror sales but with noticeable drops in months with high discounts
  - Q2 saw high revenue but low profit due to promotional campaigns

**Customer Analysis**
- **Segment-Wise Sales**
  - Consumer segment generate highest revenue, followed by the coeporate segment.
  - Home Office segment is growing but it has the lowest profit margins.
- **Retention Opportunity**
  - High value customers with decreasing monthly sales can be targeted for retention campaigns
    

### Key Insights Based on Analysis

1.  Technology product category generates more profit for the business, with technology having the highest profit in  2015, 2016, and 2017. While office supplies has the highest profit in 2014.

2.  The consumer segement generates more profit for the business, it has displayed a consistent profitability trend throught the years.

3.  The top customers who are generating more profits for the business varies over the years.  In 2017,  we have Raymond Buch, Hunter Lopez, Tom Ashbrook, Andy Relter and Jame Waco as the top 5 customers.
In  2016, we have Tamara Chand, Adrian Barton, Sanjit Engle, Bill Shonely and Daniel Raglin, as the top customers.
In 2015 and 2014, we also have different sets of top 5 customer. which denoted we need to look into our customer service/satisfactory concern of our customers

4.  Majority of the sold products falls under office supplies.

5. Revenue were mostly generate in Califonia, New York, Washington and Pnnsyvania and the company generate the least revenues from Wyoming, South Dakota, West  Virginia, and North Dakota.

6. Majority of our order Perecntage are placed through standard Class.


