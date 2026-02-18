# 📘 DAX Relationship Functions -- Interview Notes

## 6️⃣ Relationship Functions in DAX (Power BI)

### 🔹 Definition

Relationship functions in DAX are used to access related data between
tables and control how relationships behave during calculations.\
They are mainly used in Star Schema models (Fact & Dimension tables).

------------------------------------------------------------------------

# 1️⃣ RELATED()

### ✅ Definition

Returns a related value from another table using an existing
relationship.\
Works from **Many side → One side**.

### ✅ Syntax

    RELATED(TableName[ColumnName])

### ✅ Example

    Product Name = RELATED(Products[ProductName])

### ✅ Interview Points

-   Works only if relationship exists\
-   Used in Calculated Columns\
-   Moves from Many → One

------------------------------------------------------------------------

# 2️⃣ RELATEDTABLE()

### ✅ Definition

Returns a table of related rows from another table.\
Works from **One → Many side**.

### ✅ Syntax

    RELATEDTABLE(TableName)

### ✅ Example

    Total Quantity =
    SUMX(
        RELATEDTABLE(Sales),
        Sales[Quantity]
    )

### ✅ Interview Points

-   Returns table (not single value)\
-   Used with iterator functions like SUMX\
-   Opposite direction of RELATED

------------------------------------------------------------------------

# 3️⃣ USERELATIONSHIP()

### ✅ Definition

Activates an inactive relationship temporarily during calculation.

### ✅ Syntax

    CALCULATE(
        Expression,
        USERELATIONSHIP(Column1, Column2)
    )

### ✅ Example

    Sales by Ship Date =
    CALCULATE(
        SUM(Sales[SalesAmount]),
        USERELATIONSHIP(Sales[ShipDate], Date[Date])
    )

### ✅ Interview Points

-   Used when multiple relationships exist\
-   Works only inside CALCULATE\
-   Temporarily activates inactive relationship

------------------------------------------------------------------------

# 4️⃣ CROSSFILTER()

### ✅ Definition

Changes the filter direction between two related tables.

### ✅ Syntax

    CROSSFILTER(Column1, Column2, Direction)

Direction Options: - BOTH\
- ONEWAY\
- NONE

### ✅ Example

    Sales Both Direction =
    CALCULATE(
        SUM(Sales[SalesAmount]),
        CROSSFILTER(Sales[ProductID], Products[ProductID], BOTH)
    )

### ✅ Interview Points

-   Overrides model relationship direction\
-   Used in advanced modeling\
-   Temporary effect inside CALCULATE

------------------------------------------------------------------------

# 🔥 Common Interview Questions

### Q1: What is the difference between RELATED and RELATEDTABLE?

-   RELATED returns a single value (Many → One).
-   RELATEDTABLE returns a table of related rows (One → Many).

### Q2: Can RELATED work without a relationship?

No. A relationship must exist between tables.

### Q3: Why do we use USERELATIONSHIP?

To activate an inactive relationship during a specific calculation.

### Q4: When do we use CROSSFILTER?

When we need to temporarily change filter direction for a specific
measure.

### Q5: In which schema are these functions commonly used?

In Star Schema (Fact & Dimension modeling).

------------------------------------------------------------------------

# 🎯 Final Interview Summary

Relationship functions in DAX are used to access and control
relationships between tables.\
RELATED retrieves a value from a related table, RELATEDTABLE returns
related rows, USERELATIONSHIP activates inactive relationships, and
CROSSFILTER changes filter direction.\
These functions are essential in Power BI data modeling and advanced
reporting.
