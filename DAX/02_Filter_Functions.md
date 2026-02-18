# DAX Filter Functions -- Power BI 

## 1️⃣ CALCULATE()

### Definition

CALCULATE modifies the filter context of a calculation and returns the
result based on applied filters.

### Syntax

CALCULATE(Expression, Filter1, Filter2, ...)

### Example

East Sales = CALCULATE( SUM(Sales\[SalesAmount\]), Sales\[Region\] =
"East" )

### Interview Points

-   Most important DAX function
-   Modifies filter context
-   Used in advanced calculations and time intelligence
-   Can override report filters

------------------------------------------------------------------------

## 2️⃣ FILTER()

### Definition

Returns a filtered table based on a condition.

### Syntax

FILTER(TableName, Condition)

### Example

High Sales = CALCULATE( SUM(Sales\[SalesAmount\]), FILTER(Sales,
Sales\[SalesAmount\] \> 1500) )

### Interview Points

-   Returns a table
-   Used inside CALCULATE
-   Evaluates row by row

------------------------------------------------------------------------

## 3️⃣ ALL()

### Definition

Removes filters from a table or column.

### Syntax

ALL(TableName) or ALL(TableName\[ColumnName\])

### Example

Total Sales All = CALCULATE( SUM(Sales\[SalesAmount\]), ALL(Sales) )

### Interview Points

-   Removes filters completely
-   Used for percentage of total
-   Ignores slicers and visual filters

------------------------------------------------------------------------

## 4️⃣ ALLEXCEPT()

### Definition

Removes all filters except specified columns.

### Syntax

ALLEXCEPT(TableName, TableName\[Column\])

### Example

Sales by Region Only = CALCULATE( SUM(Sales\[SalesAmount\]),
ALLEXCEPT(Sales, Sales\[Region\]) )

### Interview Points

-   Keeps specific filter
-   Used in ranking and grouped calculations

------------------------------------------------------------------------

## 5️⃣ VALUES()

### Definition

Returns distinct values from a column as a table.

### Syntax

VALUES(TableName\[ColumnName\])

### Example

Customer List = VALUES(Sales\[CustomerID\])

### Interview Points

-   Returns unique values
-   Affected by filter context
-   Used in advanced DAX logic

------------------------------------------------------------------------

# 🔥 Common Interview Questions

### Q1: What is filter context?

Filter context is the set of filters applied to data by visuals,
slicers, rows, or CALCULATE.

### Q2: Difference between CALCULATE and FILTER?

FILTER returns a table.\
CALCULATE modifies filter context and returns a value.

### Q3: Why is CALCULATE powerful?

Because it can dynamically change filter context.

### Q4: When do we use ALL?

To remove filters and calculate grand totals or percentage of total.

### Q5: Difference between ALL and ALLEXCEPT?

ALL removes all filters.\
ALLEXCEPT keeps specified column filters and removes others.

### Q6: VALUES vs DISTINCT?

Both return unique values, but VALUES is affected by filter context and
returns a table.
