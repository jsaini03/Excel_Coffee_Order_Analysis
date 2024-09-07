# Coffee Orders Analysis on Excel
The goal of the project is to analyze the sale of 4 different types of coffees in United States, Ireland and United Kingdom and to derive valuable insights about the popularity among others.
The primary objective of this analysis includes identifying top customers, sale trends of different coffee types and sales by country. The dashboard created enable the opportunity to determine customer engagement and loyalty in different countries based on type and size of coffee.
### Objectives
- Track total sales over the time for better inventory management
- Analyse sales in US, Ireland and UK to aid expansion
- Identify top 5 customers
### Outcome Expected
The coffee order dashboard will give insights to boost sales and to drive startegic expansion efforts
### Data Source
![Coffee Orders Dataset](https://github.com/mochen862/excel-project-coffee-sales.git)
### Data Overview
Data on coffee sales are divided into 3 spreadsheets:
|Orders|              
|----|                
|Order ID|            
|Order Date|
|Customer ID|
|Product ID|
|Quantity Ordered|

|Customer|
|---|
|Customer ID|
|Customer Name|
|Email|
|Phone Number|
|Address Line|
|City|
|Country|
|Postcode|
|Loyalty Card|

|Products|
|---|
|Product ID|
|Coffee Type|
|Roast Type|
|Size|
|Unit Price|
|Price per 100g|
|Profit|

## Steps Taken
### Data Gathering and Cleaning:
Combined the tables to make a comprehensive table carrying all details related to orders, customer information and product details. These combined columns facilitate a more cohesive representation of the information pertaining to product orders, allowing for more effective analytical processes.
The techniques employed to retrieve data from the Customers Table involve the utilization of the VLOOKUP/XLOOKUP formula. Meanwhile, a combination of the INDEX and MATCH functions is applied to extract information from the Products Table. This approach ensures that a uniform formula can be adapted and applied across every column within the table, enabling the extraction of data in a consistent manner.
### Standardizing the Data
- Email Column: The missing values in the Email column is replaced with an empty cell using an IF 
  statement.
- Sales Column: To populate the sales column, a multiplication between Quantity and Unit Price was 
  done
- Coffee Type Name Column: Abbreviations such as Rob, Exc, Ara, and Lib, were changed to full name 
  by adding a new column _Coffee Type Name_ by using a Nested IF function. This function 
  systematically converted "Rob" to "Robusta", "Exc" to "Excelsa", "Ara" to "Arabica", and "Lib" to 
  "Liberica", thereby enhancing the comprehensibility of the coffee types.
- Roast Type Name Column: A similar approach was extended to the Roast Type Name column where "M" 
  was transformed to "Medium", "L" denoted "Light", and "D" was indicative of "Dark".
- Order Date Column: To mitigate potential confusion arising from varying date formats the month 
  component, previously represented as a numeric value, has been transformed into a categorical 
  value.
- Size Column: The Size column lacked metric value notation. As a solution, the unit "kg" was 
  uniformly appended to each row within this column.
- Unit Price and Sales Column: Changed to currency and $ symbol was added.
- Loyal Card: Added a new column that checks whether the customer has a loyalty card or not.
### Pivot Table and Dashboard:
* Total Sales Sheet:
A pivot table titled "TotalSales" was generated with the purpose of visually representing the aggregate sales across different time periods alongwith 2D Line Chart and 3 Slicers
* Country Bar Chart Sheet :
  Added a new bar graph to represent the countries with the highest sales figures in descending order.
* Top 5 Customers:
  Added a new bar graph and added customer names to the axis category, sorted the whole data in descending order, and then applied the top 5 filter.
* Dashboard :
  !["Dashboard”](/Excel_coffe_analysis_dashboard.jpg)
  
