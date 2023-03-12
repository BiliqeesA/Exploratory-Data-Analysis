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

All dimension tables (foreign keys) were connected to the fact table (primary key), establishing relationships between all of the tables. This is done in order to link all pertinent data and create zero-error visualizations.

![Annotation 2023-02-22 173949](https://user-images.githubusercontent.com/119788228/224508223-5f9564b6-f7d9-46b9-bf50-0f64930c0226.png)  
 *Data model of super store dataset*

### DATA CLEANING PROCESS

- I created a new measure called **Calendar Date** and extracted the date (date and time) from the **Order date** column using the Dax formula (Calendar function) listed below:

![Annotation 2023-02-23 060943](https://user-images.githubusercontent.com/119788228/224508392-c90cd967-7ca4-4fb7-96e3-a931ad2eba98.png)  

- Created a new column and extracted the **year** from the **calendar date**, using the function below;

![Annotation 2023-02-23 061024](https://user-images.githubusercontent.com/119788228/224508444-b5fe3edf-9591-4f1c-9892-501f706b2ba8.png)  
 *calendar date function to extract year*

- Created a new column for **month**, which was also extracted from the calendar date column.

![Annotation 2023-02-23 061114](https://user-images.githubusercontent.com/119788228/224508509-49b80f95-618b-4db3-8e53-f056cdcefb1d.png)  
 *calendar date function to extract month*

- I shortened the customer's name because it appeared too long by using only the first name and the first letter of the last name. I split the customers' name column by delimiter and extracted the first letter of the last name, i.e; **'Biliqees Abolomope'** was transformed into **'Biliqees A'**.

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
For the calendar year 2016, the superstore acquired the highest revenue in December and September, with over 1000 items sold out respectively, and had the lowest sales at the beginning of the year, which relatively picked up by May. Compared to 2016, sales increased relatively in 2017. The highest sales of items occurred in September and November 2017 as a result of an increase in the number of items purchased by customers. The increase in sales could also be a result of discounted prices of items offered in the 4th quarter of the year.

![Annotation 2023-03-10 153426,16](https://user-images.githubusercontent.com/119788228/224515375-d99a6beb-223c-45e4-a967-b2d7701a8f9e.png)  
 *2016*

![Annotation 2023-03-10 153558,17](https://user-images.githubusercontent.com/119788228/224515374-768e74f1-7036-43d3-83a8-2116f870689e.png)  
 *2017*
 
**Sales and Profit by Category:**
Over time, the most profitable items were those classified as technology and office supplies, which also had the highest sales. Although furniture-related items initially made significant sales, they eventually started to lose money. This could be the result of the cost price (the expenses to produce the furniture items) being higher than the selling price; as a result, as sales increase, more loss is incurred.

![Annotation 2023-03-10 182609,16](https://user-images.githubusercontent.com/119788228/224555047-1121521b-0320-4d0b-a03b-b3f5c808190d.png)  
*2016*

![Annotation 2023-03-10 182625,17](https://user-images.githubusercontent.com/119788228/224555042-c9b65d1e-68e2-4f4b-966b-dad846b0483a.png)  
*2017*

**Profit by Region and Category:**
In the US southern region, sales of certain products produced more profit in 2016; however, in 2017, sales in this region saw a sharp decline, possibly as a result of some unforeseeable circumstances. In 2017, the western region contributed more to overall profits, which were $46,000 higher than in 2016.

![Annotation 2023-03-10 155143,16](https://user-images.githubusercontent.com/119788228/224555179-b813dd5f-611d-4862-81bc-9fb073346056.png)  
*2016*

![Annotation 2023-03-10 155257,17](https://user-images.githubusercontent.com/119788228/224555183-548345cd-95d7-40e3-8a2e-7f1bdfc4872d.png)  
*2017*

**Sales and Profit by Sub-category:**
Humans will always purchase phones because they want the newest, most luxurious models. The revenue generated from the sales of phones increased by $29,000, with an additional profit of $4,000 in 2017. The purchase of furniture (tables) increased year over year, which led to the store owner suffering more losses.

![Annotation 2023-03-10 154446,16](https://user-images.githubusercontent.com/119788228/224555279-bd74efd4-00f5-445a-9f0f-31791c1abea2.png)  
*2016*

![Annotation 2023-03-10 154531,17](https://user-images.githubusercontent.com/119788228/224555281-c8df07f7-566f-4626-a7e3-9fbcdc11e343.png)  
*2017*

**Top 6 Profitable Products:**
![Annotation 2023-03-10 155459,16](https://user-images.githubusercontent.com/119788228/224555347-6b69d152-14e2-4740-936a-b3844ce6ad9f.png)  
*2016*

![Annotation 2023-03-10 155544,17](https://user-images.githubusercontent.com/119788228/224555346-cff30358-2dbc-4f14-be16-9286ad6d3fe7.png)  
*2017*

**Top 6 purchasing customers:**
Jonathan, Paul, and Edward purchased the highest quantity of items from the store in 2016. While in 2017, John, Seth, and Janet made more purchases.

![Annotation 2023-03-10 155755,16](https://user-images.githubusercontent.com/119788228/224555515-96deab17-8a2e-4bad-8c85-4a8a757bd3aa.png)  
*2016*

![Annotation 2023-03-10 160031,17](https://user-images.githubusercontent.com/119788228/224555518-c82a2840-e2bb-47f4-a6a4-767e2bae3620.png)  
*2017*

**Top 6 purchasing Customers by product category:**

![Annotation 2023-03-10 160238,16](https://user-images.githubusercontent.com/119788228/224555585-510af10e-6fdf-4f58-8c5c-e4c773fab5f6.png)  
*2016*

![Annotation 2023-03-10 160536,17](https://user-images.githubusercontent.com/119788228/224555589-d44dcc21-e409-4fd5-8628-5c50805f556c.png)  
*2017*

### REPORT VIEW
The report is a three-page document:
- The home page 
- Sales report page for 2016
- Sales report page for 2017

![Annotation 2023-02-26 233529](https://user-images.githubusercontent.com/119788228/224555751-00c68238-bee8-471a-a1f6-cf3c221f1b48.png)  
*Home page*

![Annotation 2023-03-12 170132](https://user-images.githubusercontent.com/119788228/224556936-07359e6d-b68b-47a2-9e0d-e9c4d9d33c5a.png)  
*2016 report view*

![Annotation 2023-03-12 170550](https://user-images.githubusercontent.com/119788228/224557427-c7015487-1306-42b2-80a5-bdf11a7a72a1.png)  
*2017 report view*

### RECOMMENDATION
- A business's primary goal is typically to maximize profits. For the products that are losing money, more research can be done to improve them better with lower costs while keeping their selling price. 
- To attract more potential customers and give existing ones more justification for buying a specific product, a marketing campaign can be implemented.










 
 



