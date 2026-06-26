# Sales Analysis

## Table of Contents
- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Cleaning Process](#data-cleaning-process)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data Analysis](#data-analysis)
- [Results](#results)
- [Recommendations](#recommendations)
- [Limitations](#limitations)

## Project Overview
This project aims to gain insight into the performance of an e-commerce company. We seek to understand the company's performance, identify trends and make data-driven recommendations to boost performace by analysing various aspects of the sales data. This dataset was choseen because of the layout of the data which is a great asset to practice data cleaning skills and producing good data models.

## Data sources
The primary dataset for this project is titled "amazon.csv" containing detailed information about the products, customers, pricing and reviews in the columns; product_id, product_name, category, discounted_price, actual_price, discount_percentage,,rating, rating_count, about_product, user_id, user_name, review_id, review_title, review_content, img_link, product_link.
- This dataset was accessed on Kaggle: [Download Here](https://www.kaggle.com/datasets/karkavelrajaj/amazon-sales-dataset/data)

## Tools
- MS excel- For data loading, walkthrough and cleaning
- Power BI- for Analysis and creating a report

## Data Cleaning Process
1. The data was initially loaded and inspected.
2. Unnecessary cloumns were removed
3. Then later split into a fact table, products_info and customer_info tables.
4. Duplicates and missing values were handled accordingly using power query.
5. The customer_info table was special as it lists of information in each row that needed to be split into different columns and then later on, appended into one column.
- This was the moment this author discovered the `TOCOL` function in excel that turns arrays into one column, a very handy function for this type of data layout.
6. Finally, the process ended with a sales table, a products_info and a Customer_info table keeping in mind primary keys for each table.

## Exploratory data analysis
This involved asking questions about the data;
1. What were the overall sales?
2. How many customers did we have?
3. Which products are the top performers?
4. What categories are best rated and worst rated?
5. What is the overall quality of the products ?

## Data Analysis 
DAX functions were used
- `Distinctcount`
e.g `Count of users = DISTINCTCOUNT(AmazonCust_info1[user_id])`

## Results
1. Overall sales were $4.5M.
2. Total Customers were 8K.
3. Top 5 products:
- Kitchen and Home appliances
- Home theatre products
- Mobiles|Accessories
- Wearable technolgy
- Computer|Accessories|Tablets

4. Best rated Category
   - Computers|Accessories|Tablets
5. Worst rated category
   - Cars & Motorbike|Cars accessories
6. The overall quality is 4.09

   
## Recommendations
Based on the analysis, we recommend the following:

1. Be more prudent with the discount rates as we made only 58% of expected revenue due to the very high discount rates.
2. Focus on expanding stock and marketing of the best performing products.
3. Improving the overall quality of the products and using that to market them.

## Limitations 
- After spliting the columns in customer_info table by delimiter, the user_name column had one extra column (user_name.9) with a lot of nulls, blanks and less than five names, while review_id and user_id each had 8. It was removed as it was going to negatively affect the analysis. The assumption was that each comma in the rows of the aforementioned columns represented each each customer, i.e., user-id.1 = review_id.1 = user-name.1.


  






