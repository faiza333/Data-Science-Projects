## Dataset
The dataset contains 20 columns, namely, Row ID, Order ID, Order Date, Ship Date, Ship Mode, Customer ID, Customer Name, Segment, Country, and City.

### First:
Using python to clean the data then convert the csv to sql 

### Second using sql:

- Use the LEAD window function to create a new column sales_next that displays the sales of the next row in the dataset. This function will help you quickly compare a given row’s values and values in the next row.

- Create a new column sales_previous to display the values of the row above a given row.

- Rank the data based on sales in descending order using the RANK function.

- Use common SQL commands and aggregate functions to show the monthly and daily sales averages.

- Analyze discounts on two consecutive days.

- Evaluate moving averages using the window functions.
