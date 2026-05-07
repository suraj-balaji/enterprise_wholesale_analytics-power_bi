# SECTION 1 —  KPI Measures
## KPI Measures

### Total Revenue


- Total Revenue =
SUM(FactSales[Total Including Tax])

Calculates total sales revenue generated across all transactions.

- Total Profit =
SUM(FactSales[Profit])

Measures total profitability across products and sales.

- Profit Margin % =
DIVIDE(
    [Total Profit],
    [Total Revenue],
    0
)

Evaluates profitability efficiency relative to revenue generation


- Average Order Value =
DIVIDE(
    [Total Revenue],
    [Total Orders],
    0
)

Measures average revenue generated per order transaction


# SECTION 2 — TIME INTELLIGENCE

## Time Intelligence Measures

### Previous Year Revenue
- Previous Year Revenue =
CALCULATE(
    [Total Revenue],
    SAMEPERIODLASTYEAR(DimDate[Date])
)

Compares current revenue against previous year performance.

- YoY Growth % =
DIVIDE(
    [Total Revenue] - [Previous Year Revenue],
    [Previous Year Revenue],
    0
)

Measures year-over-year business growth trends.


---

# SECTION 3 — RANKING MEASURES

## Ranking Measures

### Product Revenue Rank

- Product Revenue Rank =
RANKX(
    ALL(DimProducts[Stock Item]),
    [Total Revenue],
    ,
    DESC
)

Ranks products based on total revenue contribution.


# SECTION 4 — PARETO ANALYSIS
## Pareto Analysis Measures

### Cumulative Revenue

- Cumulative Revenue =
VAR CurrentRank =
    [Product Revenue Rank]

RETURN
CALCULATE(
    [Total Revenue],
    FILTER(
        ALL(DimProducts[Stock Item]),
        [Product Revenue Rank]
            <= CurrentRank
    )
)

Calculates cumulative revenue contribution across ranked products.


- Cumulative Revenue % =
DIVIDE(
    [Cumulative Revenue],
    CALCULATE(
        [Total Revenue],
        ALL(DimProducts[Stock Item])
    )
)

Supports Pareto analysis by identifying revenue concentration patterns.



---

# SECTION 5 — DYNAMIC KPI SWITCHING
## Dynamic KPI Switching

### Selected KPI

- Selected KPI =
SWITCH(
    SELECTEDVALUE(
        'KPI Selector'[KPI]
    ),

    "Revenue", [Total Revenue],
    "Profit", [Total Profit],
    "Margin", [Profit Margin %],
    "Orders", [Total Orders]
)

Allows users to dynamically switch KPI metrics within visuals using slicer-driven interaction.



---

# SECTION 6 — TOP N LOGIC
## Dynamic Top N Analysis

### Selected TopN

- Selected TopN =
SELECTEDVALUE(
    'TopN Selector'[TopN],
    10
)

- Dynamic Product Rank =
RANKX(
    ALL(
        DimProducts[Stock Item]
    ),
    [Total Revenue],
    ,
    DESC
)

- Show TopN Product =
IF(
    [Dynamic Product Rank]
        <= [Selected TopN],
    1,
    0
)

Provides interactive Top N product analysis using dynamic user selection.



---

# SECTION 7 — ROW LEVEL SECURITY

## Row-Level Security (RLS)

### Salesperson Security Logic

- [Employee] = "Lily Code"

Simulates salesperson-level security filtering for controlled report access.


# SECTION 8 — OPTIMIZATION NOTES
## DAX Optimization Notes

Optimization techniques used:
- DIVIDE() instead of manual division
- Measure-based calculations
- Variable usage for cumulative calculations
- Reduced calculated column dependency
- Context-aware filtering
