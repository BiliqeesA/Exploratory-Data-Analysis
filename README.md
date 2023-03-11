## SUPER STORE ANNUAL SALES REPORT

### INTRODUCTION

At the end of every calendar year, a business owner would like to compare sales and profit from one year to the next in order to determine which item is the least profitable or the most profitable with respect to sales. In addition, they would like to know who their regular customers are, which month had the highest and lowest sales, and how many products were sold out during that particular year.
### OBJECTIVES

The project's goal is to analyze the store's sales figures for 2016 and 2017 and offer recommendations on how to improve them the following year.
### ABOUT THE DATASET

The data was obtained as an excel file from a secondary source and saved to my Google drive @ (https://docs.google.com/spreadsheets/d/1QvPMSnGuREgU-v_xnN79dhlg2seGSNXD/edit#gid=1276821084). The data consists of the following columns: row, order id, order date, ship date, ship mode, customer id, customer name, segment, country, city, state, postal code, region, product id, category, sub-category, product name, sales, city, quantity, discount, and profit.

![Annotation 2023-02-26 180659](https://user-images.githubusercontent.com/119788228/224508060-3981d988-82e9-4afe-bc34-4d7d70d880cc.png)  
 *Raw dataset*
 
Tool used: **Microsoft Power BI**

After importing the dataset into the power query, the values were categorized into the **dimension table** and **fact table**.
- The **fact table** is a table that contains quantitative data, number data types, dates, continuous variables, **foreign keys**, and **duplicates**.
- The **dimension table** consists of qualitative data, text data type, categorical variables, **primary keys**, and **no duplicates**.

All dimension tables (foreign keys) were linked to the fact table (primary key), establishing relationships between all of the tables. This is done in order to link all relevant data and produce zero-error visualizations.

![Annotation 2023-02-22 173949](https://user-images.githubusercontent.com/119788228/224508223-5f9564b6-f7d9-46b9-bf50-0f64930c0226.png)  
 *Data model of super store dataset*

### DATA CLEANING PROCESS

- Using the Dax formula (Calendar function) below, I created a new measure called **Calendar Date** and extracted the date (date and time) from the **Order date** column:

![Annotation 2023-02-23 060943](https://user-images.githubusercontent.com/119788228/224508392-c90cd967-7ca4-4fb7-96e3-a931ad2eba98.png)  

- Created a new column and extracted the **year** from the **calendar date**, using the function below;

![Annotation 2023-02-23 061024](https://user-images.githubusercontent.com/119788228/224508444-b5fe3edf-9591-4f1c-9892-501f706b2ba8.png)  
 *calendar date function to extract year*

- Created a new column for month

![Annotation 2023-02-23 061114](https://user-images.githubusercontent.com/119788228/224508509-49b80f95-618b-4db3-8e53-f056cdcefb1d.png)  
 *calendar date function to extract month*

- First and last names were included in the customer's name, so I divided the customer name column by delimiter to reduce it to just the first name and first letter of the last name.

![Annotation 2023-02-26 155621](https://user-images.githubusercontent.com/119788228/224508574-0c868c4b-9b1d-4f2c-9ff6-741547d42c24.png)  
 *Split column by delimiter not by the number of characters* *

![Annotation 2023-02-26 155735](https://user-images.githubusercontent.com/119788228/224508668-0cc477aa-8e66-4c7c-9915-b164062f6e84.png)  
 *split column by leftmost delimiter*

![Annotation 2023-02-26 170033](https://user-images.githubusercontent.com/119788228/224508724-c93d2687-26db-4d6e-8bbf-bb5247028fe2.png)  
 *what the customer's name looks like after splitting*
 
### DATA VISUALIZATION & INSIGHTS

The store made a profit of $81,000 in 2016 and a $93,000 profit the following year. In 2016, the store sold over 9000 items, and 12,000 items the following year. This rise in sales and profits was brought on by more potential customers.

![Annotation 2023-02-26 165525,2016](https://user-images.githubusercontent.com/119788228/224514799-ec4a9757-9018-4774-bf86-610591f0e8e2.png)  
 *2016*

![Annotation 2023-02-26 165435,2017](https://user-images.githubusercontent.com/119788228/224514797-5573d55e-b99f-4731-bdcf-62871b5d6184.png)  
 *2017*
 
**Quantity and Sales by Month:**
For the calendar year 2016, super store acquired the highest revenue by December and September with over 1000 items sold out respectively, and had the lowest sales at the beginning of the year 2016 which relatively picked up by May. Compared to the year 2016, sales increased relatively in 2017. The highest sales of items occurred  in September and November 2017 as a result of an increase in the number of items purchased by customers. The increase in sales could also be a result of discounted prices of items offered at the 4th quarter of the year.

![Annotation 2023-03-10 153426,16](https://user-images.githubusercontent.com/119788228/224515375-d99a6beb-223c-45e4-a967-b2d7701a8f9e.png)  
 *2016*

![Annotation 2023-03-10 153558,17](https://user-images.githubusercontent.com/119788228/224515374-768e74f1-7036-43d3-83a8-2116f870689e.png)  
 *2017*
 
**Sales and Profit by Category:**
Items classified under technology had the highest sales and generated more profit than office supplies items. By 2017, there was an increase in sales profit generated by Technology and office supplies items by $45,000 and $47,000 respectively. Even when furniture items has massive sales in 2017 compared to the previous year, there was a drastic loss made from those items.
 



