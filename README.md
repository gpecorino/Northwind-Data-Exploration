# Northwind-Data-Exploration
**Description**

This project delves into the Northwind database, housing a variety of data for the fictional company Northwind Traders, which specializes in the export/import of specialty foods. My objective is to craft visualizations that narrate the company's story and facilitate data-driven business decisions. To achieve this, I leverage two key tools:
1. PostgreSQL was utilized to pull data from the Northwind database that I use to create my visualizations and to perform other tasks such as inventory management and analysis of customer purchasing behavior.
2. Tableau was used to develop two comprehensive dashboards, enabling in-depth analysis of both sales data and employee performance metrics.

Here you will find a file containing the queries that were used, the tables that I created to make my visualizations and a link to my dashboards on [Tableau Public](https://public.tableau.com/app/profile/giovanni.pecorino/viz/NorthwindDashboards/SalesBreakdown?publish=yes).

**About the Dataset**

This database contains a variety of information about the orders, customers, employees, suppliers and products of Northwind Traders, distributed across multiple tables. To streamline the analysis process, I selectively extracted pertinent data, focusing solely on information essential for addressing crucial business inquiries. Utilizing these refined queries, I generated three tables within this repository, serving as the foundation for crafting my visualizations.

The first table all_order_data.csv contains relevant information for all orders in the database. It has 17 features:
1. Orderid - Order number 
2. Employee - Name of employee that made the sale
3. Order_Date - Date the order was placed
4. Required_Date - Date the customer requires the order by
5. Shipped_Date - Date the order was shipped
6. Shipper - Company that is handling the shipping
7. Freight - Price it costs to ship order
8.Customer - Customer that made the order
9. City - City customer is located in
10. Country - Country customer is located in
11. Product - Product name
12. Category - Category that product belongs to
13. Current_Price - The current price for 1 unit of the product
14. Ordered_Price - The price of the product at the time of order
15. Quantity - Number of units of product ordered 
16. Discount - Amount discounted from the order
17. Total_Sale_Price - Total price of all units ordered

The following table, profit_data.csv, provides insights into the products within each order and the profits generated by Northwind Traders from each transaction. This portion contains data that I generated for this analysis. The original Northwind database does not contain information about how much money Northwind Traders makes on each order so to perform this analysis I had to generate this data myself using 2 key assumptions. First I assume that the prices listed in this dataset refer to the price that Northwind Traders sells these products to the customer for. The next assumption I made was that they yield a profit ranging from 10%-40% on each product. I randomly assigned values in this range to each product to create a cost that Northwind Traders pays to the suppliers for each unit of product. This table contains 16 features:
1. Orderid - Order number
2. Product - Product name
3. Category - Category that product belongs to
4. Order_Date - Date the order was placed
5. Employee - Name of employee that made the sale
6. Customer - Customer that made the order
7. Customer_Price - The price of the product at the time of order
8. Quantity - Number of units of product ordered 
9. Discount - Amount discounted from the order
10. Purchased_Price -  Price of 1 unit of product after applying the discount
11. Supplier_Price - The price Northwind Traders pays to the product supplier
12. Profit_per_Unit - Amount profited off of 1 unit of product
13. Profit_per_Unit_Percent - Percent profited off of 1 unit of product
14. Total_Supplier_Cost - Total cost Northwind pays to supplier for all units of product ordered
15. Total_Sale_Price - Total price customer pays for all units ordered
16. Total_Profit - Total amount profited off of all units ordered

The last table included is the employee_best_customer.csv which shows the customers that employees sold the most to each year. This table contains 4 features:
1. Employee - Name of employee that made the sale
2. Year - Year
3. Customer- Name of the customer
4. Total_Sales - Total amount sold to customer



**Conclusions**
![](images/Sales%20Breakdown.png)
**Technologies**

+ PostgreSQL: Used to create queries for the database
+ Tableau: Used to create visualizations and dashboards

