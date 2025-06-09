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
  
| **Column Name** | **Data Type** | **Description**                                            |
| --------------- | ------------- | ---------------------------------------------------------- |
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
- **Created measures**: Total Revenues, Total Orders, Total quantity,...
- **Created calculated columns**: Time of Day, Date Hierarchy,...
- Created day and time to identifier in the Calendar table to enable consistent joins across related tables.

## Insights
**1. Sales Trends and Anomalies**
a. Daily, Weekly, and Monthly Sales Trends (2015)
**- Daily trend:** Sales peak consistently around 12 PM, with a visible decline after 8 PM.
**- Weekly trend:** The highest revenue is generated on Fridays, followed closely by Thursdays and Wednesdays. The lowest is on Sundays.
**- Monthly trend:** August shows the highest revenue (1,935 orders), while October records the lowest (1,646 orders). Revenue generally rises mid-year and drops slightly towards the end.

b. Peak Sales Periods, Patterns, and Seasonal Trends
- **Peak hour:** The top revenue hour is 12:00 PM, with $111,878 earned.
- **Seasonality: **There’s a revenue rise from March to August, peaking in August, indicating a potential summer boost.
- **Off-season:** September and October show a drop in orders and revenue, possibly due to school or weather changes.

c. Sales by Day of the Week and Time of Day
- **Best-performing days:** Friday and Thursday dominate weekly sales.
- ** Best time of day:** From 11 AM to 2 PM is the most profitable period.
- **Lowest activity:** Mornings before 10 AM and late evenings after 9 PM.

d. Potential Causes Behind Sales Spikes or Drops
- Spikes in August may be linked to school holidays or promotions (unconfirmed in dataset).
- Drops in October may be due to fewer events or seasonal slowdown.
- 
**2. Product Performance Analysis**
a. Rank pizza categories by total quantity sold and revenue generated.
**- Top 5 Pizzas by Revenue**
Thai Chicken Pizza - $43,000 (5.3% of total revenue)
Barbecue Pizza - $41,000 (5.0% of total revenue)
Californian Pizza - $41,000 (5.0% of total revenue)
Hawaiian Pizza - $38,000 (4.7% of total revenue)
Spicy Italian Pizza - $35,000 (4.3% of total revenue)

**- Top 5 Pizzas by Quantity**
Classic Deluxe Pizza - 2,500 pizzas sold
Barbecue Pizza - 2,400 pizzas (4.8% of total)
Hawaiian Pizza - 2,400 pizzas (4.8% of total)
Pepperoni Pizza - Similar high volumes
Thai Chicken Pizza - Similar high volumes

b. Identify the top 5 and bottom 5 pizzas by both quantity and revenue.
**- Bottom 5 Pizzas by Revenue**
Brie Carre Pizza - $12,000 (1.5% of total revenue)
Green Garden Pizza - $14,000 (1.7% of total revenue)
Spinach Pizza - $15,000 (1.8% of total revenue)
Mediterranean Pizza - Low performer
Calabrese Pizza - Low performer

**- Bottom 5 Pizzas by Quantity**
Brie Carre Pizza - 490 pizzas sold (0.98% of total orders)
Mediterranean Pizza - 912 units (1.84% of total)
Calabrese Pizza - 937 units (1.89% of total)
Spinach Pizza - 970 units (1.95% of total)
Other low performers - Various underperforming specialty pizzas

**3. Size and Ingredient Analysis**
a. Analyze the relationship between pizza size and sales volume within each category.
Large pizzas represent the clear customer preference. This indicates that customers prefer moderate to large portions over specialty extra-large options.

**Large pizzas** - 45.89% of total sales (most popular size)
**Medium pizzas** - 30.49% of total sales
**Regular pizzas** - 21.77% of total sales
**X-Large and XX-Large** - 1.72% combined (minimal market share)

b. Identify the most and least popular ingredients for each pizza category based on quantity sold.
**Most Popular Ingredients Generally:** Pepperoni, Extra cheese, Sausage, and Mushrooms
**Least Popular Ingredients:** Anchovies, Eggplant, Jalapeños, and Broccoli

The data shows that traditional toppings like pepperoni and extra cheese remain the most popular choices, while more unique or acquired-taste ingredients like anchovies and eggplant are consistently avoided by most customers

**4. Order and Ingredient Correlations**
a. Revenue vs. Quantity Sold by Ingredient
The scatter plot is divided using two average reference lines (vertical = quantity; horizontal = revenue), creating four segments:
- **Top Right (High Quantity, High Revenue):** Most profitable and popular ingredients (keep or promote).
- **Top Left (Low Quantity, High Revenue):** High-margin but less frequent — explore upselling.
- **Bottom Right (High Quantity, Low Revenue):** Common but low-margin — consider price adjustments.
- **Bottom Left (Low Quantity, Low Revenue):** Least effective — consider discontinuation.

b. Correlation Between Price and Sales Volume
- The chart on the top right shows a positive correlation between price and volume sold across pizza categories.
- Correlation Coefficient = 0.84, indicating a strong relationship: as **price** increases (possibly due to size), **sales** also tends to increase
- A trend line is plotted to reinforce this relationship.

**5. Order Frequency and Timing**
a. Single-item vs. Multi-item Orders
- The pie chart shows 96.39% of orders are multi-item, while only 3.61% are single-item.
- This indicates strong customer preference for group or family purchases — marketing should focus on combo deals and bulk offers.

b. Average Time Interval Between Orders
- The gauge shows an average interval of 29.5 minutes between orders.
- This suggests relatively frequent ordering throughout the day, but may vary during off-peak hours.
- Use this insight to optimize staffing and kitchen preparation during peak periods.

## Recommendations
- During off-peak hours (before 10 AM and after 9 PM), consider reducing operational costs, such as by changing opening hours at 11AM
- Launching a campaign in September–October to combat seasonal revenue drops.
- Focusing marketing efforts on the top-selling pizzas like Thai Chicken, Barbecue, and Hawaiian
- Upselling drinks, sides, or desserts with multi-item bundles to increase average order value.
- Keeping and  high-demand ingredients like Pepperoni, Sausage, Mushrooms, and Extra Cheese. Consider phasing out low-performing toppings such as Anchovies, Eggplant, and Broccoli, or use them in specialty/seasonal pizzas only.
