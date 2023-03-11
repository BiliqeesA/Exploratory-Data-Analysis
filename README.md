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

After importing the dataset into the power query, the values were categorized into the dimension table and fact table.
- The fact table is a table that contains quantitative data, number data types, dates, continuous variables, foreign keys, and duplicates.
- The dimension table consists of qualitative data, text data type, categorical variables, primary keys, and no duplicates.

All dimension tables (foreign keys) were linked to the fact table (primary key), establishing relationships between all of the tables. This is done in order to link all relevant data and produce zero-error visualizations.

![Annotation 2023-02-22 173949](https://user-images.githubusercontent.com/119788228/224508223-5f9564b6-f7d9-46b9-bf50-0f64930c0226.png)  
*Data model of super store dataset*

### DATA CLEANING PROCESS

- Using the Dax formula (Calendar function) below, I created a new measure called Calendar Date and extracted the date (date and time) from the Order date column:

![Annotation 2023-02-23 060943](https://user-images.githubusercontent.com/119788228/224508392-c90cd967-7ca4-4fb7-96e3-a931ad2eba98.png)  

- Created a new column and extracted the year from the calendar date, using the function below;

![Annotation 2023-02-23 061024](https://user-images.githubusercontent.com/119788228/224508444-b5fe3edf-9591-4f1c-9892-501f706b2ba8.png)  
**calendar date function to extract year**

- Created a new column for month

![Annotation 2023-02-23 061114](https://user-images.githubusercontent.com/119788228/224508509-49b80f95-618b-4db3-8e53-f056cdcefb1d.png)  
**calendar date function to extract month**

- First and last names were included in the customer's name, so I divided the customer name column by delimiter to reduce it to just the first name and first letter of the last name.

![Annotation 2023-02-26 155621](https://user-images.githubusercontent.com/119788228/224508574-0c868c4b-9b1d-4f2c-9ff6-741547d42c24.png)  
**Split column by delimiter not by the number of characters** *

![Annotation 2023-02-26 155735](https://user-images.githubusercontent.com/119788228/224508668-0cc477aa-8e66-4c7c-9915-b164062f6e84.png) 
**split column by leftmost delimiter**

![Annotation 2023-02-26 170033](https://user-images.githubusercontent.com/119788228/224508724-c93d2687-26db-4d6e-8bbf-bb5247028fe2.png)  
**what the customer's name looks like after splitting**


