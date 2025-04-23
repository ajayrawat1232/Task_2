## 📊 Power BI Sales Performance Dashboard
## 📌 Project Overview
An interactive sales analytics dashboard built with Power BI, leveraging the AdventureWorks Data Warehouse. This tool enables dynamic tracking of both team and individual sales performance across various regions, products, and time frames.

## ⭐ Key Features
Interactive Filters: Year, Region, Salesperson
Key Metrics: Lifetime Sales, Year-over-Year (YoY) Growth %, Top-Selling Products
Drill-Down Functionality: In-depth analysis of sales reps and regional performance
Product & Regional Insights: Identify high-performing categories and markets

## 🔧 Technical Implementation
## 🛠️ Tools & Technologies
Power BI: Visualization and dashboard development
Power Query: ETL (Extract, Transform, Load) process
DAX (Data Analysis Expressions): Calculated fields and custom metrics

## 🗄️ Data Source
AdventureWorks OLAP Database

## 📐 Data Model: Star Schema
## 🧾 Fact Tables
FactInternetSales: Online B2C sales
FactResellerSales: B2B transactions
FactSalesQuota: Sales goals and targets

## 🧩 Dimension Tables
DimEmployee: Sales reps with regional mapping
DimProduct: Product data (e.g., Bikes, Accessories)
DimDate: Time-based breakdown (Year, Quarter, Month)
DimSalesTerritory: Geographic classification (Country, Region)
Central Fact Table: FactInternetSales
Relationships: Linked via foreign keys (e.g., ProductKey, TerritoryKey)
Optimization: Designed for efficient aggregation and querying

## ⚙️ ETL & Data Preparation (Power Query)
Standardized currency formats (e.g., ₹ to USD)
Cleaned null/missing values
Created calculated columns:
YoY % Growth = DIVIDE([Total Sales] - [Previous Year Sales], [Previous Year Sales])
YTD Sales = TOTALYTD(SUM(FactInternetSales[SalesAmount]), DimDate[Date])

## 📈 Dashboard Highlights
Team Overview: Filterable matrix with yearly and regional performance
Individual Growth: Drill into standout performers (e.g., Rachel Valdez with 815% YoY growth)
Product Trends: Visual analysis by category, highlighting Bikes as the top revenue driver ($1.38M)
