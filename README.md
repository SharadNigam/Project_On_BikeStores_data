
<h1> Project On BikeStores Data </h1>

<h3>METHODOLOGY</h3>
  
 
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

Data was collected from their open source site, and i have uploaded the sql query files in the folder 'dataset' which you can run to obtain the same.
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

<h3> STEPS IF YOU WISH TO RECREATE THIS PROJECT </h3>

1.After having imported the data in Sql, write down the following query in the sql terminal:
  
 The query which i wrote is available here:
 https://github.com/SharadNigam/Project_On_BikeStores_data/blob/main/SQLQuery2.sql
  
  **_This will basically give you a table containing order_id,customer names (with their first and last names joined into one column), City, State, roder_date, total_units, revenue, product_name,category_name,store_name,sales_rep_**
 
2.Open excel and create a blank workbook and import the data from your sql server database by also pasting the above query in the advanced options so that only the selected columns and their associated data is imported in.

3.Analyze the data for the above questions using pivot tables and filtering followed by charts/graphs creations.

<h3>FINAL THOUGHTS</h3>
  It was lot of fun and education filled project, i have attached my completed excel file named **'BikeStores.xlsx'** with everything completed in it for if anyone feels lost or needs to cross verify their findings with mine.
