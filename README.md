# Mobile_Sales_Analysis
## Overview:
+ This is a sales report for Mobile Sales products

 ___

 ## Content:
 Project Overview| Data Source| Tools Used| Table Outlay| Query Languages (SQL)| Visualization

___

## Project Overview:
>> This Project analyzes the sales of Mobile Sales products and shows various attributes such as Brands, Customer Gender, Payment Method Using Pivot table, This analysis helps to understand the key factors of sales in dataset.

___

## Data Source:
www.kaggle.com/dataset

___

## Tools Used:
+ Pivot table / charts
+ Power BI
+ SQL

___

## Table Outlay:
First Three Records

|TransactionID|	Date	|MobileModel|	Brand	|Price|	UnitsSold|	TotalRevenue|	CustomerAge|	CustomerGender|	Location	|PaymentMethod|
|------|------|------|------|------|------|------|------|------|------|------|
|79397f68-61ed-4ea8-bcb2-f918d4e6c05b|	1/6/2024|	direction |	Green Inc	|1196.95|	85	|28002.8|	32 |Female|	Port Erik |Online|
|4f87d114-f522-4ead-93e3-f336402df6aa|	4/5/2024	|right|	Thomas-Thompson	|1010.34|	64	|2378.82|	55	|Female|	East Linda	|Credit Card|
|6750b7d6-dcc5-48c5-a76a-b6fc9d540fe1|	2/13/2024|	summer|	Sanchez-Williams	|400.8|	95	|31322.56|	57	|Male|	East Angelicastad	|Online|	

### Query Language: (SQL)
Some of the query languges to retrieve records are displayed here

```SQL
---Categorize the data into gold, silver and diamond---
SELECT price,
CASE
WHEN price <=500 THEN 'Silver' WHEN price <=1000 THEN 'Gold' 
ELSE 'Platinum'
END
FROM [dbo].[mobile_sales (1)]


---Retrieve all female customers that bought goods above 900---
SELECT* FROM [mobile_sales (1)]
WHERE CustomerGender = 'female' AND price > 900;


---Retrieve the sales by payment, arranging from largest to smallest amount---
SELECT PaymentMethod, SUM(TotalRevenue) AS Total_Sales FROM [mobile_sales (1)]
GROUP BY PaymentMethod ORDER BY Total_Sales DESC;

---Retrieve the most expensive brand---
SELECT brand, MAX(price) AS expensive_brand FROM [mobile_sales (1)]
GROUP BY brand
ORDER BY expensive_brand DESC;

---How many brands are there?---

## Visualization:
+ PowerBi







```
