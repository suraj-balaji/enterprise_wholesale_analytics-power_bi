# Data Model Documentation

## Model Architecture

The solution was designed using a star schema architecture consisting of:
- One centralized transactional fact table
- Multiple supporting dimension tables
- One-to-many relationships
- Dedicated date dimension


## Fact Table

### FactSales

Contains transactional sales-level data including:
- Revenue
- Profit
- Quantity
- Tax
- Delivery metrics
- Invoice details

Approximate Row Count:
~228K rows

## Dimension Tables

### DimProducts
Contains:
- Product names
- Packaging information
- Product attributes

### DimCustomer
Contains:
- Customer information
- Customer categories

### DimEmployee
Contains:
- Salesperson details

### DimCity
Contains:
- Geographic hierarchy

### DimDate
Dedicated calendar dimension supporting time intelligence analysis.

## Relationships

Implemented one-to-many relationships between:
- FactSales and DimProducts
- FactSales and DimCustomer
- FactSales and DimEmployee
- FactSales and DimCity
- FactSales and DimDate

Relationship Design:
- Single direction filtering
- Optimized cardinality
- Active and inactive date relationships


## Hierarchies

### Geography Hierarchy
Country → Region → State Province → City

### Calendar Hierarchy
Year → Month → Date


## Model Optimization

Optimization techniques included:
- Removal of unnecessary columns
- Hidden technical keys
- Disabled auto date/time
- Centralized measures table
- Reduced high-cardinality fields
- Measure-based calculations

## Security

Implemented Row-Level Security (RLS) for salesperson-level report access simulation.

## Data Model Screenshot

<img width="475" height="338" alt="Data_Model" src="https://github.com/user-attachments/assets/2a7ba59d-fcd0-4b59-82c2-957ebf6cbc80" />
