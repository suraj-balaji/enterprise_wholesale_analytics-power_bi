# Enterprise Wholesale Sales & Profitability Analytics Suite

## Project Overview

This project is an enterprise-style Power BI analytics solution built using the World Wide Importers wholesale distribution dataset.

The objective was to design an interactive business intelligence platform capable of supporting executive reporting, product profitability analysis, operational monitoring, and strategic sales analysis.


## Business Problem

The business lacked centralized visibility into:
- Revenue performance
- Product profitability
- Regional sales trends
- Operational delivery efficiency
- Product contribution analysis

Leadership teams needed an analytics solution capable of supporting faster and more data-driven decision-making.


## Dataset Information

Dataset Used:
- World Wide Importers Dataset

Fact Table:
- FactSales (~228K rows)

Dimension Tables:
- Products
- Customers
- Employees
- Cities
- Calendar Date

Business Domain:
Wholesale import and distribution operations.


## Data Model Architecture

Implemented an enterprise-style star schema model:
- Centralized fact table
- One-to-many relationships
- Dedicated date dimension
- Geography hierarchy
- Product hierarchy
- Optimized relationship filtering

### Data Model

<img width="475" height="338" alt="Data_Model" src="https://github.com/user-attachments/assets/68ece8a1-de3a-47db-bb92-2b5ee26c1809" />



## Executive Overview Dashboard

Features:
- KPI Monitoring
- Revenue Trends
- Profitability Tracking
- Geographic Sales Analysis
- Product Revenue Ranking
- Dynamic Filtering

<img width="593" height="336" alt="Executive_Overview" src="https://github.com/user-attachments/assets/69a53748-b07e-4600-8707-4d5862c47abf" />



## Product Profitability Analytics

Features:
- Scatter Plot Product Segmentation
- Pareto Analysis
- Dynamic Top N
- KPI Switching
- Product Profitability Comparison
- Field Parameters
  
<img width="594" height="335" alt="Product_Analysis" src="https://github.com/user-attachments/assets/4f8f79fc-f07e-4911-98dd-f920905a7a7d" />


## Drillthrough Investigation Page

Implemented drillthrough workflows to support detailed product-level investigation including:
- Revenue trends
- Customer contribution
- Regional performance
- Salesperson analysis

<img width="592" height="335" alt="Drillthrough_Analysis" src="https://github.com/user-attachments/assets/fd2d17f5-91e1-4cc1-aed0-0ad6f917b657" />


## Advanced Power BI Features

- Star Schema Data Modeling
- Advanced DAX Measures
- Dynamic KPI Switching
- Field Parameters
- Pareto Analysis
- Scatter Plot Analytics
- Drillthrough Navigation
- Custom Tooltips
- Mobile Layout Optimization
- Row-Level Security (RLS)
- Performance Optimization


## Key Business Insights

- Revenue was highly concentrated among a limited number of products.
- Several high-revenue products generated relatively lower margins.
- Geographic sales performance varied significantly across states.
- Scatter analysis revealed clear segmentation between strategic and underperforming products.
- Operational delivery performance remained relatively stable across periods.


## Tools & Technologies

- Power BI Desktop
- Power Query
- DAX
- Data Modeling
- Microsoft Bing Maps
- Excel


## Project Outcome

The final solution delivered an enterprise-style analytics experience capable of supporting executive reporting, product profitability analysis, operational monitoring, and interactive business investigation workflows.


## Future plan
Customer Segmentation Analytics </br>
Salesperson Performance Analytics

### Author
Suraj Balaji Bhagaye </br>
bhagayesuraj@gmail.com
