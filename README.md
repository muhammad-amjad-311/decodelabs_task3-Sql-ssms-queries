# decodelabs_task3-Sql-ssms-queries

🗄 SQL Data Analysis —
Project 3
DecodeLabs | Batch 2026
📌 Overview
E-commerce dataset ka SQL analysis jisme filtering,
grouping, aur aggregations use ki gayi hain.
🛠 Database Setup
create database decodelabs;
use decodelabs;
📋 Queries & Results
1️⃣ View All Data
select * from datatbl;
2️⃣ Filter — Online Payments Only
select * from datatbl where
PaymentMethod='Online';
3️⃣ Filter — Pending Orders Only
select * from datatbl where
OrderStatus='Pending';
4️⃣ Round Decimal Values
update datatbl
set UnitPrice = ROUND(UnitPrice, 2),
 TotalPrice = ROUND(TotalPrice, 2);
5️⃣ Count Total Phone Sales
select count(Product) as TotalPhonesell 
from datatbl 
where Product='Phone';
6️⃣ Count Tablets & Total Tablet Revenue
select count(Product) as TotalTablets, 
 sum(TotalPrice) as
TotalpriceofTablet
from datatbl 
where Product='Tablet';
7️⃣ Total Quantity & Revenue per Product
select Product, 
 sum(Quantity) as TotalQnt,
 sum(TotalPrice) as Totalprice 
from datatbl 
group by product;
8️⃣ Average Price per Product
select product, 
 avg(TotalPrice) as avgprice 
from datatbl 
group by product;
9️⃣ Orders Between 2023–2024 (Sorted by
Date)
select * from datatbl 
where date between '2023-01-01' and '2024-
01-01' 
order by Date asc;
🧠 Concepts Used
Concept Usage
SELECT Data retrieval
WHERE Row filtering
UPDATE Modifying data
ORDER BY Sorting results
GROUP BY Grouping data
COUNT() Counting records
SUM() Total calculations
AVG() Average calculations
ROUND() Decimal precision
BETWEEN Date range filtering
🏷 Tech Stack
SQL Server
SSMS
Powered by DecodeLabs 🚀
