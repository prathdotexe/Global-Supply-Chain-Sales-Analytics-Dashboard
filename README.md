# Global Supply Chain & Sales Analytics Dashboard

This repository contains an end-to-end **Power BI analytics project** built to analyze **sales performance, customer behavior, shipping efficiency, and cost & risk factors** using real-world supply chain data.

The primary focus of this project is not just visualization, but handling **raw, imperfect data** and transforming it into a **structured, decision-ready business intelligence solution**.

---

## Project Objective

The objective of this project is to demonstrate the complete BI lifecycle:
- Working with messy, real-world datasets
- Cleaning and standardizing data using business logic
- Designing a scalable data model
- Creating meaningful KPIs using DAX
- Building dashboards that support executive, operational, and financial decision-making

---

## Datasets Used

The project integrates three independent datasets representing different layers of a supply chain system:

### 1. Sales & Orders Dataset
Contains transactional-level data including:
- Order details and dates  
- Customer and geographic information  
- Product, category, and department data  
- Sales, profit, discounts, and delivery status  

This dataset is the core source for revenue, customer, and profitability analysis.

### 2. Customer Web Interaction Dataset
Captures digital engagement data such as:
- Product page views  
- Category and department interest  
- Timestamped browsing behavior  

This dataset adds behavioral context to customer demand and product interest.

### 3. Shipment & Logistics Dataset
Focuses on logistics and cost-related information:
- Vendor and shipment details  
- Freight cost and shipment weight  
- Delivery timelines and shipment modes  
- Country-level logistics data  

This dataset is used for cost efficiency, vendor performance, and delivery risk analysis.

---

## Data Cleaning & Preparation

Significant effort was dedicated to data preparation using **Power Query (M)**.

### Raw Data Handling
- All datasets were preserved in their original form as `raw_` queries
- No transformations were applied directly to raw data
- Load was disabled for raw tables to maintain traceability and debugging capability

### Date Standardization
- Multiple date columns contained mixed formats (`MM/DD/YYYY` and `DD/MM/YYYY`)
- Dates were converted to text and conditionally parsed using custom logic
- Clean, standardized date columns were created to support time-based analysis

### Numeric Columns with Business Text
Some numeric fields contained descriptive business text instead of numbers (e.g., freight included, invoiced separately).
- Business-rule-based transformations were applied
- Freight included in product cost was treated as zero
- Values recorded elsewhere were treated as null
- This prevented double counting and incorrect cost assumptions

### Derived Columns
Additional analytical columns were created, including:
- Delivery delay days
- Late delivery flags
- Cost per kilogram
- Clean order and shipping dates

---

## Data Model Design

A **star schema** was implemented to ensure performance and clarity.

### Fact Tables
- Sales transactions
- Shipment records
- Web activity events

### Dimension Tables
- Date
- Customer
- Product
- Category
- Vendor
- Geography

This modeling approach reduces redundancy, simplifies DAX calculations, and improves dashboard performance.

---

## Key Measures (DAX)

The dashboard includes a comprehensive set of measures, such as:
- Total Sales
- Total Orders
- Total Profit
- Profit Margin %
- Average Delay Days
- On-Time Delivery %
- Late Delivery Risk %
- Freight Cost
- Cost per Kilogram

Measures were written using clean, reusable DAX with proper handling of nulls and edge cases.

---

## Dashboard Pages Overview

### Page 1: Executive Overview
Provides a high-level snapshot of overall business performance, including sales, profit, order trends, geographic distribution, and category contribution.

### Page 2: Sales & Customers
Focuses on customer segmentation, top customers, product profitability, and the relationship between discounting and profit.

### Page 3: Shipping & Delivery
Analyzes delivery delays, on-time performance, shipping modes, and country-level logistics efficiency.

### Page 4: Cost & Risk Analysis
Examines freight cost distribution, cost efficiency, late delivery risk, and high-risk orders that require attention.

---

## Key Insights

- Revenue is concentrated among a small set of customers and product categories
- Certain shipping modes and regions consistently contribute to delivery delays
- Excessive discounting often reduces profitability rather than increasing it
- Freight cost efficiency varies significantly across vendors and shipment types
- High-risk orders can be proactively identified using delay and cost indicators

---

## Tools & Technologies

- Power BI
- Power Query (M)
- DAX
- Data Modeling
- Business Intelligence
- Data Cleaning & Transformation

---

## Learning Outcomes

Through this project, I gained hands-on experience in:
- Handling real-world data quality issues
- Translating business problems into analytical metrics
- Designing scalable and explainable BI models
- Writing reliable DAX measures
- Building dashboards that balance executive summaries with operational detail

---

## Future Enhancements

- Predictive modeling for delivery delays
- Sales and demand forecasting
- Vendor performance scoring
- Integration with real-time or API-based data sources

---

## Author

Built as a learning-focused analytics project to strengthen skills in **Data Analytics and Business Intelligence**.

Feedback and suggestions are welcome.
