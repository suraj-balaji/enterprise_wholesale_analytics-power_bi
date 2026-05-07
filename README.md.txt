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

![Data Model](Screenshots/Data_Model.png)


## Executive Overview Dashboard

Features:
- KPI Monitoring
- Revenue Trends
- Profitability Tracking
- Geographic Sales Analysis
- Product Revenue Ranking
- Dynamic Filtering

![Executive Overview](Screenshots/Executive_Overview.png)


## Product Profitability Analytics

Features:
- Scatter Plot Product Segmentation
- Pareto Analysis
- Dynamic Top N
- KPI Switching
- Product Profitability Comparison
- Field Parameters


## Drillthrough Investigation Page

Implemented drillthrough workflows to support detailed product-level investigation including:
- Revenue trends
- Customer contribution
- Regional performance
- Salesperson analysis



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