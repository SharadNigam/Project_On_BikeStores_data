
# Project On BikeStores Data

<h1>METHODOLOGY</h1>
  
 
(_These are basically the steps i followed for the project_)


**1.Understanding the problem**
_Here we are asking and understanding what the company wants us to do_

For this project the company wanted to know the following questions:
* Condition of sales activity within the company
* Total revenue generated, 
* Revenue per state,
* Revenue per store,
* Revenue per category of items,
* Top 10 customers and 
* Best performing sales rep.

**2.Collecting and Gathering the Data**

Data was collected from their open source site, and i have uploaded the sql querry files which you can run to obtain the same.
To do it follow this process:
1. Open SQL server, create a new database and name it BikeStores
2. Select the new BikeStores database in the SQL server
3. Open the zip downloaded from the link I provided 
4. Open the 'create objects' query file and then execute it in the SQL server for the BikeStores database
5. Open the 'load data' query file and then execute it in the SQL server for the BikeStores database.

_NOTE: The query section of this project was done on SQL server Management Studio 19_


**3.Cleaning the data (if necessary)**

The data was already clean in this case so verification of the data was done here, which was to see for any missing or null values.


**4.Analyzing the data and creating visualizations**

The data was analyzed in Microsoft Excel, and the visualizations(graphs and charts) were also made there.

<h1> STEPS IF YOU WISH TO RECREATE THIS PROJECT </h1>

1.After having imported the data in Sql, write down the following query in the sql terminal:
  
  SELECT
	ord.order_id,
	CONCAT(cus.first_name,' ',cus.last_name) AS 'customers',
	cus.city,
	cus.state,
	ord.order_date,
	SUM(ite.quantity) AS 'total_units',
	SUM(ite.quantity * ite.list_price) AS 'revenue',
	pro.product_name,
	cat.category_name,
	sto.store_name,
	CONCAT(sta.first_name,' ',sta.last_name) AS 'sales_rep'
	FROM sales.orders ord
	JOIN sales.customers cus
	ON ord.customer_id = cus.customer_id
	JOIN sales.order_items ite
	ON ord.order_id = ite.order_id
	JOIN production.products pro
	ON ite.product_id = pro.product_id
	JOIN production.categories cat
	ON pro.category_id = cat.category_id
	JOIN sales.stores sto
	ON ord.store_id = sto.store_id
	JOIN sales.staffs sta
	ON ord.staff_id = sta.staff_id
	GROUP BY 
	ord.order_id,
	CONCAT(cus.first_name,' ',cus.last_name),
	cus.city,
	cus.state,
	ord.order_date,
    pro.product_name,
	cat.category_name,
	sto.store_name,
	CONCAT(sta.first_name,' ',sta.last_name)
  
  **_This will basically give you a table containing order_id,customer names (with their first and last names joined into one column), City, State, roder_date, total_units, revenue, product_name,category_name,store_name,sales_rep_**
 
2.Open excel and create a blank workbook and import the data from your sql server database by also pasting the above query in the advanced options so that only the selected columns and their associated data is imported in.

3.Analyze the data for the above questions using pivot tables and filtering followed by charts/graphs creations.

<h1>FINAL THOUGHTS</h1>
  It was lot of fun and education filled project, i have attached my completed excel file with everything completed in it for if anyone feels lost or needs to cross verify their findings with mine.
