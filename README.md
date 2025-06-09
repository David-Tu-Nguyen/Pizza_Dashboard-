# Pizza_Dashboard
Analyzed data for a pizza manufacturing and distribution company to identify insights and suggest improvements for business performance.
[Preview_Dashboard](https://github.com/David-Tu-Nguyen/Coffee_Shop_Sales_Analysis/blob/main/PowerBI_Dashboard/Dashboard_Snapshot.gif/). 

## Main objective

**1. KPIs:** Create KPI cards displaying the following metrics: Total Revenue, Total Quantity Sold, Total Orders, Average Order Value and Average Pizza per Order.

**2. Sales Trends and Anomalies**
   a. Analyze and present daily, weekly, and monthly sales trends across 2015.
   b. Identify peak sales periods, patterns, and any seasonal trends.
   c. Investigate sales performance by day of the week and time of day.
   d. Examine and identify the potential causes behind significant sales spikes or drops on specific dates throughout the year.
   
**3. Product Performance Analysis**
   a. Rank pizza categories by total quantity sold and revenue generated.
   b. Identify the top 5 and bottom 5 pizzas by both quantity and revenue.
   
**4. Size and Ingredient Analysis**
   a. Analyze the relationship between pizza size and sales volume within each category.
   b. Identify the most and least popular ingredients for each pizza category based on quantity sold.
   
**5. Order and Ingredient Correlations**
   a. Investigate the correlation between revenue and quantity sold by specific ingredients. Use two average reference lines to segment the ingredients into four distinct groups for comparison.
   b. Explore the correlation between average pizza prices and sales volume across categories. Include a trend line and calculate the correlation coefficient between the two variables.
   
**6. Order Frequency and Timing**
   a. Analyze the frequency of single-item vs. multi-item orders.
   b. Examine the average time interval in minutes between orders.

## Data dictionary
- Number of Rows: 48620
- Number of Columns: 10
  
Column Name | Data Type | Description

| **Column Name** | **Data Type** | **Description**                                            |
| `order_id`      | Text/ID       | Unique identifier for each order placed by a transaction.  |
| `date`          | Date          | Date the order was placed (entered into the system).       |
| `time`          | Time          | Time the order was placed (entered into the system).       |
| `quantity`      | Integer       | Quantity ordered for each pizza of the same type.          |
| `pizza_id`      | Text/ID       | Unique identifier for each pizza (includes size and type). |


## Methodology and tools used
Tables
| Step  | Used Tools |
| ------------- |:-------------:|
|First Exploratory Data Analysis & Joining Tables     |     |
|Data Cleaning, Advanced Exploratory Data Analysis & First Visualizations  |  |
|Advanced Data Visualizations & Dashboard    |  Power BI     |

## Data Cleaning and Transformations
I cleaned the data in Power Query and created the following;
- **Created measures**: Total Sales, Total Orders, Total quantity,...
- **Created calculated columns**: Time of Day, Date Hierarchy, Linear Regression Prediction,...

## Insights
**Revenue and transactions**
- Monthly sales have consistently grown since the second month (February), reaching their peak in the sixth month (June) across all stores.
- 72.06% of revenue is generated during weekdays for all stores
- On weekdays, Hell's Kitchen experiences its highest sales on Friday and Tuesday, signifying these as the busiest days. Similarly, Astoria's busiest weekdays are Thursday and Monday. Lower Manhattan's busiest weekday is Monday.

**Store hours**
- Hell's Kitchen and Lower Manhattan operate from 6:00 to 20:00, while Astoria is open from 7:00 to 19:00.
- Peak hours for Hell's Kitchen and Lower Manhattan are between 6:00 AM and 10:00 AM.
- Astoria experiences its busiest period from 7:00 to 10:00, consistently throughout the week and on weekends.
  
> Although Lower Manhattan generates the lowest total revenue, it records the highest sales during peak hours compared to the other locations. In contrast, Astoria achieves the highest sales during non-peak hours among all stores, despite having shorter operating hours.

**Top 3 product and category across all 3 stores.**

a) **Coffee** generated $269,952 in revenue, accounting for 38.6% of total sales, making it the highest-performing product category across all branches.
- Top coffee item at each location:
* Astoria: Barista Espresso (~$27K)
* Hell’s Kitchen: Barista Espresso (~$32K)
* Lower Manhattan: Barista Espresso (~$31K)

b) **Tea** sales make up 27.7% of the total combined revenue from the three stores, amounting to $196,406.
- Leading tea products by store:
* Astoria: Brewed Chai Tea (Spicy Eye Opener Chai, Large) – approx. $27K
* Hell’s Kitchen: Brewed Chai Tea (Morning Sunrise Chai, Regular) – approx. $26K
* Lower Manhattan: Brewed Chai Tea (Morning Sunrise Chai, Regular) – approx. $24K

c) **Bakery** items generated $82,316 in sales, contributing 12.3% to the total revenue across all stores, ranking as the third best-selling product category.

## Recommendations
- Leverage data from peak hours and top-performing days to optimize staffing and inventory distribution.
- Target underperforming locations for improvement while replicating successful strategies from high-performing stores.
- Distribute marketing resources according to the revenue share of each product category.
